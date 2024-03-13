<template>
 <!-- <img alt="Vue logo" src="./assets/logo.png">``--> 
  <HeaderComponent></HeaderComponent>
  <HelloWorld></HelloWorld>
  <PredComp msg="Weather App soon"/>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import HelloWorld from './components/HelloWorld.vue'
import PredComp from './components/PredComp.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    HelloWorld,
    PredComp
  }
}
</script>

<style lang="scss">
// empty
</style>./components/PredictionsComponent.vue
