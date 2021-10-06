<template>
  <div id="app">
    <Header @searching="searchFilm"/>
    <Main :films="films"/>
  </div>
</template>
    

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import axios from "axios";

export default {
  name: 'App',
  components: {
    Header,
    Main,
  },
  data() {
    return {
      films: []
    }
  },
  methods: {
    searchFilm(query) {
      axios.get('https://api.themoviedb.org/3/search/movie', {
        params: {
          api_key: 'f7e5315902a0e7bdffd73c714f75926d',
          query: query,
          language: 'it-IT'
          
        }
      })
      .then((response) => {
        this.films = response.data.results;
      });
    }
  }
}
</script>

<style lang="scss">

@import './assets/common.scss';

</style>
