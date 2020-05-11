<template>
  <div>
    <span class="name" >按省份选择：</span>
    <m-select title="省份"
    :list="provinceList"
    :value="province"
    :showWrapperActive ="provinceActive"
    @change = "changeProvince"
    @change_active = "changeProvinceActive"
    />
    <m-select
    title="城市"
    :list="cityList"
    :value="city"
    :showWrapperActive ="cityActive"
    @change_active = "changeCityActive"
    @change = "changeCity"
    />

    <span>直接搜索：</span>
       <el-select placeholder="请输入关键词">

       </el-select>
  </div>
</template>

<script>
import MSelect from './select.vue'
export default {
  data(){
    return {
      provinceList: ['山东','甘肃','江苏','北京','云南','海南','浙江','上海'],
      province: '省份',
      cityList: ['合肥','蚌埠','芜湖','淮南','马鞍山','淮北','铜陵',
      '安庆','黄山','滁州','阜阳','宿州','巢湖','六安','亳州','池州',
      '宣城','明光','天长','桐城','太和','无为','芜湖县','繁昌'],
      city: '城市',
      provinceActive: false,
      cityActive: false
    }
  },
  methods: {
    changeProvinceActive(flag){
      this.provinceActive = flag;
      if(flag){
        this.cityActive = false;
      }
    },
    changeCityActive(flag){
      this.cityActive =flag ;
      if(flag){
        this.provinceActive = false;
      }
    },
    changeProvince(item){
      this.province = item;
    },
    changeCity(item){
      this.city=item;
    }
  },
  components: {
    MSelect
  }
}
</script>

<style lang="scss">
  @import '@/assets/css/changecity/iselect.scss';
</style>
