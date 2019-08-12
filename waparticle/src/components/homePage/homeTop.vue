<template>
  <div class="hometop">
    <div :class="['topbg',purple]">
      <div class="navbox">
        <a href="http://m.lotour.com"
           class="wap-zl-home"></a>
        <a href="#"
           class="wap-zl-share"
           @click="sharecl"></a>
      </div>
      <div class="writer">
        <h2 class="wap-h2">
          <p class="name_txt">
            幻羽惊鸿
          </p>
          <span><em>LOTOUR</em>乐途灵感旅行家</span>
        </h2>
        <div class="touxiang">
          <img width="200"
               height="200"
               class="touxiangimg"
               title=""
               src="http://img1.lotour.net/Inspiration/2016/0222/20160222101549346322313_310.jpg   ">
        </div>
        <span class="wap-zl-see"><i></i>2038万+</span>
      </div>

    </div>
    <div class="info">
      <div class="weiwei">
        <p>
          我的微博：幻羽惊鸿z<br>
          我的微信：wx96d4a7co57fof95e
        </p>
      </div>
      <div class="dy_btn_zl"
           style="">
        <img src="http://img1.lotour.net/inspiration/dingyue/dy+w.png"><i>订阅</i>
      </div>
      <div class="ydy_btn_zl"
           style="display: none;">已订阅</div>
      <p class="brief">湖北省作家协会会员，中国民间文艺家协会会员,湖北省教育学会会员，旅游体验师。多家报刊杂志专栏作家，广电APP有游记专栏。</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'hometop',
  data () {
    return {
      purple: 'purple',
      'iscancle': true
    }
  },
  methods: {
    sharecl () {
      this.bus.$emit('sharecl', this.iscancle)
      // console.log(this.iscancle)
    }
  },
}
</script>
<style scoped lang="less">
.hometop {
  position: relative;
  width: 100%;
  // margin-bottom: 4.6rem;
  .topbg {
    width: 100%;
    height: 5.9rem;
    .navbox {
      position: relative;
      .wap-zl-home {
        display: block;
        position: absolute;
        width: 0.5rem;
        height: 0.55rem;
        top: 0.2rem;
        left: 0.21rem;
        background: url(http://img1.lotour.com/writer2/writer-article/wap-home.png)
          no-repeat;
        background-size: 0.5rem 0.5rem;
      }
      .wap-zl-share {
        display: block;
        position: absolute;
        width: 0.55rem;
        height: 0.55rem;
        top: 0.2rem;
        right: 0.2rem;
        background: url(http://img1.lotour.com/writer2/writer-article/wap-share.png)
          no-repeat;
        background-size: 0.5rem 0.5rem;
      }
    }
    .wap-h2 {
      display: block;
      color: #fff;
      font-size: 0.36rem;
      padding-top: 2.6rem;
      text-align: center;
      font-weight: normal;
      // font-family: "Microsoft YaHei";
      .name_txt {
        display: inline-block;
        position: relative;
        line-height: 0.5rem;
      }
      span {
        display: block;
        font-size: 0.2rem;
        filter: alpha(opacity=50);
        opacity: 0.5;
        font-weight: normal;
        letter-spacing: -0.6px;
        em {
          font-family: "Arial";
        }
      }
    }
    .touxiang {
      background: none;
      width: 3.35rem;
      height: 3.35rem;
      margin-top: 0.5rem;
      border: 0.08rem solid rgba(255, 255, 255, 0.5);
      left: 50%;
      position: relative;
      margin-left: -1.76rem;
      border-radius: 100%;
      box-sizing: content-box;
      .touxiangimg {
        display: block;
        width: 3.35rem;
        height: 3.35rem;
        border-radius: 100%;
        margin: 0;
        border: none;
      }
    }
    .wap-zl-see {
      display: block;
      font-size: 0.23rem;
      color: #fff;
      position: absolute;
      bottom: 0.13rem;
      right: 0.17rem;
      font-family: "Arial";
      i {
        width: 0.26rem;
        height: 0.26rem;
        display: inline-block;
        background: url(http://img1.lotour.com/writer2/writer-article/wap-see.png)
          no-repeat;
        background-size: 0.25rem 0.25rem;
        margin-right: 0.03rem;
        position: relative;
        top: 0.03rem;
        opacity: 0.75;
      }
    }
  }
  .info {
    display: block;
    width: 5.8rem;
    margin: 0 auto;
    font-size: 0.24rem;
    color: #333;
    margin-top: 1.8rem;
    margin-bottom: 0.38rem;
    .weiwei {
      font-size: 0.18rem;
      color: #999;
      text-align: center;
      margin-bottom: 0.16rem;
      p {
        display: inline-block;
        text-align: left;
      }
    }
    .dy_btn_zl {
      width: 1.1rem;
      height: 0.42rem;
      background: #ff9900;
      line-height: 0.42rem;
      border-radius: 5px;
      margin: 0 auto;
      margin-bottom: 0.3rem;
      font: 0.2rem/0.4rem \5fae\8f6f\96c5\9ed1, "Microsoft YaHei";
      img {
        display: block;
        float: left;
        margin-top: 0.09rem;
        margin-right: 0.07rem;
        margin-left: 0.2rem;
        width: 0.2rem;
        height: 0.2rem;
      }
      i {
        font-style: normal;
        color: #fff;
      }
    }
    .brief {
      padding: 0 0.45rem;
    }
  }
}
</style>