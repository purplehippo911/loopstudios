<template>
  <HeaderPart/>
  <MainPart/>
  <FooterPart/>
</template>

<script>
import HeaderPart from './components/HeaderPart.vue'
import MainPart from './components/MainPart.vue'
import FooterPart from './components/FooterPart.vue'


export default {
  name: 'App',
  components: {
    HeaderPart,
    MainPart,
    FooterPart
  }
}
</script>

<style lang="scss">
  @import './_variables';

  *, *::before, *::after {
    box-sizing:border-box;
    margin:0;
    padding:0;
  }

body {
  margin:0;
  padding:0;
  background-color: $White;
  font-family: 'Josefin Sans', sans-serif; 
  font-size:15px;
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
