<template>
  <div class = 'tab-control'>
    <div v-for="(item,index) in tabItem"
         class="tab-control-item"
         :class="{active:currentIndex==index}"
         @click="tabClick(index)">
      <span>{{item}}</span>
    </div>
  </div>
</template>

<script>
    export default {
    name: "TabControl",
    props:{
      tabItem:{
        type:Array,
        default(){
          return [];
        }
      }
    },
    data(){
      return {
        currentIndex:0
      }
    },
    methods:{
      tabClick(index){
        this.currentIndex = index;
        this.$emit('tabIsClicked',index);
      }
    }
  }
</script>

<style scoped>
  .tab-control{
    display: flex;
    height: 40px;
    line-height: 40px;
    width: 100%;
    text-align: center;
    font-size: 15px;
    background-color: white;
  }
  .tab-control-item{
    flex: 1;
  }
  .tab-control-item span{
    padding: 5px;
  }
  .active{
    color:var(--color-high-text);
  }
  .active span{
    border-bottom: 2px var(--color-high-text) solid;
  }
</style>
