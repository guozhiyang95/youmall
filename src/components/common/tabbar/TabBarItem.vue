<template>
  <div class="tabbar-item" @click="itemClick" :style="activeStyle">
    <div v-if="!isActive" >
      <slot name="item-icon"></slot>
    </div>
    <div v-else >
      <slot name="item-icon-active"></slot>
    </div>
    <slot name="item-text"></slot>
  </div>  
</template>

<script>
export default {
  name: 'TabBarItem',
  props:{
    path: String,
    activeColor:{
      type: String,
      default: 'red'
    }
  },
  data() {
    return {
      // isActive: true,
    }
  },
  computed: {
    isActive(){
      return this.$route.path.indexOf(this.path) !== -1
    },
    activeStyle(){
      return this.isActive ? {color: this.activeColor} : {}
    }
  },
  methods: {
    itemClick(){
      this.$router.replace(this.path).catch(err=>{});
    }
  },
}
</script>

<style>
  
</style>