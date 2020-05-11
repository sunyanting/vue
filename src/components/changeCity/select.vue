<template>
  <div class="choose-wrap" @click="showWrapper" v-document-click="documentClick">
    <div class="choose">
      <span>{{ value }}</span>
      <i class="el-icon-caret-bottom"></i>
      <div :class="{'mt-content':true,'active': showWrapperActive}" >
        <h2>{{ title }}</h2>
        <div class="wrapper">
          <div class="col">
            <span :class="{'mt-item':true,'active': item==value}"
                  v-for="item in list"
                  :key="item"
                  @click="selectClick(item)"
                  >{{item}}</span>
          </div>
        </div>

      </div>
    </div>

  </div>
</template>

<script>
export default {
  props: ['title','list','value','showWrapperActive'],
  data(){
    return {
      //showWrapperActive: false
    }
  },
  methods: {
    showWrapper(e){
      e.stopPropagation();
      //this.showWrapperActive = true;
      this.$emit('change_active',true)
    },
    selectClick(item){
      //this.value = item;
      this.$emit('change',item);

    },
    documentClick(e){
      //console.log(123);
      // this.showWrapperActive=false;
      this.$emit('change_active',false)
    }
  }
}
</script>

<style lang="scss">
  @import '@/assets/css/changecity/select.scss';
</style>
