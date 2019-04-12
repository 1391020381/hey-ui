<template>
  <div class="tabs-head">
      <slot></slot>
      <div class="line" ref="line"></div>
      <div class="actions-wrapper">
        <slot name="actions"></slot>
      </div>
  </div>
</template>

<script>
export default {
  name:"TabsHead",
  inject:['eventBus'],
  components: {},
  props: {},
  data() {
    return {

    };
  },
  created() {},
  mounted() {
    this.eventBus.$on('update:selected',(item,vm)=>{
      let { width, height ,top ,left } = vm.$el.getBoundingClientRect()
      this.$refs.line.style.width = `${width}px`
      this.$refs.line.style.left = `${left}px`
    })
  },
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
$tab-height:40px;
$blue:blue;
$border-color:#ddd;
.tabs-head{
  display: flex;
  height: $tab-height;
  justify-content: flex-start;
  position: relative;
  border-bottom:1px solid $border-color;
  > .line {
    position: absolute;
    bottom:0;
    border-bottom: 1px  solid $blue;
    transition:all 350ms;
  }
  > .action-wrapper{
    margin-left:auto;
    display: flex;
  }
}
</style>
