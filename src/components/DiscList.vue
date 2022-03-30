<template>
    <div id="disc-list">
        <DiskCard />
    </div>
</template>

<script>
import DiskCard from './DiskCard.vue'

export default {
    name: 'discList',
    components: {
        DiskCard
    },
    created(){

    },
    methods: {
        
    }
}
</script>

<style lang="scss" scoped>
    div#disc-list{
        width: 70%;
        margin: 0 auto;
        padding: 5rem 0;
    }
</style>