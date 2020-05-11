<template>
  <div class="page-product">
    <el-row>
      <crumbs class="m-crumbs"/>
    </el-row>
    <el-row>
      <el-col :span="19">
        <el-row>
          <category />
        </el-row>
        <el-row>
          <list />
        </el-row>
      </el-col>
      <el-col :span="5">
        <slide-right />
      </el-col>
    </el-row>
  </div>
</template>

<script>
import crumbs from '@/components/products/crumbs.vue'
import category from '@/components/products/categroy.vue'
import list from '@/components/products/list.vue'
import slideRight from '@/components/products/slideRight.vue'
export default {
  components: {
    crumbs,
    category,
    list,
    slideRight
  }
}
</script>

<style lang="scss">
  @import '@/assets/css/products/index.scss'
</style>
