<template>
  <div id="app">
    <div id="nav">
      <nav class="navbar navbar-dark bg-primary">
        <span class="navbar-brand mb-0 h1">Shark Info</span>
      </nav>

        <router-link :to="{name: '/'}"></router-link>
      <!-- <div v-for="shark in sharkNames" :key="shark">
          <Card :sharkInfo="shark"/>
      </div> -->

    <router-view/>
    </div>
  </div>
</template>


<script>
import Card from './components/Card.vue'

export default{
  components:{Card},
  
}
</script>





<style>
span{
  padding-left: 20px;
  letter-spacing: 1px;
  font-weight: bold;
  font-size: .6em;
}
.navbar{
  border: none;
  border-radius: 10px;
  margin: 0px 30px;
  
}
.edit{
  display: inline-block;
}
.gridClass{
  margin: 30px auto;
  max-width: 300px;
}
.cardClass{
  letter-spacing: 1px;
  background: rgb(2, 62, 97);
  
  
  border-radius: 5px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
}
body{
  background-color: #29539b;
  background-image: linear-gradient(315deg, #29539b 100%, #1e3b70 74%);
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
