<template>
  <div class="right">
    
     <About id="About"></About>
  
     <Exprence id="Exprence"></Exprence>

     <Skill></Skill>
  </div>
</template>

<script>
import About from '../components/about.vue'
import Exprence from '../components/Exprence.vue'
import Skill from '../components/Skills.vue'
export default {
    data() {
        return {
            
        }
    },
    components:{
      About,
      Exprence,
      Skill,
    }
}
</script>

<style scoped>
    .right{
        position: relative;
        overflow:scroll;
        height: 100vh;
        background-color: #fff4f425;
    }
@media screen and(min-width:430px){
  .myExprence{
    top: 200px;
  }
}
</style>