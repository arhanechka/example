<template>
    <div>
        <h2>Counter {{carName}}</h2>
    </div>
</template>

<script>
import {eventBus} from '../main'

export default {
      data () {
          return {
              carName: 'Ford'
          }
      },
      created(){
          eventBus.$on('UppCar', ()=>{
              this.carName = 'Mazda'
          })

      }
}