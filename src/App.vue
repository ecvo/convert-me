<template>
  <div id="nav">
     <nav class="main-nav">
     <div class="logo_text">
       <router-link class="nav_link_text" @click="$router.replace({path:'/'})" exact>ConvertMe</router-link>
     </div>
     <Burger></Burger>
   </nav>
   <Sidebar>
     <ul class="sidebar-panel-nav">
       <li><router-link class="nav_link" to="/" exact>Главная</router-link></li>
       <li><router-link class="nav_link" to="/choose">Конвертация .docx в .odt</router-link></li>
       <li><router-link class="nav_link" to="/help">Помощь</router-link></li>
     </ul>
   </Sidebar>
  <router-view></router-view>
</div>
</template>
<script>
import Burger from './components/menu/Burger';
import Sidebar from './components/menu/Sidebar';

export default {
 name: 'app',
 components: {
   Burger,
   Sidebar
 }
}
</script>
<style>
html {
  height: 100%;
  overflow:hidden;
  background: #373737;
}

body {
  border: 0; margin: 0; padding: 0;
  font-family: 'Open Sans';
  height: 100%;

 }

.logo_text {
  align-self: center;
  color: #ffffff;
  font-weight: bold;
  font-family: 'Open Sans'
}

.main-nav {
    display: flex;
    justify-content: space-between;
    padding: 0.5rem 0.8rem;
}

ul.sidebar-panel-nav {
    list-style-type: none;
}

.nav_link, .nav_link_text {
    color: #ffffff;
    text-decoration: none;
    font-size: 1.2rem;
    display: block;
    padding-bottom: 0.5em;
}
ul.sidebar-panel-nav > li > .nav_link {
    color: #ffffff;
    text-decoration: none;
    font-size: 1.2rem;
    display: block;
    padding-bottom: 0.5em;
}
</style>
