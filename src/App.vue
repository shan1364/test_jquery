<template>
  <div id="app">
    <div class="component demo">
    
    <div class="alert alert-primary alert-dismissible" role="alert">
       <h4>Alert</h4>
       hello~ <a href="#" class="alert-link">see more.</a> 
       <button class="close" data-dismiss="alert"> 
       &times;
       </button>   
     </div>
     <button class="btn btn-danger close-alert">Close</button>
  
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import HelloWorld from './components/HelloWorld.vue'


@Component({
  components: {
    HelloWorld,
  }
})
export default class App extends Vue {}


$(document).ready( () => {
  $('.close-alert').click( () => {
    $('.alert').alert('close')
  })
$('.alert').on('close.bs.alert', () => {
  console.log('close alert')
})
$('.alert').on('closed.bs.alert', () => {
  console.log('closed alert')
})
})



</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
  margin-left: 30px;
}

.component.demo {
  padding: 50px;
}

</style>
