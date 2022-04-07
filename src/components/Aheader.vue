<template>
   <div class="header">
      <h1>{{h1text}}</h1>
      <h2>{{h2text}}</h2>
      <el-divider></el-divider>
   </div>
</template>

<script>
export default {
    data() {
        return {
     
        }
    },
    props:{
        h1text:String,
        h2text:String,
    }
}
</script>

<style scoped>
    .header{
        left: 2%;
        width: 100%;
        height: 80px;
        border-left: 8px solid blue;
    }
    .header h1{
    font-size: 12px;
    text-transform: uppercase;
    font-weight: 400;
    letter-spacing: 5px;
    color: #888;
    padding-left: 25px;
    padding-top: 5px;
    }
    .header h2{
     font-weight: 500;
    font-size: 28px;
    letter-spacing: 3px;
    text-transform: uppercase;
    margin: 0;
      padding-left: 25px;
    padding-top: 15px;
    }
</style>