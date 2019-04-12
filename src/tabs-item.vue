<template>
  <div class="tabs-item" @click="onClick" :class="classes" :data-nam="name">

  </div>
</template>

<script>
export default {
  name:"TabsItem",
  inject:['eventBus'],
  components: {},
  props: {
    disabled:{
      type:Boolean,
      default:false
    },
    name:{
      type:String|Number,
      required:true
    }
  },
  data() {
    return {
      active:false
    };
  },
  created() {
    if(this.eventBus){
      this.eventBus.$on('update:selected',(name)=>{
        this.active = name === this.name
      })
    }
  },
  mounted() {},
  activited() {},
  update() {},
  beforeRouteUpdate() {},
  methods: {
    onClick () {
      if (this.disabled) { return }
      this.eventBus && this.eventBus.$emit('update:selected',this.name,this)
      this.$emit('click',this)
    }
  },
  filter: {},
  computed: {
    classes () {
      return {
        active :this.active,
        disabled :this.disabled
      }
    }
  },
  watch: {},
};
</script>

<style lang="scss" scoped>

</style>
