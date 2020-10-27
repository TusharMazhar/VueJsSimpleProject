<template>
    <div class="container">
        <h1>Details Information</h1>
        <img src="~/assets/img/person.jpg" alt=" picture" width="400px">
    <h1> 
    <div v-for="person in persons" :key="person.id" >
         
         
         <p v-if="person.id==$route.params.id">

            

             {{person.name}}, Your id is =  {{$route.params.id}}
                 <br>

             {{person.email}}
              <br>
             {{person.details}}
         </p>
    </div>

    </h1>
</div>
</template>
<script>

export default {
     computed:{
       persons(){
          return this.$store.state.persons
           //console.log("Person Array",this.$store.state.persons)
       }
      
    }
    
  
    
}
</script>
<style scoped>
.container{
    background-color: cadetblue;
    border:1px solid black;
    width:500px;
    height:500px;
    text-align:center;
    margin:auto

}
.singleValue{
    color:red;
    
}
</style>