<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <div class="border"></div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
<style>
.border{
  width: 0px;
  height: 0px;
  border-style: solid;
  border-width: 0 20px 20px;
  border-color: transparent transparent #d9534f;
  position: relative;
}
.border:after{
  content: '';
  border-style:solid;
  border-width: 0 15px 15px;
  border-color: transparent transparent #96ceb4;
  position: absolute;
  top: 3px;
  left: -15px;
}
</style>