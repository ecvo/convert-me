<template>
  <div class="help_container">
      <div class="help_container_title">Как это работает:</div>
      <div class="help_container_text">1. Выберите тип конвертации: docx to odt.
      <br>2. Выберите файл который Вы хотите преобразовать в новый формат.
      <br>3. Нажмите кнопку “Начать”, чтобы начать процесс конвертации.
      <br>4. Конвертированный файл сохраниться автоматически в текущей папке файла.</div>
  </div>
</template>

<script>
export default {
    name: 'Help'
}
</script>

<style>
.help_container {
  height: 100%;
  background: #fff;
  padding-left: 1.5em;
}
.help_container_title {
  font-size: 2.2rem;
  font-weight: 600;
  text-decoration: underline;
}
.help_container_text {
  font-size: 1.2rem;
}
</style>