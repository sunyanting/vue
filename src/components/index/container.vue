<template>
  <div>
    <el-row>
      <cone />
    </el-row>
    <el-row>
      <ctwo :nav="nav" />
    </el-row>
    <el-row>
      <cthree />
    </el-row>
  </div>
</template>

<script>
import cone from './cone.vue' ;
import ctwo from './ctwo.vue' ;
import cthree from './cthree.vue' ;
export default {
  data(){
    return {
      nav: [{
        text: "天津",
        tab: 'tj'
      },
      {
        text: "济南",
        tab: 'jn'
      },
      {
        text: "大连",
        tab: 'dl'
      },
      {
        text: "太原",
        tab: 'ty'
      },
      {
        text: "石家庄",
        tab: 'sjz'
      },
      {
        text: "秦皇岛",
        tab: 'qhd'
      },
      {
        text: "呼和浩特",
        tab: 'hhht'
      },
      {
        text: "潍坊",
        tab: 'wf'
      },
      {
        text: "唐山",
        tab: 'ts'
      },
      {
        text: "泰安",
        tab: 'ta'
      }
      ]
    }
  },
  components: {
    cone,
    ctwo,
    cthree
  }
};
</script>

