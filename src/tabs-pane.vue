<template>
  <div class="tabs-pane">

  </div>
</template>

<script>
export default {
  name:"TabsPane",
  inject:['eventBus'],
  components: {},
  props: {
    name:{
      type:String | Number,
      required:true
    }
  },
  data() {
    return {
       active:false
    };
  },
  created() {
    this.eventBus.$on('update:selected',(name)=>{
      this.active = name === this.name
    })
  },
  mounted() {},
  activited() {},
  update() {},
  beforeRouteUpdate() {},
  methods: {

  },
  filter: {},
  computed: {
    classes () {
      return {
        active :this.active
      }
    }
  },
  watch: {},
};
</script>

<style lang="scss" scoped>
.tabs-pane{
  padding:1em;
  &.active {
    
  }
}
</style>
