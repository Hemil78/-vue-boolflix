<template>
  <div id="app">
    <Header @searching="searchFilm"/>
    <Main :films="films" :serie="serieTv"/>
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
      films: [],
      serieTv: [],
      apiKey: 'f7e5315902a0e7bdffd73c714f75926d'
    }
  },
  methods: {
    searchFilm(query) {
      /* creo una costante con i valori che vogliamo passare */
      const params = {
        api_key: this.apiKey,
        query: query,
        language: 'it-IT'
      }
      /* chiamata per i films */
      axios.get('https://api.themoviedb.org/3/search/movie', {
        params: params
      })
      .then((response) => {
        this.films = response.data.results;
      });
      /* chiamata per le serie tv */
      axios.get('https://api.themoviedb.org/3/search/tv', {
        params: params
      })
      .then((response) => {
        this.serieTv = response.data.results;
      });
    }

  }
}
</script>

<style lang="scss">

@import './assets/common.scss';

</style>
