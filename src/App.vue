<template>
  <div id="app">
    <nav class="main-nav">
      <div class="logo_text">
        <router-link class="nav_link_text" to="/">Преобразование документов</router-link>
      </div>
      <Burger></Burger>
    </nav>
    <Sidebar>
      <ul class="sidebar-panel-nav">
        <li>
          <router-link class="nav_link" to="/" exact>Главная</router-link>
        </li>
        <li>
          <router-link class="nav_link" to="/upload">Конвертация .docx в .odt</router-link>
        </li>
        <li><router-link class="nav_link" to="/help">Помощь</router-link></li>
      </ul>
    </Sidebar>
    <transition name="fade" mode="out-in">
      <router-view></router-view>
    </transition>
  </div>
</template>

<script>
import Burger from "./components/menu/Burger";
import Sidebar from "./components/menu/Sidebar";

export default {
  name: "app",
  components: {
    Burger,
    Sidebar,
  },
};
</script>
<style>
#app {
  background: #373737;
  height: 100%;
}
html {
  height: 100%;
  overflow: hidden;
}

body {
  border: 0;
  margin: 0;
  padding: 0;
  font-family: "Open Sans";
  height: 100%;
}

.logo_text {
  align-self: center;
  color: #ffffff;
  font-weight: bold;
  font-family: "Open Sans";
}

.main-nav {
  display: flex;
  justify-content: space-between;
  padding: 0.5rem 0.8rem;
}

ul.sidebar-panel-nav {
  list-style-type: none;
}

.nav_link {
  color: #ffffff;
  text-decoration: none;
  font-size: 1.4rem;
  display: block;
  padding-bottom: 0.5em;
}
.nav_link_text {
  color: #ffffff;
  text-decoration: none;
  font-size: 1.125rem;
  display: block;
  padding-bottom: 0.5em;
}

ul.sidebar-panel-nav > li > .nav_link {
  color: #ffffff;
  text-decoration: none;
  font-size: 1.2rem;
  font-weight: 600;
  display: block;
  padding-bottom: 0.5em;
}
.router-link-active {
  color: rgba(226, 226, 226, 0.74) !important;
}
.nav_link_text {
  color: #ffffff !important;
  cursor: pointer;
  user-select: none;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s !important;
}
.fade-enter,
.fade-leave-to {
  opacity: 0 !important;
}
</style>