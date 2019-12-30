<template>
  <div id="app">
    <img src="./assets/logo.png" />
    <div>
      <el-button @click="startCalc">Calc</el-button>
      <el-button @click="startShow">Show</el-button>
      <el-drawer
      title="Visual Log Drawer"
      :visible.sync="showDrawer"
      :with-header="false"
      direction="btt">
      <view-content :content-data="mockData"></view-content>
      </el-drawer>
    </div>
  </div>
</template>

<script>
import ViewContent from "./visual-log/components/ViewContent.vue";
import { LineType, ViewModeType } from "./visual-log/components/VisualLogType";

export default {
  name: "App",
  data () {
    return {
      mockData: {
        options: {
          viewMode: ViewModeType.containLineNum
        },
        viewData: []
      },
      index: 1,
      showDrawer: false
    }
  },
  methods: {
    startCalc() {
      this.mockData.viewData.push({index: this.index, lineData: {type: LineType.error, message: "test"+this.index}});
      this.index++;
    },
    startShow() {
      this.showDrawer = true;
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
