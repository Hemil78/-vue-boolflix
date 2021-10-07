<template>
  <header>
    <div class="box-logo">
      <img src="../assets/images/logo.png" alt="Boolflix">
    </div>
    <div class="box-search">
      <form>
        <input type="text" v-model="searchText">
        <button tipe="submit" @click.prevent="$emit('searching', searchText)">Search</button>
      </form>
    </div>

  </header>
</template>


<script>
export default {
    name: "Header",
    data() {
        return {
          searchText: ""
      }
    }
}
</script>

<style lang="scss" scoped>

@import '../assets/common.scss';

header{
  background-color: $BGcolorHeader;
  padding: 8px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;

  .box-logo{

    img{
      width: 150px;
    }
  }
  .box-search{

    input{
      width: 300px;
      padding: 8px 12px;
      border-radius: 5px;
      background-color: $BGcolorMain;
      color: #fff;
      border: none;
      margin-right: 20px;
      font-size: 16px;
    }

    button{
      border: none;
      padding: 8px 12px;
      border-radius: 5px;
      background-color: #5c5f64;
      color: #fff;
      font-size: 16px;
      transition: .3s;

      &:hover{
        background-color: #909194;
        color: $BGcolorMain;
      }
    }
  }
}


</style>