<template>
  <HeaderPart/>
  <MainPart/>
</template>

<script>
import HeaderPart from './components/HeaderPart.vue'
import MainPart from './components/MainPart.vue'

export default {
  name: 'App',
  components: {
    HeaderPart,
    MainPart
  }
}
</script>

<style lang="scss">
  @import './_variables';

body {
  margin:0;
  padding:0;
  background-color: $White;
  font-family: 'Josefin Sans', sans-serif; 
}

.container {
  width:80%;
  margin:0 auto;
}

.row {
  display:flex;
  align-items:center;
}

img {
  max-width:100%;
}




</style>
