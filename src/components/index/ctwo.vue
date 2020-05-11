<template>
  <div class="m-two">
    <dl @mouseover="over">
      <dt>推荐民宿</dt>
      <dd v-for="(item,index) in nav"
       :class="{active: kind==item.tab}"
       :key="index"
       :date-type="item.tab">
       {{ item.text }}</dd>
    </dl>
    <ul class="ibody">
        <li v-for="(item,index) in list" :key="index">
          <img :src="item.image" class="product-img">
          <div class="hotel-info">
            <p><span class="title">{{ item.title}}</span></p>
            <p><span class="sub-title">{{item.subTitle}}</span></p>
            <p>
              ¥
              <span class="money">{{item.money}}</span>
            </p>
          </div>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ['nav'],
  data(){
    return {
      kind: 'tj',
      list: [{
        image:'http://p0.meituan.net/iphoenix/6892b7b164e57c2261ebe68644fb476f1881757.jpg@740w_416h_1e_1c',
        title:'【爱无止境】白色婚纱/北欧简约/天津站/意大利风情区/古文化街 地铁2号线直达',
        subTitle:'整套一居室可住2人| 天津站后广场',
        money:168
      },
      {
        image:'https://img.meituan.net/phoenix/e79ceadbe6602e17357a6bcdeeb6ece7228168.jpg@740w_416h_1e_1c',
        title: '嗨图',
        subTitle:'整套一居室可住2人| 图书大厦',
        money:567
      },
      {
        image:'https://img.meituan.net/phoenix/5b7706363118d707a3b43ae5cc8e21dd1040532.jpg@740w_416h_1e_1c',
        title:'【爱无止境】白色婚纱/北欧简约/天津站/意大利风情区/古文化街 地铁2号线直达',
        subTitle:'整套一居室可住2人| 天津站后广场',
        money:168
      },
      {
        image:'https://img.meituan.net/phoenix/9096ac7cc7fd95c6400bbd0cfa27b7dc3613025.jpg@740w_416h_1e_1c',
        title: '嗨图',
        subTitle:'整套一居室可住2人| 图书大厦',
        money:567
      },
      {
        image:'https://img.meituan.net/phoenix/b1b6e52f309afe9d04f6ce0000ac3888927756.jpg@740w_416h_1e_1c',
        title:'【爱无止境】白色婚纱/北欧简约/天津站/意大利风情区/古文化街 地铁2号线直达',
        subTitle:'整套一居室可住2人| 天津站后广场',
        money:168
      },
      {
        image:'https://img.meituan.net/phoenix/84b2a7eea0e6a92ab2766f5d837d01b0164246.jpg@740w_416h_1e_1c',
        title: '嗨图',
        subTitle:'整套一居室可住2人| 图书大厦',
        money:567
      }
      ]
    }
  },
  methods: {
    over(e){
      if(e.target.tagName!=='DD'){
        return ;
      }
      this.kind = e.target.getAttribute('date-type');
    }
  }
}
</script>

<style lang="scss">
  @import "@/assets/css/index/ctwo.scss";
</style>
