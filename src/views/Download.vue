<template>
  <div class="download_container">
    <div class="download_text_container">Преобразованный файл готов</div>
      <form action='http://192.168.0.202:8000/download' method='get'>
        <input type='submit' value='Загрузить' v-on:click='sumbitMain()' />
      </form>
  </div>
</template>

<script>
export default {
    name: 'Download'
    ,
    methods: {
      sumbitMain() {
        setTimeout(() => {
          this.$router.push('/')
        }, 5000);
      }
    }
}
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
  padding: 15px;
}
</style>