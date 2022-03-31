<template>
    <header>
        <nav class="navbar">
            <a class="navbar-brand" href="#">
                <img src="https://www.freepnglogos.com/uploads/spotify-logo-png/spotify-download-logo-30.png" alt="">
            </a>

            <select class="form-select" aria-label="Default select example" v-model="selected">
                <option value="" >Seleziona il Genere</option>
                <option value="rock" @click="$emit('genre', selected)">Rock</option>
                <option value="pop" @click="$emit('genre', selected)">Pop</option>
                <option value="jazz" @click="$emit('genre', selected)">Jazz</option>
                <option value="metal" @click="$emit('genre', selected)">Metal</option>
            </select>
        </nav>
    </header>
</template>

<script>
export default {
    name: 'mainHeader',
    data: function(){
        return{
            selected: '',
        }
    }
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