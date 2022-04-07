<template>
  <div class="About">
    <div class="header1">
      <Aheader :h1text="`information`" :h2text="'about me'"></Aheader>
    </div>
    <div class="img">
      <img
        src="../assets/jing.jpg"
        alt=""
        style="width: 80%; border-radius: 15px"
      />
    </div>
    <div class="Text ">
      <div>
        <p style="font-size: 18px">
          <el-divider content-position="left">学业未完</el-divider>
          <span >
            鄙人小念，生于河南，虽不说苦读数年，但也尽力而为，后求学于南阳~
            <br />
            要『<strong>独立，自信</strong>』这是在这两年本科生涯最大的感触。
          </span>
          <br />

          <el-divider content-position="left">良辰美景</el-divider>
          求学之际偶遇佳人，虽不曾朝朝暮暮，但依稀能看到未来的路<br />
          <el-divider content-position="left">前路漫漫</el-divider>
          因兴趣所致，热情投身猿类大军，由得遇良友，带我认识多方技术栈。<br />
          虽还未能站立于一方天地，每日寻寻问道，自知其中快乐~
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import Aheader from "./Aheader.vue";
export default {
  data() {
    return {};
  },
  components: {
    Aheader,
  },
};
</script>

<style scoped>
.About {
  position: relative;
  height: 550px;
  overflow: scroll;
}
.header1 {
  position: absolute;
  width: 100%;
  left: 3%;
  top: 30px;
}
.img {
  position: absolute;
  width: 23%;
  overflow: hidden;
  top: 150px;
  left: 5%;
}
.Text {
  position: absolute;
  text-align: left;
  top: 120px;
  left: 25%;
  padding: 20px;
}
.Text div {
  padding: 15px;
}
@media screen and (max-width: 1300px) {
  .img {
    display: none;
  }
  .Text {
    left: 10%;
  }
}
</style>