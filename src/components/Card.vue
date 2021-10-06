<template>
  
  <div class="box-card">
    <div class="box-img">
      <img :src="details.backdrop_path" alt="">
    </div>
    <div class="box-text">
      <h3>{{details.title}}</h3>
      <h4>{{details.original_title}}</h4>
      <h5>{{details.original_language}}</h5>
      <h5>{{details.vote_average}}</h5>
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

.box-card{
  width: 100%;

  .box-img{
    width: 100%;

    img{
    width: 100px;
    height: 100px;
    }
  }


  
}

</style>