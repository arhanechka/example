<template>
    <div>
        <h2>{{title}}</h2>
        <p> Counter {{counter}}</p>
        
        <button @click = titlechange>Name</button>
                <button @click = updateCar>UppCar</button>

    </div>
</template>

<script>
import {eventBus} from '../main'
export default {
    props: ['counter', 'title'],
    data() {
        return { 
            carName: 'Ford'
             }
    },
   computed: {
  titleRev(){
    return this.title + "hello"
}

   },
methods: {
titlechange(){
    
   // this.$emit('namech', this.title)
   eventBus.$emit('titleName')
},
updateCar(){
   eventBus.$emit('UppCar')
}
}
}
</script>

 