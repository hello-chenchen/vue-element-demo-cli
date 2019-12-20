<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div>
      <el-button @click="startHacking">Start</el-button>
      <view-content :view-content-data="mockData"></view-content>
    </div>
  </div>
</template>

<script>
import { ViewContent } from "./visual-log/components/ViewContent";

export default {
  name: "App",
  data () {
    return {
      mockData: [{index: 1, lineData: "It works!"}]
    }
  },
  methods: {
    startHacking() {
      this.$notify({
        title: "It works!",
        type: "success",
        message:
          "We've laid the ground work for you. It's time for you to build something epic!",
        duration: 5000
      });
    }
  },
  components: {
    ViewContent
  }
};
</script>
<style>
#app {
  font-family: Helvetica, sans-serif;
  text-align: center;
}
</style>
