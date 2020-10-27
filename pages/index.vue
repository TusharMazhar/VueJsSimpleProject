<template>
  <div class="container" >
    <div class="inside">
       <h1 class="title">SPURT</h1>
       <p class="info">Peronal Information Management</p>
        <nuxt-link  class="linknuxt" to='/users'>Usesr</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.container{
  background-color: black;
  color: white;
  border:1px solid rgb(194, 171, 171);
  width:100%;
  height: 150px;
  text-align: center;
  
}
.inside{
  margin-top:40px;
 
  display:inline-block;
 
  text-align: center;
  
}
.linknuxt{
  text-decoration: none;
  color:red;
  font-size: 30px;
}
</style>
