<template>
  <div class="download_container">
    <div class="download_text_container">
      Ваши преобразованные файлы готовы
      <br />
      Вам будет предложено сохранить как
    </div>
    <router-link to="/upload" class="btn_back">Начать заново</router-link>
  </div>
</template>
<script>
export default {
  name: "Download",
  methods: {},
};
</script>

<style>
.download_container {
  height: 100%;
  padding: 15px;
  margin: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
.download_text_container {
  color: #ffffff;
  font-size: 1em;
  padding: 0px 15px 15px 15px;
}
.btn_back {
  display: block;
  width: 360px;
  height: 50px;
  line-height: 45px;
  font-weight: bold;
  text-decoration: none;
  background: #333;
  text-align: center;
  color: #fff;
  text-transform: uppercase;
  letter-spacing: 1px;
  border: 3px solid #333;
  transition: all 0.35s;
}
.btn_back:hover {
  border: 3px solid #ffffff;
  background: transparent;
  color: #ffffff;
}
</style>