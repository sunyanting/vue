<template>
  <div class="page-changeCity">
    <el-row>
      <province />
    </el-row>
    <el-row>
      <hot title="热门城市:" :list="list" />
    </el-row>
    <el-row>
      <hot title="最近访问:" :list="list" />
    </el-row>
    <el-row>
      <category />
    </el-row>
  </div>
</template>

<script>
import province from '@/components/changeCity/province.vue'
import hot from '@/components/changeCity/hot.vue'
import category from '@/components/changeCity/category.vue'
export default {
  data(){
    return {
      list: ['北京','上海','广州','深圳']
    }
  },
  components: {
    province,
    hot,
    category
  }
}
</script>



