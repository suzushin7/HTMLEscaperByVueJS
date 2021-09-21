<template>
  <div class="html-escaper">
    <p class="main-title">HTML Escaper</p>
    <div class="in">
      <p class="title">Input</p>
      <textarea name="" id="input"></textarea><br />
      <button v-on:click="resetText">Reset</button>
      <button v-on:click="htmlEscape">Escape</button>
    </div>
    <div class="out">
      <p class="title">Output</p>
      <textarea name="" id="output"></textarea>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HTML Escaper',
  props: {
    msg: String
  },
  methods: {
    resetText: () => {
      document.getElementById('input').value = "";
    },
    htmlEscape: () => {
      let src = document.getElementById('input').value;
      src = src.replace(/&/g, "&amp;");
      src = src.replace(/</g, "&lt;");
      src = src.replace(/>/g, "&gt;");
      src = src.replace(/"/g, "&quot;");
      document.getElementById('output').value = src;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.html-escaper {
  border: 1px solid lightblue;
  padding: 5px;
}
.html-escaper div {
  margin-top: 1.0em;
  margin-bottom: 1.0em;
  padding: 10px;
  border: 1px solid #cccccc;
}
.html-escaper textarea {
  width: 280px;
  height: 200px;
  font-size: 15px;
}
.html-escaper button {
  width: 120px;
  height: 30px;
  margin-left: 10px;
  margin-right: 10px;
}
.html-escaper .main-title {
  border-top: 3px double #999999;
  border-bottom: 3px double #999999;
  padding: 10px;
  font-size: 1.25em;
  font-weight: bold;
}
.html-escaper .title {
  border-left: 10px solid #999999;
  border-bottom: 1px solid #999999;
  padding: 10px;
  font-size: 1.25em;
  font-weight: bold;
}
</style>
