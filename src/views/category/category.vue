<template>
  <div id = 'category'>
    <scroll class="category">
      <ul>
        <li>aa</li>
        <button @click="click1">点我！</button>
        <li @click="click2">aa</li>
        <div @click="click3">bb</div>
        <li>aa</li>
        <li>aa</li>
        <li>aa</li>
        <li>aa</li>
        <li>aa</li>
        <li>aa</li>
        <li>aa</li>
        <li>aa</li>
        <li>aa</li>
        <li>aa</li>
        <li>aa</li>
        <li>aa</li>
        <li>aa</li>
        <li>aa</li>
      </ul>
    </scroll>
    <div class="aa">
      11
    </div>
    <div class="bb">22</div>
  </div>
</template>

<script>
  // import BScroll from 'better-scroll';
  import Scroll from 'components/common/scroll/Scroll';
  export default {
    name: "category",
    data(){
      return {
        bscroll:null
      }
    },
    components:{
      Scroll
    },
    methods:{
      click1(){
        console.log('1呗点了');
      },
      click2(){
        console.log('2被点了');
      },
      click3(){
        console.log('3呗点了');
      }

    }

    // mounted(){
    //   this.bscroll = new BScroll('#category',{
    //     probeType:2,
    //     pullUpLoad:true
    //   })
    //   this.bscroll.on('scroll',(position)=>{
    //     // console.log(position);
    //   });
    //   this.bscroll.on('pullingUp',()=>{
    //     console.log('Upload');
    //     this.bscroll.finishPullUp();
    //   })
    // }
  }

</script>

<style scoped>
  .category{
    background-color: red;
    height: 150px;
    overflow: hidden;
    /*overflow-y: scroll;*/
  }
  li{
    font-size:20px;
  }
  .aa{
    width: 100px;
    height: 100px;
    background-color: pink;
    float: left;
  }
  .bb{
    background-color: yellow;
    width: 150px;
    /*height: 100px;*/
  }
</style>
