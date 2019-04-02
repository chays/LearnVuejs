<template>
  <div class="about">
    <h1 class="title">About</h1>

    <div v-bind:class="{'is-active':isActive}" @click="isActiveClick">토글</div>
    <div v-bind:class="{'is-active':isActive}" class="toggle-cont">
      토글 컨텐츠
    </div>
    
  </div>
</template>
<script>
export default {
  data:function(){
    return{
      isActive: false,
    }
  },
  methods:{
    isActiveClick(){
      this.isActive=!this.isActive;
    }
  }
  
}
</script>
<style lang="scss" scoped>
.toggle-cont{
  display:none;
}
.toggle-cont.active{
  display:block;
}
</style>

