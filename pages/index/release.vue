<template>
  <view class="page">
    <view class="nav">
      <!-- 引入官方的导航栏-->
      <uni-nav-bar left-icon="arrowleft" color="#fff" rightText="发布" :statusBar='true'>
        <view class="title" @tap="changeType">
          {{selects[selectsIndex]}}<view class="iconfont icon iconxiala"></view>
        </view>
      </uni-nav-bar>
    </view>
  </view>
</template>

<script>
  import uniIcons from '@/components/uni-icons/uni-icons.vue'
  import uniNavBar from '@/components/uni-nav-bar/uni-nav-bar.vue'
  export default {
    data() {
      return {
        selects:['所有人可见', '仅自己可见'],
        selectsIndex:0 
      }
    },
    methods: {
      changeType(){
        //showActionSheet是uniapp提供的
        uni.showActionSheet({
            itemList: this.selects,
            success: (res) => {
                this.selectsIndex = res.tapIndex;
            }
        });
      }
    },
    components: {
      uniIcons,
      uniNavBar
    }
  }
</script>

<style lang="less" scoped>
  .page {
    .title{
      display: flex;
      margin: 0 auto;
      align-items: center;

      .iconxiala{
          margin-left: 5px;
          margin-top: 2px;
      }
    }
  }
</style>
