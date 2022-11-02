<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Component1></Component1>
    <Component2 title="title1 :"></Component2>
    <Component3></Component3>
    <Component4></Component4>
    <Component5></Component5>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Component1 from './components/Component1.vue'
import Component2 from './components/Component2.vue'
import Component3 from './components/Component3.vue'
import Component4 from './components/Component4.vue'
import Component5 from './components/Component5.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    Component1,
    Component2,
    Component3,
    Component4,
    Component5
  },
  props:['title']
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

button {
margin: 10px;

}

</style>
