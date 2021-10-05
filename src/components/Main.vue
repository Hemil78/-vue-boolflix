<template>
  <main>
    <div class="box-cards">
        <div class="box-card">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus, ipsum. Sit sapiente numquam, voluptates reprehenderit, quia ullam adipisci, illo possimus fugit repudiandae a explicabo ab vel vitae minus cumque incidunt!
            
        </div>
        <div class="box-card">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus, ipsum. Sit sapiente numquam, voluptates reprehenderit, quia ullam adipisci, illo possimus fugit repudiandae a explicabo ab vel vitae minus cumque incidunt!
            
        </div>
        <div class="box-card">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus, ipsum. Sit sapiente numquam, voluptates reprehenderit, quia ullam adipisci, illo possimus fugit repudiandae a explicabo ab vel vitae minus cumque incidunt!
            
        </div>
        <div class="box-card">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus, ipsum. Sit sapiente numquam, voluptates reprehenderit, quia ullam adipisci, illo possimus fugit repudiandae a explicabo ab vel vitae minus cumque incidunt!
            
        </div>
        <div class="box-card">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus, ipsum. Sit sapiente numquam, voluptates reprehenderit, quia ullam adipisci, illo possimus fugit repudiandae a explicabo ab vel vitae minus cumque incidunt!
            
        </div>
        <div class="box-card">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus, ipsum. Sit sapiente numquam, voluptates reprehenderit, quia ullam adipisci, illo possimus fugit repudiandae a explicabo ab vel vitae minus cumque incidunt!
            
        </div>
        <Card/>
    </div>
      
  </main>
</template>

<script>


import Card from './Card.vue';

export default {
    name: "Main",
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

        .box-card{
            width: calc(100% / 5 - 40px);
            margin: 0 20px;
        }
    }
}

</style>