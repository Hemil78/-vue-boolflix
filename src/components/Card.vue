<template>
  
  <div class="container-card">
    
    <div class="box-img">
      <div v-if="details.overview" class="poster">
        <span><small>{{details.overview}}</small></span>
      </div>
      <img v-if="details.poster_path" :src="`https://image.tmdb.org/t/p/w342${details.poster_path}`" alt="">
      <img v-else :src= "require(`../assets/images/sorry.jpg`)">

      <div class="box-vote">

        <img :src= "require(`../assets/images/${details.original_language}.png`)">

        <div class="box-stars">
          <ul v-for= "(star, index) in stars" :key="index">
            <li>
              <i v-if="star <= Math.floor(details.vote_average / 2)" class="fas fa-star"></i>
              <i v-if="star > Math.floor(details.vote_average / 2)" class="far fa-star"></i>
            </li>
          </ul>
        </div>

      </div>
            
    </div>
        

    <div class="box-text">
  
      <div class="box-title">
        <!-- operatore ternario -->
        <h4>{{details.title ? details.title : details.name}}</h4>
        <!-- operatore logico -->
        <span v-if="details.original_title != details.title || details.original_name != details.name">
          <small>{{details.original_title || details.original_name}}</small>
        </span>
      </div>

    </div>
  </div>

</template>
      

<script>
export default {
  name: "Card",
  props: ['details'],
  data() {
    return {
      stars: 5
    }
  },
  methods() {

    }
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
    height: 350px;
    }

    .poster{
      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      background-color: rgba(0, 0, 0, 0.7);
      z-index: 1;
      transition: .3s;
      opacity: 0;
      color: #fff;
      padding: 35px 20px;
      overflow: auto;

      &::-webkit-scrollbar {
        display: none;
      }

      &:hover{
        opacity: 1;
      }
    }

    .box-vote{
      position: absolute;
      left: 0;
      bottom: 0;
      right: 0;
      z-index: 999;
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
      .box-stars{
        display: flex;
        align-items: center;

          ul{
          list-style: none;
          
          li{
            display: inline-block;
            color: rgb(255, 208, 0);
            font-size: 14px;
            margin: 0 2px;
            
          }
        }
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
      padding: 0 10px;

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