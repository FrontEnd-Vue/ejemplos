<template>
 <!-- <div class="container">
    <h2>Fundamentos de Front - End</h2>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quia facilis accusantium itaque doloremque pariatur quis id non quae, vitae voluptates iure laudantium voluptate dolores tempora eaque, debitis odit eligendi ad.</p>
  </div>
   <HelloWorld />
  <ComponentDos /> 
  <Registro /> 
  <UserList />
    <AuthUser />-->
  <NavBar />
  <router-view />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import ComponentDos from './components/ComponentDos.vue'
// import Registro from './components/Registro.vue'
// import UserList from './components/UserList.vue'
//import AuthUser from './components/AuthUser.vue'
import NavBar from "@/components/NavBar";
export default {
  name: 'App',
  components: {
    NavBar
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
