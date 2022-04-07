<template>
  <div class="Skill">
    <div class="header1">
      <Aheader :h1text="`skill`" :h2text="`i can`"></Aheader>
    </div>
    <div class="skills">
        <h5>其实我什么都不会，但我学的快啊!</h5>
     
    </div>
  </div>
</template>

<script>
import Aheader from "./Aheader.vue";
export default {
  components: {
    Aheader,
  },
  methods: {},
};
</script>

<style scoped>
.Skill {
  position: relative;
  width: 100%;
  height: 200px;
}
.header1 {
  position: relative;
  width: 100%;
  left: 3%;
  top: 50px;
}
.skills {
    width: 100%;
  position: relative;
  text-align: center;
  top: 40%;
  
}
</style>