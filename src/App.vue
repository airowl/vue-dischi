<template>
  <div id="app">
    <Header @genre="genreSelected"/>
    <main>
      <DiscList 
        
      />
    </main>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'
import DiscList from './components/DiscList.vue'

export default {
  name: 'App',
  components: {
    Header,
    DiscList
  },
  data: function(){
    return{
      genreSelectedByUser: '',
    }
  },
  methods: {
    genreSelected(selected){
      this.genreSelectedByUser = selected;
    }
  }
}
</script>

<style lang="scss">
@import '@/assets/scss/style.scss';

</style>
