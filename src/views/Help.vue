<template>
  <div class="help_container">
      <div class="help_container_title">Как это работает:</div>
      <br>
      <div class="help_container_text">
      <ol>
        <li>Выберите тип конвертации: docx to odt.</li>
        <li>Выберите файл который Вы хотите преобразовать в новый формат.</li>
        <li>Нажмите кнопку "Начать", чтобы начать процесс конвертации.</li>
        <li>Нажмите кнопку "Загрузить" для сохранения архива с преобразованными файлами</li>
        </ol>
        </div>
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
  background: #373737;
  padding-left: 30px;
}
.help_container_title {
  font-size: 2.2rem;
  font-weight: 600;
  color: #fff;
  text-decoration: underline;
}
.help_container_text {
  font-size: 1.2rem;
  color: #fff;
}
.help_container_text > ol {
  margin: 0;
  padding-left: 22px;
}
</style>