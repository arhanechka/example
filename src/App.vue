<template>
  <div id="app">
     <app-car></app-car>
    <!-- <h2>{{title}}</h2>
   
    <app-counter 
    :counter = counter
    :title = title
    @namech = "title = $event"
    >
    </app-counter>
    <h2> Under Counter</h2>
    <button @click = addCounter()>Add</button> -->
  </div>
</template>

<script>
import Car from './components/Car'
import Counter from './components/Counter'
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Folk App',
      counter: 0,
      title: 'Title from parent'
    }
  },
  components: {
    
    appCar: Car,
    appCounter: Counter
  },
  methods:{
    changeTitle(num){
    return this.title+num
    },
     addCounter(){
    return this.counter++;
},
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
