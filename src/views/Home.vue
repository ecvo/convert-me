<template>
<div class="main_page_main">
  <div class="main_page_text">Преобразование документов</div>
  <div class="wrapper">
  <div class="link_wrapper">
    <router-link class="main_page_link" to="/upload">Начать работу</router-link>
    <div class="icon">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 268.832 268.832">
        <path d="M265.17 125.577l-80-80c-4.88-4.88-12.796-4.88-17.677 0-4.882 4.882-4.882 12.796 0 17.678l58.66 58.66H12.5c-6.903 0-12.5 5.598-12.5 12.5 0 6.903 5.597 12.5 12.5 12.5h213.654l-58.66 58.662c-4.88 4.882-4.88 12.796 0 17.678 2.44 2.44 5.64 3.66 8.84 3.66s6.398-1.22 8.84-3.66l79.997-80c4.883-4.882 4.883-12.796 0-17.678z"/>
      </svg>
    </div>
  </div>
  
</div>
</div>
</template>

<script>
export default {
  name: 'Home'
}
</script>

<style>
.main_page_main {
  height: 100%;
  width: 100%;
  position: relative;
  background: #373737;
}
.main_page_text {
  display: none;
  color: #ffffff;
  font-weight: 500;
  font-size: 2em;
  text-align: center;
  position: fixed;
  top: 38%;
  left: 50%;
  transform: translate(-50%, -50%);
  user-select: none;
}
@media (min-width: 1901px) {
.main_page_text{
  font-size: 2em;
  }
}

@media (min-width: 1601px) and (max-width: 1920px) {
  .main_page_text{
  font-size: 2em;
  }
}

@media (min-width: 901px) and (max-width: 1600px) {
  .main_page_text{
  font-size: 2em;
  }
}
@media (min-width: 300px) and (max-width: 900px) {
  .main_page_text{
  font-size: 1.125em;
  }
}

@media (min-height: 400px) {
  .main_page_text {
    display: block;
  }
  
}
.wrapper{
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.link_wrapper{
  position: relative;
}

.main_page_link {
  display: block;
  width: 350px;
  height: 50px;
  line-height: 50px;
  font-weight: bold;
  text-decoration: none;
  background: #333;
  text-align: center;
  color: #fff;
  text-transform: uppercase;
  letter-spacing: 1px;
  border: 3px solid #333;
  transition: all .35s;
}

.icon{
  width: 50px;
  height: 50px;
  border: 3px solid transparent;
  position: absolute;
  transform: rotate(45deg);
  right: 0;
  top: 0;
  z-index: -1;
  transition: all .35s;
}

.icon svg{
  width: 30px;
  position: absolute;
  top: calc(50% - 15px);
  left: calc(50% - 15px);
  transform: rotate(-45deg);
  fill: #ffffff;
  transition: all .35s;
}

.main_page_link:hover{
  width: 250px;
  border: 3px solid #ffffff;
  background: transparent;
  color: #ffffff;
}

.main_page_link:hover + .icon{
  border: 3px solid #ffffff;
  right: -25%;
}
</style>