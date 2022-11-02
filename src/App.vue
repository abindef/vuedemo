<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Component1></Component1>
    <Component2 title="title1122 :"></Component2>
    <Component3 @func="func"></Component3>
    <Component4  
    v-for="post in posts"
    v-bind:key="post.id"
    v-bind:post="post"></Component4>
    <button @click="sayHello">父子通信</button>
    <Component5 ref="childFef"></Component5>
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
   
  methods:{
    func(arg1,arg2){
        alert(arg1)
        console.log(arg1);
        console.log(arg2);
    },
    sayHello(){
        this.childFef.sayHello();
    }
  },
  data:function() {
        return {
            posts: [
            { id: 1, title: '标题1',content:'内容1' },
            { id: 2, title: '标题2',content:'内容2' },
            { id: 3, title: '标题3' ,content:'内容3'}
            ],
            //childFef:null,
        };
    },
     mounted(){
        this.childFef=this.$refs.childFef;
        console.log(this.childFef.name);
    },
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
