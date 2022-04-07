<template>
  <!-- 左侧菜单实现 -->

  <div class="Menu" ref="show">
    
    <div class="SMenu" @click="SMenu">
      <i class="el-icon-s-unfold" style="font-size: 25px"></i>
    </div>
    <el-drawer
      title="侧边导航栏 虽然功能并没有实现"
      :visible.sync="drawer"
     
      :modal="true"
      :size="`40%`"
      :show-close="false"
    >
      <div class="list list1" >
        <ul>
           <li><a href="javascipt:;" @click="scroll()">首页</a></li>
          <li><a href="#About">关于</a></li>
          <li><a href="#Exprence">经历</a></li>
          <li><a href="javascipt:;"  @click="scroll()">乱七八糟</a></li>
        </ul>
      </div>
    </el-drawer>
    <div class="leftMenu">
      <div class="user">
        <div class="userimg">
          <el-avatar :size="120" :src="imgurl"></el-avatar>
        </div>
      </div>
      <div class="list">
        <ul>
          <li><a href="javascipt:;" @click="scroll()">首页</a></li>
          <li><a href="#About">关于</a></li>
          <li><a href="#Exprence">经历</a></li>
          <li><a href="javascipt:;"  @click="scroll()">乱七八糟</a></li>
        </ul>
      </div>
      <div class="Github"></div>
    </div>
  </div>
</template>

<script scoped>
export default {
  data() {
    return {
      imgurl:
        "https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fb-ssl.duitang.com%2Fuploads%2Fitem%2F201804%2F09%2F20180409214117_Q4AS3.thumb.700_0.jpeg&refer=http%3A%2F%2Fb-ssl.duitang.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651753452&t=aa295fde50b576d8d0eb39f3dedcd0ac",
      drawer: false,
    };
  },
  methods: {
    scroll() {
      window.scrollTo({
        top: 0,
        behavior: "smooth",
        show:'none',
      })
    },
  SMenu(){
    this.drawer=true
  }
  },
};
</script>

<style scoped>
.Menu {
  position: relative;
  width: 100%;
  height: 100vh;
  background-image: url("../assets/leftbc.jpg");
  background-size: 100% 100%;
  background-repeat: no-repeat;
  box-shadow: 0px 0px 1.5px #000000;
}
.close{
  position: absolute;
  color: white;
  font-size: 25px;
  right: 5%;
  top: 5%;
}
.user {
  width: 100%;
  height: 30%;
}
.userimg {
  position: absolute;
    left:50%;
   top:10%;
    transform: translate(-50%);

}
.list {
  position: absolute;
  width: 100%;
  top: 35%;
  margin: 0;
}

.list ul{
  position: absolute;
  width: 100%;
  left:75%;
  transform: translate(-50%);
}
.list ul li {
  text-align: center;
  line-height: 45px;
  height: 45px;
  width: 40%;
  border-bottom: 1px solid rgb(136, 136, 136);
  list-style: none;
}
.list a {
  font-size: 20px;
  font-weight: bolder;
  color: rgb(47, 66, 64);
  text-decoration: none;
}
.list a:hover {
  color: rgba(19, 166, 199, 0.697);
}
.SMenu {
  position: absolute;
  background-color: #dcdfe6;
  border-radius: 100%;
  width: 35px;
  height: 35px;
  margin: 40px;
  z-index: 1;
  display: none;
  text-align: center;
  line-height: 40px;
  border: 1px solid black;
}
.Smenu:hover {
  box-shadow: 0 0 10px black;
}
@media screen and (max-width: 1100px) {
  .leftMenu {
    display: none;
  }
  .Menu {
    width: 0;
    height: 0;
  }
  .SMenu {
    display: block;
  }
}
</style>