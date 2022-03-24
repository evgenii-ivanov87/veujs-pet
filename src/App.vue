<template>
      <h1>{{title}}</h1>
      <ButtonItem @click="increment" >Click me</ButtonItem>
  
  
</template>

<script>
import ButtonItem from './components/Button.vue';

export default {
  name: 'App',
  components: {
    ButtonItem
  },
  data(){
    return{
      amountOfCliks:0
    }
  },
  computed:{
    title(){
      return `Amount Of Cliks ${this.amountOfCliks}`
    }
  },
  methods:{
    increment(){
      this.amountOfCliks+=1
    }
  }
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
</style>

