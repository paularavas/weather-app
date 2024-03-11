<template>
 <!-- <img alt="Vue logo" src="./assets/logo.png">``--> 
  <HeaderComponent></HeaderComponent>
  <HelloWorld msg="Weather App soon"/>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    HelloWorld
  }
}
</script>

<style lang="scss">
// empty
</style>
