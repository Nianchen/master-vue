<template>
  <div class="banner">
    <div class="bg"></div>

    <div
      class="
        desc
        animate__animated animate__fadeIn animate__1 animate__delay-1s
      "
    >
      <div class="userimg">
        <el-avatar :size="160" :src="imgurl"></el-avatar>
      </div>
    </div>
    <div>
      <h1>{{ typewriter }}</h1>
    </div>
    <div class="next" @click="next">》</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      imgurl:
        "https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fb-ssl.duitang.com%2Fuploads%2Fitem%2F201804%2F09%2F20180409214117_Q4AS3.thumb.700_0.jpeg&refer=http%3A%2F%2Fb-ssl.duitang.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1651753452&t=aa295fde50b576d8d0eb39f3dedcd0ac",
      typewriter: "",
      i: 0,
      timer: 500,
      str: "这里是故人叹，正在努力赶往未来。",
    };
  },
  components: {},
  methods: {
    next() {
      window.scrollTo({
        top: window.innerHeight,
        behavior: "smooth",
      });
    },
    typeing() {
      if (this.i <= this.str.length) {
        this.typewriter = this.str.slice(0, this.i++);
        this.timer = setTimeout(() => {
          this.typeing();
        }, 80);
      } else {
        clearTimeout(this.timer);
      }
  

    },
  },
  mounted() {
    this.typeing();
  },
};
</script>

<style scoped>
.banner {
  display: flex;
  position: relative;
  justify-content: center;
  align-items: center;
  width: 100vw;
  height: 100vh;
  overflow-x: hidden;
  text-shadow: 0 0 5px rgb(27, 27, 27);
  color: white;
}

.bg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
  background: url("../assets/bc1.png") no-repeat center center scroll;
  background-size: cover;
}
.desc {
  position: absolute;
}
.userimg {
  position: absolute;
  top:-300px;
  transform: translate(-50%);
}
h1 {
  font-size: 35px;
  font-family: "楷体";
  text-shadow: 25px 25px 15px black;
}

.next {
  position: absolute;
  left: 49.4%;
  bottom: 20%;
  cursor: pointer;
  font-size: 35px;
  transform: rotate(90deg);
  animation-name: tiao;
  animation-duration: 2s;
  animation-iteration-count: infinite;
  animation-timing-function: ease;
  animation-direction: alternate-reverse;
}
@keyframes tiao {
  0% {
    bottom: 20%;
  }

  100% {
    bottom: 10%;
  }
}
</style>