<template>
  <div class="wapshare disblock"
       v-show="iscancle">
    <div class="zz"
         v-show="iszz">
      <img :src="shareimg">
      <p class="know"
         @click="iknow">我知道啦!</p>
    </div>
    <div class="share_cont"
         style="display: block;">
      <div class="share_all">
        <span class="ss s1"
              @click="s1">
          <img src="http://img1.lotour.com/xingqu_m/share_icon_03.png"
               style="visibility: visible;">
          <span>微信</span>
        </span>
        <span class="ss s1"
              @click="s2">
          <img src="http://img1.lotour.com/xingqu_m/share_icon_01.png"
               style="visibility: visible;">
          <span>朋友圈</span>
        </span>
        <a href="javascript: eval(sns_share_show('wb_tinfo_1', '如果不出去走走，你会以为这就是世界！幻羽惊鸿的专栏主页，湖北省作家协会会员，中国民间文艺家协会会员,湖北省教育学会会员，旅游体验师。多家报刊杂志专栏作家，广电APP有游记专栏。@乐途旅游网官方微博', '', 'http://m.zhuanlan.lotour.com/1160/', '','1160')); void 0;"
           class="ss s3">
          <img src="http://img1.lotour.com/grzx/ico-share_03.png"
               style="visibility: visible;">
          <span>微博</span>
        </a>
        <span class="ss s4"
              @click="s4">
          <img src="http://img1.lotour.com/xingqu_m/share_icon_02.png"
               style="visibility: visible;">
          <span>QQ</span>
        </span>
        <a href="javascript: eval(sns_share_show('qz_tinfo_1', '幻羽惊鸿的专栏主页，湖北省作家协会会员，中国民间文艺家协会会员,湖北省教育学会会员，旅游体验师。多家报刊杂志专栏作家，广电APP有游记专栏。@乐途旅游网', '', 'http://m.zhuanlan.lotour.com/1160/', '','1160')); void 0;"
           class="ss s5">
          <img src="http://img1.lotour.com/grzx/ico-share_09.png"
               style="visibility: visible;">
          <span>QQ空间</span>
        </a>
      </div>
      <p class="share_cancle"
         @click="cancle">取消</p>
    </div>
  </div>
</template>

<script>
export default {
  // props: ['iscancle'],
  data () {
    return {
      'iszz': false,
      'iscancle': false,
      'shareimg': ''
    }
  },
  created () {
    this.bus.$on('sharecl', iscancle => {
      this.iscancle = iscancle
    })
  },
  methods: {
    s1 () {
      this.iszz = true;
      console.log(this.iszz);
      this.shareimg = 'http://img1.lotour.com/xingqu_m/other-wchat.png'
    },
    s2 () {
      this.iszz = true;
      this.shareimg = 'http://img1.lotour.com/xingqu_m/other-ring.png'
    },
    s4 () {
      this.iszz = true;
      this.shareimg = 'http://img1.lotour.com/xingqu_m/other-qq.png'
    },
    iknow () {
      this.iszz = false
    },
    cancle () {
      this.iscancle = !this.iscancle
      // console.log(iscancle)
    }
  },
}
</script>
<style scoped lang="less">
.wapshare {
  display: block;
  position: fixed;
  left: 0;
  bottom: 0;
  top: 0;
  right: 0;
  z-index: 11;
  text-align: center;
  background: rgba(0, 0, 0, 0.5);
  .zz {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 999;
    background: rgba(0, 0, 0, 0.5);
    // display: none;
    img {
      display: block;
      width: 100%;
      position: absolute;
      bottom: 1.75rem;
      left: 0;
      width: 100%;
      height: auto;
    }
    .know {
      position: absolute;
      bottom: 3.4rem;
      right: 2.38rem;
      width: 1.5rem;
      font: 0.24rem/0.55rem "微软雅黑";
      color: #ff9900;
      text-align: center;
    }
  }
  .share_cont {
    position: absolute;
    bottom: 0;
    background: #fff;
    width: 100%;
    display: none;
    .share_all {
      width: 5.973rem;
      height: 2.304rem;
      margin: 0 auto;
      .ss {
        width: 1.194rem;
        margin-top: 0.512rem;
        display: block;
        float: left;
        img {
          display: block;
          margin: 0 auto;
          width: 0.853rem;
          height: 0.853rem;
        }
        span {
          width: 100%;
          display: block;
          margin-top: 0.28rem;
          font: 0.2rem/0.26rem "微软雅黑";
          color: #666;
          text-align: center;
        }
      }
    }
    .share_cancle {
      height: 0.8rem;
      border-top: 1px solid #cdcdcd;
      text-align: center;
      display: block;
      width: 100%;
      font: 0.3rem/0.8rem \5fae\8f6f\96c5\9ed1, "Microsoft YaHei";
      color: #008cee;
    }
  }
}
</style>