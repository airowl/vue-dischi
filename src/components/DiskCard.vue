<template>
    <div id="disk-card">
        <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
        <h5>New Jersey</h5>
        <p>Bon Jovi</p>
        <p>1988</p>
    </div>
</template>

<script>
export default {
    name: 'diskCard'
}
</script>

<style lang="scss" scoped>
    div#disk-card{
        background-color: #2e3a46;
        text-align: center;
        width: calc((100% / 5) - 2rem);
        height: calc((100% / 2) - .5rem);
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