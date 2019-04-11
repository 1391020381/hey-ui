<!-- row -->
<template>
  <div class="row" :style="{marginLeft:-gutter/2+'px',marginRight:-gutter/2+'px'}">
  <slot></slot>
  </div>
</template>
<script>
export default {
  name:'GuluRow',
  props:{
    gutter:{
      type:[Number,String]
    }
  },
  data () {
    return {
    }
  },
  components: {},
  computed: {},
  created(){
    console.log('row crated')
  },
  mounted(){
    console.log('row mounted')
    console.log('this.$children')
    this.$children.forEach(vm=>{
      vm.gutter = this.gutter
    })
    var div = document.createElement('div')
    var childDiv = document.createElement('div')
    div.appendChild(childDiv)
    document.body.appendChild(div)
  },
  methods: {}
}

</script>
<style lang='scss' scoped>
.row{
  display: flex;
}
</style>