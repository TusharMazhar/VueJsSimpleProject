<template>
   <div>
    <h1 class="allusers">ALL USERS</h1>
    <ul>
        <li v-for="person in persons" :key="person.id" v-on:click="specificPerson(person.id)">

            <div class="personDiv">
              
                <img src="~/assets/img/person.jpg" alt="customer" width="100%" height="120px">
               
                <br>
                <span class="singleValue">{{person.name}} </span>
                 <br>
                <span class="singleValue">{{person.email}} </span>
           </div>
            
        </li>
    </ul>
   
</div>
</template>
<script>
import PersonId from '../../pages/users/_id/index'
export default {

    // data(){
    //     return{
    //         persons:[
    //             {name:"Tushar ",email:"tushar@gmail.com",details:"Working in inneed cloud" , id:1},
    //              {name:"Belal ",email:"belal@gmail.com",details:"Working in inneed cloud" ,id:2},
    //               {name:"Akib ",email:"Akib@gmail.com",details:"Working in inneed cloud" ,id:3},
    //                {name:"mursalin ",email:"mursalin@gmail.com",details:"Working in inneed cloud" ,id:4},
    //                 {name:"ashik ",email:"ashik@gmail.com",details:"Working in inneed cloud" ,id:5},
    //                  {name:"Asad ",email:"asad@gmail.com",details:"Working in inneed cloud" ,id:6},
    //                   {name:"Sadman",email:"sadman@gmail.com",details:"Working in inneed cloud" ,id:7},
    //                    {name:"Anik",email:"anik@gmail.com",details:"Working in inneed cloud" ,id:8},
    //                     {name:"Manik",email:"manik@gmail.com",details:"Working in inneed cloud" ,id:9},
    //                      {name:"Shakib",email:"shakib@gmail.com",details:"Working in inneed cloud" ,id:10},
    //         ]
    //     }
    // },
    computed:{
       persons(){
          return this.$store.state.persons
           //console.log("Person Array",this.$store.state.persons)
       }
      
    },
    components:{
        PersonId 

    },
    methods:{
        specificPerson(id){
            this.$router.push("/users/"+id)
        }
    }
    

}
</script>

<style scoped>
  ul{
      text-decoration: none;
  }
  li{
      list-style-type: none;
  }
  .personDiv{
      background-color: rgb(2, 2, 2);
      color:white;
      display: inline-block;
      margin-top:10px;
      margin-bottom:10px;
      width:250px;
      text-align: center;


  }
  .allusers{

      margin-left:80px;
      color:red;
  }
 

</style>