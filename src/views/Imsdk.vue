<template>
   <div class="gaodesdk">
       <el-amap vid="amapDemo"     class="amap-demo"> </el-amap>
   </div>
</template>

<script>
import { AMapManager,lazyAMapApiLoaderInstance } from 'vue-amap'
export default {
    name:"Index",
    data(){
        return{
            map:null,
            zoom:12,
            events:{}
        }
    },
    mounted(){
        lazyAMapApiLoaderInstance.load().then(()=>{
            this.map = new AMap.Map('amapDemo',{
               
                    center:new AMap.LngLat(116.404765,39.918052),
                    zoom:this.zoom
                
            })
        })
    }

}
</script>

<style>
.gaodesdk{
    height: 100%;
}
</style>