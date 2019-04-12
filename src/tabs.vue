<template>
  <div class="tabs">
   <slot></slot>
  </div>
</template>

<script>
import Vue from 'vue'
export default {
  name:"Tabs",
  components: {},
  props: {
    selected:{
      type:String,
      required:true
    },
    direction:{
      type:String,
      default:'horizontal',
      validator (value) {
        return ['horizontal','vertical'].indexOf(value) >=0
      }
    }
  },
  data() {
    return {
       eventBus :new Vue()
    };
  },
  provide () {
    return {
      eventBus :this.eventBus
    }
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
