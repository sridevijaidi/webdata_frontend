<template>
<div>
    <h1> <a href="https://sridevij.herokuapp.com/"> {{aboutme  }} </a> </h1>
    
</div>
</template>

<script>

export default{
    name: 'About',
    props:{
        aboutme: String
        
    }
}

</script>

<style scoped>

div{
    text-align: center;
}
a{
    text-decoration: none;
    color: black;
}
</style>