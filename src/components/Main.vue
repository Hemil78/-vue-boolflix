<template>
  <main>
      <Card/>
  </main>
</template>

<script>

import axios from 'axios';
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

</style>