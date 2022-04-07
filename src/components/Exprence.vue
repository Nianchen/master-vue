<template>
  <div class="Exprence">
    <div class="header1">
      <Aheader :h1text="`Exprence`" :h2text="`MY exprence`"></Aheader>
    </div>
    <div class="myExprence">
      <div class="block">
        <el-timeline>
          <el-timeline-item timestamp="2020/10/8" placement="top" color="blue">
            <el-card>
               <p>南阳理工 2020/10/8 08:56</p>
              <h3>虽然高考成绩算不上特别好，但好歹尽力而为了，两年前带上行李继续追赶人生的下一趟列车</h3>
            </el-card>
          </el-timeline-item>
          <el-timeline-item timestamp="2018/4/3" placement="top">
            <el-card>
              <h4>更新 Github 模板 没啥可写的了 随便扔点啥</h4>
              <p>王小虎 提交于 2018/4/3 20:46</p>
            </el-card>
          </el-timeline-item>
          <el-timeline-item timestamp="2018/4/2" placement="top">
            <el-card>
              <h4>更新 Github 模板</h4>
              <p>王小虎 提交于 2018/4/2 20:46</p>
            </el-card>
          </el-timeline-item>
           <el-timeline-item timestamp="2018/4/2" placement="top">
            <el-card>
              <h4>更新 Github 模板</h4>
              <p>王小虎 提交于 2018/4/2 20:46</p>
            </el-card>
          </el-timeline-item>
           <el-timeline-item timestamp="2018/4/2" placement="top">
            <el-card>
              <h4>更新 Github 模板</h4>
              <p>王小虎 提交于 2018/4/2 20:46</p>
            </el-card>
          </el-timeline-item>
           <el-timeline-item timestamp="2018/4/2" placement="top">
            <el-card>
              <h4>更新 Github 模板</h4>
              <p>王小虎 提交于 2018/4/2 20:46</p>
            </el-card>
          </el-timeline-item>
        </el-timeline>
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
.Exprence{
  position: relative;
  /* height: 550px; */
  margin-bottom: 50px;
}
.header1 {
  position: relative;
  width: 100%;
  left: 3%;
  top: 30px;
}
.myExprence{
    position: relative;
    width: 85%;
    left: 8%;
    top: 80px;
}
.black{
  /* overflow: scroll; */
}
.el-card:hover{
  box-shadow: 0px 0px 3px black;
}

  

</style>