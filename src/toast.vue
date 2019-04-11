<template>
  <div class="wrapper" :class="toastClasses">
      <div class="toast" ref="toast">
          <div class="message">
              <slot v-if="!enableHtml"></slot>
              <div v-else v-html="$slots.default[0]"></div>
          </div>
          <div class="line" ref="line"></div>
          <span class="close" v-if="closeButton" @click="onClickClose">
              {{closeButton.text}}
          </span>
      </div>
  </div>
</template>

<script>
export default {
  name:"Toast",
  components: {},
  props: {
      autoClose:{
          type:[Boolean,Number],
          default:5,
          validator (value){
              return value === false || typeof value === 'number'
          }
      },
      closeButton:{
          type: Object,
          default () {
              return {
                  text:'关闭',callback:undefined
              }
          }
      },
      enableHtml: {
          type: Boolean,
          default:false
      },
      position:{
          type:String,
          default: 'top',
          validator (value) {
              return ['top','bottom','middle'].indexOf(vlaue)>=0
          }
      }
  },
  data() {
    return {

    };
  },
  created() {},
  mounted() {},
  activited() {},
  update() {},
  beforeRouteUpdate() {},
  methods: {
   onClickClose(){

}
  },
  filter: {},
  computed: {},
  watch: {},
};
</script>

<style lang="scss" scoped>

</style>
