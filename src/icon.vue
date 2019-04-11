<!-- icon -->
<template>
  <svg class="g-icon">
    <use :xlink:href="`#i-${name}`"></use>
  </svg>
</template>

<script>
import svg from './svg.js'
export default {
  name:'GuluIcon',
  props:['name'],
  data () {
    return {
    }
  },
  components: {},
  computed: {},
  mounted(){},
  methods: {}
}

</script>
<style lang='scss' scoped>
.g-icon {
  width:1em;
  height: 1em;
}
</style>