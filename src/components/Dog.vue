<template>
   
    <div>
       <h2>{{dog.dogbreed}}</h2>
       <h4>{{dog.behavoiur}}</h4>
       <h4>{{dog.description}}</h4>
       <h4>{{dog.breedcost}}</h4>
       <h4>{{dog.breedlifetime}} </h4>
    </div>
   
   
   
</template>

<script>

export default{
    name: 'Dog',
    props:{
        dog: Array
    }
   
}
</script>

<style scoped>

h4{
    margin: 2px;
}


div{
    background-color: #69e9dec5;
    color: #171718;
    padding: 1em;
}



</style>