<template>
  <div class="container">
    
    <Myheader mytitle="Pet Dogs" 
      aboutpage ="Dog Breeds" />
    
    <Dogbox :dogs = "dogs"/>
    <About aboutme="About" />
    



  </div>
</template>
<script>




import Myheader from './components/Myheader.vue'
import About from './components/About.vue'


import Dogbox from './components/Dogbox.vue'



export default {
  name: 'App',
  components: {
    // 2 register the component 
    Myheader,
    Dogbox,
    About
  },

  data(){
    return {
      dogs: []
    }
  },
  methods: {
    // promises

      async fetchDogs(){
         const res= await fetch('https://sridevij.herokuapp.com/db.json')
         const data= await res.json()
          console.log(data)
         return data
      }

  },

  async created(){
    this.dogs = await this.fetchDogs()
  }
}
</script>


<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;
}

</style>


