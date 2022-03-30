<template>
    <div id="disk-card">
        <img :src="image" alt="">
        <h5>{{title}}</h5>
        <p>{{author}}</p>
        <p>{{year}}</p>
    </div>
</template>

<script>
export default {
    name: 'diskCard',
    props: ['image', 'title', 'author', 'year']
}
</script>

<style lang="scss" scoped>
    div#disk-card{
        background-color: #2e3a46;
        text-align: center;
        width: calc((100% / 5) - 2rem);
        height: calc(100% / 2);
        padding: 1rem;
        margin-bottom: 1rem;

        img{
            width: 100%;
        }

        h5{
            margin: 1rem 0;
            text-transform: uppercase;
        }

        p{
            color: #6a6460;
        }
    }
</style>