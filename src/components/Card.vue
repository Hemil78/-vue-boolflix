<template>
  
  <div class="container-card">
    <div class="box-img">
      <img :src="`https://image.tmdb.org/t/p/w342${details.backdrop_path}`" alt="">
    </div>
    <div class="box-text">
      <span><strong>{{details.title}}</strong></span><br>
      <span>{{details.original_title}}</span><br>
      <span>{{details.original_language}}</span><br>
      <span>{{details.vote_average}}</span>
    </div>
      
  </div>
</template>

<script>
export default {
    name: "Card",
    props: ['details']
    
}
</script>

<style lang="scss" scoped>

@import '../assets/common.scss';

.container-card{
  width: 100%;

  .box-img{
    width: 100%;

    img{
    width: 100%;
    }
  }
}
.box-text{
  width: 100%;
  text-align: center;
  h3{
    display: block;
  }
  h4{

  }
}

</style>