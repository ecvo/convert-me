<template>
  <div class="choose_container">
    <div class="choose_text_container">Загрузите ваш файл</div>
    <form
      class="choose_form_container"
      ref="uploadForm"
      id="uploadForm"
      action="http://192.168.0.202:8000/upload"
      method="post"
      encType="multipart/form-data"
    >
      <div class="file-upload">
        <div class="file-select">
          <div class="file-select-button" id="fileName">Выберите файл</div>
          <div class="file-select-name" id="noFile">Файл не выбран...</div>
          <input
            type="file"
            name="sampleFile"
            id="sampleFile"
            accept="application/vnd.openxmlformats-officedocument.wordprocessingml.document"
            multiple='multiple'
            required
          />
        </div>
      </div>
      <br />
      <input type="submit" value="Начать" v-on:click="submit()" />
    </form>
  </div>
</template>

<script>
import $ from 'jquery';

export default {
  name: 'Upload',
  data(){
      return {
        sampleFile : null
      }
    },
    methods: {
          submit(event){
        if( $('#sampleFile').val() == ""){
       event.preventDefault()
       
   }
   else{
        this.$router.push('/download')
   }
       }
    },
    mounted() {
      $('#sampleFile').bind('change', function () {
        var filename = $("#sampleFile").val();
        if (/^\s*$/.test(filename)) {
          $(".file-upload").removeClass('active');
          $("#noFile").text("No file chosen..."); 
        } else {
          $(".file-upload").addClass('active');
          $("#noFile").text(filename.replace("C:\\fakepath\\", "")); 
  }
});

    }     
  }
</script>

<style>
.choose_container {
  height: 100%;
  padding: 0;
  margin: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.choose_text_container {
  font-size: 1em;
  color: #ffffff;
  padding: 15px;
}

.choose_form_container {
  display: flex;
  align-items: left;
  justify-content: left;
  flex-direction: column;
}

input[type="submit"] {
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
input[type="submit"]:hover {
  border: 3px solid #ffffff;
  background: transparent;
  color: #ffffff;
}

.file-upload {
  display: block;
  text-align: center;
  font-size: 12px;
}

.file-upload .file-select {
  display: block;
  border: 2px solid #dce4ec;
  color: #333;
  cursor: pointer;
  height: 40px;
  line-height: 40px;
  text-align: left;
  background: #ffffff;
  overflow: hidden;
  position: relative;
}

.file-upload .file-select .file-select-button {
  background: #dce4ec;
  padding: 0 10px;
  display: inline-block;
  height: 40px;
  line-height: 40px;
}

.file-upload .file-select .file-select-name {
  line-height: 40px;
  display: inline-block;
  padding: 0 10px;
}

.file-upload .file-select:hover {
  border-color: #333;
  transition: all 0.2s ease-in-out;
  -moz-transition: all 0.2s ease-in-out;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
}

.file-upload .file-select:hover .file-select-button {
  background: #333;
  color: #ffffff;
  transition: all 0.2s ease-in-out;
  -moz-transition: all 0.2s ease-in-out;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
}

.file-upload.active .file-select {
  border-color: #3fa46a;
  transition: all 0.2s ease-in-out;
  -moz-transition: all 0.2s ease-in-out;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
}

.file-upload.active .file-select .file-select-button {
  background: #3fa46a;
  color: #ffffff;
  transition: all 0.2s ease-in-out;
  -moz-transition: all 0.2s ease-in-out;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
}

.file-upload .file-select input[type="file"] {
  z-index: 100;
  cursor: pointer;
  position: absolute;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
  opacity: 0;
  filter: alpha(opacity=0);
}

.file-upload .file-select.file-select-disabled {
  opacity: 0.65;
}

.file-upload .file-select.file-select-disabled:hover {
  cursor: default;
  display: block;
  border: 2px solid #dce4ec;
  color: #34495e;
  cursor: pointer;
  height: 40px;
  line-height: 40px;
  margin-top: 5px;
  text-align: left;
  background: #ffffff;
  overflow: hidden;
  position: relative;
}

.file-upload .file-select.file-select-disabled:hover .file-select-button {
  background: #dce4ec;
  color: #666666;
  padding: 0 10px;
  display: inline-block;
  height: 40px;
  line-height: 40px;
}

.file-upload .file-select.file-select-disabled:hover .file-select-name {
  line-height: 40px;
  display: inline-block;
  padding: 0 10px;
}
</style>