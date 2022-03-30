<template>
    <div>
        <div id="disc-list" v-if="musicList">
            <DiskCard 
            v-for="(element, index) in musicList"
            :key="index"
            :image="element.poster"
            :title="element.title"
            :author="element.author"
            :year="element.year"
            />
        </div>
        <div class="loader position-absolute top-50 start-50 translate-middle" v-else>
            <h3>Loading...</h3>
        </div>
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
        setTimeout(this.apiGetMusic, 10000)
        
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
        padding: 2.3rem 0;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }
</style>