<template>
   <div>
      <div class="container">
         <div><img src="../assets/download (1).png" alt=""></div>
      </div>
      <div class="register">
         <div><input class="name" v-model="name" placeholder="Enter Name"/></div>
         <div> <input class="email" v-model="email" placeholder="Enter Email"/></div>
         <div><input class="password" v-model="password" placeholder="Enter Password"/></div>
         <button v-on:click="signUp">Sign Up</button>
      </div>
   </div> 
 </template>
<script>
 import axios from 'axios'
 export default {
    name: 'Sign Up',
    data(){
      return{
        name: '',
        email: '',
        password: '',
      }
    },
    methods:{
     signUp(){
      let result = axios.post("http://localhost:3000/user",{
        email:this.email,
        password:this.password,
        name:this.name,
      });
      console.warn(result);
      if(result.status=201){
        alert("sign up done");
        localStorage.setItem("user-info", JSON.stringify(result.data));
        this.$router.push({name:'Home'})
      }
     }
    },
    mounted()
    {
      let user=localStorage.getItem("user-info");
      if(user){
        this.$router.push({name:'Home'})
      }
    }
 }
</script>
<style>
 #app{
    font-family: Avenir, Arial, Helvetica, sans-serif;
    align-content: center;
    
 }
 .container{
   display: flex;
   flex-direction: column;
   
   justify-content: center;
   align-items: center;
 }
 .text-signUp{
   color: lightsalmon;
 }
 .name {
   width: 500px;
   height: 40px;
   border: 1px solid lightsalmon;
   border-radius: 5px;
   
 }
 .email {
   width: 500px;
   height: 40px;
   border: 1px solid lightsalmon;
   border-radius: 5px;
 }
 .password {
   width: 500px;
   height: 40px;
   border: 1px solid lightsalmon;
   border-radius: 5px;

 }
 .register{
   display: flex;
   justify-content: center;
   align-items: center;
   flex-direction: column;
   gap: 15px;
 }
 


</style>