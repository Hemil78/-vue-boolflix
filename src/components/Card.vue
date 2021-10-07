<template>
  
  <div class="container-card">
    <div class="box-img">
      <img :src="`https://image.tmdb.org/t/p/w342${details.poster_path}`" alt="">

      <div class="box-vote">
        <img :src= "require(`../assets/images/${details.original_language}.png`)">
        <span>{{details.vote_average}}</span>
      </div>

    </div>
    <div class="box-text">
      
      <div class="box-title">
        <!-- operatore ternario -->
        <h4>{{details.title ? details.title : details.name}}</h4>
        <!-- operatore logico -->
        <span><small>{{details.original_title || details.original_name}}</small></span>
      </div>

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
    position: relative;
    width: 100%;
    margin-bottom: 5px;

    img{
    width: 100%;
    height: 320px;
    }

    .box-vote{
      position: absolute;
      left: 0;
      bottom: 0;
      right: 0;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 30px 5px 5px 5px;
      background: linear-gradient( rgba(0, 0, 0, 0), #000 );

      img{
      width: 25px;
      height: 25px;
      }
      span{
        color: #fff;
      }
    }
  }
  .box-text{
    display: flex;
    flex-direction: column;
    width: 100%;
    text-align: center;
    color: #fff;

    .box-title{

      h4{
      margin-bottom: 0;
      }

      span{
        color: $ColorSmallText;
      }
    }
    
  }
}
</style>