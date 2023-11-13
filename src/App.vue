<script>
  import SignUp from "./components/SignUp.vue"
  export default{
    name: 'App',
    components:{
      SignUp,
    }
  }
</script>

<template>
   <div class="container">
    <img class="logo" src="./assets/logo.jpg" alt="">
    <h1 class="text">Sign Up</h1>
    <div class="register">
      <input type="text" placeholder="Enter name" />
      <input type="text" placeholder="Enter Email" />
      <input type="text" placeholder="Enter Password" />
      <button class="button">Sign Up</button>
    </div>
   </div>

  
</template>

<style>
 
 .logo{
    width: 100px;
    position: relative;
    left: 400px;
   
   
    
   
 }
 .register input{
   width: 300px;
   height: 40px;
   padding-left: 20px;
   display: block;

   margin-bottom: 10px;
   margin-right: auto;
   margin-left: auto;
   border: 1px solid brown;
 
 }
 .text{
   font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
   font-size: medium;
   color: rgb(163, 76, 76);
   position: relative;
   left: 425px;
   bottom: 10px;
 }
 .register button{
  position: relative;
  left: 307px;
  font-size: smaller;
  border-radius: 5px;
  border: none;
  color: white;
  cursor: pointer;
  width: 302px;
  height: 40px;
  background: rgb(163, 76, 76) ;
 }



 
</style>
