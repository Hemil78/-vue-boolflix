<template>
  <main>
    <h2>Movies</h2>
    <div class="box-cards">
        <div class="box-card" v-for="(film, index) in films" :key="index">
          <Card :details="film"/> 
        </div>
    </div>
    <h2>Serie TV</h2>
    <div class="box-cards">
        <div class="box-card" v-for="(episode, index) in serie" :key="index">
          <Card :details="episode"/> 
        </div>
    </div>
      
  </main>
</template>
            

        

<script>


import Card from './Card.vue';

export default {
    name: "Main",
    props: ['films', 'serie'],
    components: {
        Card
    }
    
}
</script>




<style lang="scss" scoped>

@import '../assets/common.scss';

main{
    background-color: $ColorSmallText;
    padding: 20px 20px;
    background-color: $BGcolorMain;

    h2{
      color: #fff;
      margin-bottom: 10px;
    }

    .box-cards{
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        

        .box-card{
            width: calc(100% / 6 - 8px);
            margin: 0 4px;
            margin-bottom: 30px;
        }
    }
}

</style>