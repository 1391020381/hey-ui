<template>
  <div class="cascader" ref="cascader" >
      <div class="trigger">

      </div>
      <div class="popover-wrapper" >

      </div>
  </div>
</template>

<script>
// cascader 的数据流
// cascader 的子类数据是怎么挂载到页面上的

import CascaderItems from './cascader-items.vue'
export default {
  name:"Cascader",
  components: {CascaderItems},
  props: {
    source:{
      type:Array
    },
    popoverHeight:{
      type:String
    },
    selected:{
      type:Array,
      default:()=>{
        return []
      }
    },
    loadData:{
      type:Function
    }
  },
  data() {
    return {
      popoverVisible:false,
      loadingItem:{}
    };
  },
  created() {},
  mounted() {},
  activited() {},
  update() {},
  beforeRouteUpdate() {},
  methods: {

  },
  filter: {},
  computed: {},
  watch: {},
};
</script>

<style lang="scss" scoped>

</style>
