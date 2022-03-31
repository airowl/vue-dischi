<template>
    <header>
        <nav class="navbar">
            <a class="navbar-brand" href="#">
                <img src="https://www.freepnglogos.com/uploads/spotify-logo-png/spotify-download-logo-30.png" alt="">
            </a>
            <select class="form-select" aria-label="Default select example">
                <option selected>Seleziona il Genere</option>
                <option value="1">Rock</option>
                <option value="2">Pop</option>
                <option value="3">Jazz</option>
                <option value="4">Metal</option>
            </select>
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

        nav.navbar{

            a{
                width: 4rem;

                img{
                    width: 100%;
                }
            }

            select{
                width: 30%;
            }
        }
        

    }
</style>