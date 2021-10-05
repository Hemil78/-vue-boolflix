<template>
  <header>
    <div class="box-logo">
      <h1>BOOLFLIX</h1>
    </div>
    <div class="box-search">
      <input type="search">
    </div>

  </header>
</template>

<script>
export default {
    name: "Header",
    props: ['logo']
}
</script>

<style lang="scss" scoped>

@import '../assets/common.scss';

header{
  background-color: #000;
  padding: 8px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;

  .box-logo{

    h1{
      color: red;
    }
  }
  .box-search{

    input{
      padding: 8px 12px;
      border-radius: 5px;
    }
  }
}


</style>