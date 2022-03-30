<template>
    <div id="disc-list">
        <DiskCard 
        v-for="(element, index) in musicList"
        :key="index"
        />
    </div>
</template>

<script>
import axios from 'axios';
import DiskCard from './DiskCard.vue'

export default {
    name: 'discList',
    components: {
        DiskCard
    },
    data: function(){
        return {
            musicList: null
        }
    },
    created(){
        this.apiGetMusic()
    },
    methods: {
        apiGetMusic(){
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then((result) => {
                this.musicList = result.data.response;
                console.log(this.musicList);
            })
        }
        
    }
}
</script>

<style lang="scss" scoped>
    div#disc-list{
        width: 70%;
        margin: 0 auto;
        padding: 5rem 0;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-evenly;
    }
</style>