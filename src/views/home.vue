<template>
  <div>
    <el-row class="layout-header">
      <el-col :span="24">
        <div id="Banner">
          <Banner></Banner>
        </div>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="6" style=""><Menu> </Menu> </el-col>
      <el-col :span="18"
        ><div><right></right></div
      ></el-col>
    </el-row>
  </div>
</template>

<script>
import Banner from "../components/Banner.vue";
import Menu from "../components/Mune.vue";
import right from "../views/right.vue";
export default {
  data() {
    return {};
  },
  components: {
    Banner,
    Menu,
    right,
  },
};
</script>

<style>
* {
  margin: 0;
}
.layout-header {
  overflow: hidden;
  padding: 0;
}
.Smenu {
  position: absolute;
}
@media screen and(min-width: 1100px) {
  .el-col-18 {
    width: 100%;
  }
}
</style>