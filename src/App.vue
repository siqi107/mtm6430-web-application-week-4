<template>
  <div id="app">
    <div>
      <input type="text">
    </div>
    <el-button type="primary" @click="openDiag = true">Welcome</el-button>
    <el-dialog :visible.sync="openDiag">
      <input type="text" v-model="sendTreat">
      <HelloWorld msg="My first App"/>
      <Simba v-bind:treat="sendTreat"/>
    </el-dialog>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Simba from "./components/Simba";

export default {
  name: "app",
  components: {
    HelloWorld,
    Simba
  },
  data: function() {
    return {
      sendTreat: "Raw Hide",
      openDiag: false
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
