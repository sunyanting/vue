<template>
  <div class="m-three">
    <dl>
      <dt>猜你喜欢</dt>
      <dd class="active">为你甄选最适合的</dd>
    </dl>
   <ul class="ibody">
     <li v-for="(item,index) in list" :key="index">
       <img :src="item.image" class="image">
       <p>
         <span class="title">{{ item.title }}</span>
       </p>
       <p>
         <span v-for="item in 5" :key="item">
           <i class="el-icon-star-on"></i>
         </span>
         <span class="score">{{item.score}}个评价</span>
       </p>
       <p>
         <span class="address">{{ item.address}}</span>
       </p>
       <p>
         <span class="money">¥{{ item.money }}起</span>
       </p>
     </li>
   </ul>
  </div>
</template>

<script>
export default {
  data(){
    return {
      list:[{
        image:'//p1.meituan.net/poi/b0588c60f5885dc1aec50fa82f579bc5178176.jpg@214w_120h_1e_1c',
        title:'铁木真自助涮烤城（石景山店）',
        score:'1141',
        address:'鲁谷',
        money: '82.9'
      },{
        image:'//p0.meituan.net/bbia/73ed163f933a1e79deeb233b520d83b5267387.jpg@214w_120h_1e_1c',
        title:'蟹老宋香锅（方庄店）',
        score:'14569',
        address:'刘家窑/宋家庄',
        money: '50.0'
      },{
        image:'//p1.meituan.net/msmerchant/2dc4a686f4b7eb35bab80b4789b5ee192070548.jpg@214w_120h_1e_1c',
        title:'铁木真自助涮烤城（石景山店）',
        score:'1141',
        address:'鲁谷',
        money: '82.9'
      },{
        image:'//p1.meituan.net/msmerchant/98a0e4b1aafa7c0418753aed4575d94c1444319.jpg@214w_120h_1e_1c',
        title:'蟹老宋香锅（方庄店）',
        score:'14569',
        address:'刘家窑/宋家庄',
        money: '50.0'
      },{
        image:'//p1.meituan.net/mogu/0da0cd3be3a6a1e107ca8fe6eb639ef967394.jpg@214w_120h_1e_1c',
        title:'铁木真自助涮烤城（石景山店）',
        score:'1141',
        address:'鲁谷',
        money: '82.9'
      },{
        image:'//p1.meituan.net/mogu/0da0cd3be3a6a1e107ca8fe6eb639ef967394.jpg@214w_120h_1e_1c',
        title:'蟹老宋香锅（方庄店）',
        score:'14569',
        address:'刘家窑/宋家庄',
        money: '50.0'
      },{
        image:'//p0.meituan.net/merchantpic/e3f61992caf9efaf93750bfc7fd88b7e33151.jpg@214w_120h_1e_1c',
        title:'铁木真自助涮烤城（石景山店）',
        score:'1141',
        address:'鲁谷',
        money: '82.9'
      },
      {
        image:'//p1.meituan.net/msmerchant/0a0cca979d4602ac3b9a5b04ddfa6d3e95958.jpg@214w_120h_1e_1c',
        title:'蟹老宋香锅（方庄店）',
        score:'14569',
        address:'刘家窑/宋家庄',
        money: '50.0'
      },
      {
        image:'//p1.meituan.net/bbia/9b2926a2c8812d693818a067b86939e4454342.jpg@214w_120h_1e_1c',
        title:'铁木真自助涮烤城（石景山店）',
        score:'1141',
        address:'鲁谷',
        money: '82.9'
      },{
        image:'//p0.meituan.net/bbia/f58fafc0be2bc3a69dfcac20260888c2201000.jpg@214w_120h_1e_1c',
        title:'蟹老宋香锅（方庄店）',
        score:'14569',
        address:'刘家窑/宋家庄',
        money: '50.0'
      },{
        image:'//p1.meituan.net/bbia/3e36af692ce40ea56575b7c19dc3581c464792.png@214w_120h_1e_1c',
        title:'铁木真自助涮烤城（石景山店）',
        score:'1141',
        address:'鲁谷',
        money: '82.9'
      },
      {
        image:'//p0.meituan.net/msmerchant/4bbd54ec513e6ab035a4083d1c2683a74978152.jpg@214w_120h_1e_1c',
        title:'蟹老宋香锅（方庄店）',
        score:'14569',
        address:'刘家窑/宋家庄',
        money: '50.0'
      },
      {
        image:'//p1.meituan.net/bbia/66fd7b3ea9b59d4687b42e07a514013593187.jpg@214w_120h_1e_1c',
        title:'铁木真自助涮烤城（石景山店）',
        score:'1141',
        address:'鲁谷',
        money: '82.9'
      },
      {
        image:'//p0.meituan.net/mogu/858f9caa9fbcc0f55cfb6f33ac63d69733687.jpg@214w_120h_1e_1c',
        title:'蟹老宋香锅（方庄店）',
        score:'14569',
        address:'刘家窑/宋家庄',
        money: '50.0'
      },
      {
        image:'//p1.meituan.net/joymerchant/6053e5b18897846a5f17b71f70c6f1b5--1632437674.jpg@214w_120h_1e_1c',
        title:'铁木真自助涮烤城（石景山店）',
        score:'1141',
        address:'鲁谷',
        money: '82.9'
      }
      ]
    }
  }

}
</script>
<style lang="scss">
  @import "@/assets/css/index/cthree.scss";
</style>
