<template>
    <header>
        <nav class="navbar">
            <a class="navbar-brand" href="#">
                <img src="https://www.freepnglogos.com/uploads/spotify-logo-png/spotify-download-logo-30.png" alt="">
            </a>
        </nav>
    </header>
</template>

<script>
export default {
    name: 'mainHeader',
}
</script>

<style lang="scss" scoped>
    header{
        background-color: #2e3a46;
        padding: 0 1rem;

        a{
            width: 4rem;

            img{
                width: 100%;
            }
        }

    }
</style>