<template>
  <main>
    <h2>Movies</h2>
    <div class="box-cards">
        <div class="box-card" v-for="(film, index) in films" :key="index">
          <Card :details="film"/> 
        </div>
    </div>
      
  </main>
</template>
            

        

<script>


import Card from './Card.vue';

export default {
    name: "Main",
    props: ['films'],
    components: {
        Card
    }
    
}
</script>




<style lang="scss" scoped>

@import '../assets/common.scss';

main{
    background-color: $ColorSmallText;
    padding: 20px 0;

    .box-cards{
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        border: 1px solid red;

        .box-card{
            width: calc(100% / 5 - 40px);
            margin: 0 20px;
            border: 1px solid green;
        }
    }
}

</style>