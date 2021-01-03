<template>
<!-- 地图 -->
  <div id="about">
    <el-amap vid="amapDemo"  :center="center" :zoom="zoom" > </el-amap>
  </div>
  
</template>

<script>

export default {
   name:"about",
   data(){
     return {
       zoom:18,
       center:[113.30025,23.04291],
       
     }
   },
   methods:{
     
   }
}
</script>

<style>
#about{
  height: 100%;
}
 
</style>
