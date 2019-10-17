<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  mounted() {
    var urlParam = location.search.substring(1);
    var paramArray = [];

    // パラメータが存在確認、無ければ何もしない
    if (urlParam) {
        // 「&」が含まれている場合は「&」で分割
        var param = urlParam.split('&');
        // パラメータを格納する用の配列を用意
        // 用意した配列にパラメータを格納
        for (var i = 0; i < param.length; i++) {
            var paramItem = param[i].split('=');
            paramArray[paramItem[0]] = paramItem[1];
        }

        //if (paramArray.te === "ppp") {
            //document.getElementById("app").style.display = "none";
        //}
        alert("text=" + paramArray.text);
        alert("url=" + paramArray.url);
        alert("title=" + paramArray.title);
        alert("all=" + param);

}
},
methods:{

}
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
