<template>
  <div class="homearticle">
    <div class="navarticle">
      <span class="st st-one on">文章(<em>103</em>)<i class="arrow-down"></i></span>
    </div>
    <div class="wap-article">
      <ul>
        <!-- {{article}} -->
        <li v-for="(item,index) in article"
            :key="index">
          <div class="wap-pic-index">
            <img src="http://img1.lotour.com/writer2/writer-article/wap-shouye.png"
                 alt="上首页">
          </div>
          <a :href="item.Url"
             target="_blank">
            <img :src="item.HeadPic"
                 style="display: block;"></a>
          <h2><a :href="item.Url">{{item.Title}}</a></h2>
          <div class="tags clearfix">
            <div class="inbox">
              <a href="#"
                 target="_blank"
                 class="in"
                 v-for="(v,i) in item.Tags.split(',')"
                 :key="i"
                 v-if="v ? v : ''">{{v}}</a>
            </div>
            <span id="spq75974"
                  class="fr look"><img src="http://img1.lotour.com/writer2/writer-article/wap-see2.png">52871</span>
          </div>
        </li>
      </ul>
    </div>

  </div>
</template>

<script>

import axios from 'axios'

export default {
  data () {
    return {
      article: []
    }
  },
  created () {
    axios.get('https://www.easy-mock.com/mock/5d4b77e1df3ead4c90c93ce6/homePage/article').then(res => {
      this.article = res.data.data
    })
  }
}
</script>
<style scoped lang="less">
.homearticle {
  position: relative;
  width: 100%;
  height: auto;
  background: #ebf0f2;
  .navarticle {
    position: relative;
    margin-bottom: 0.2rem;
    height: 0.86rem;
    line-height: 0.86rem;
    border-top: 1px solid #eee;
    font-size: 0.25rem;
    text-align: center;
    color: #000;
    background: #fff;
    em {
      font-family: "Arial";
    }
    .arrow-down {
      width: 0;
      height: 0;
      border-left: 0.2rem solid transparent;
      border-right: 0.2rem solid transparent;
      border-bottom: 0.2rem solid #ebf0f2;
      position: absolute;
      bottom: 0;
      left: 50%;
      margin-left: -0.3rem;
    }
  }
  .wap-article {
    display: block;
    margin: 0 0.2rem;
    font-family: "Microsoft YaHei";
    margin-bottom: -0.4rem;
    li {
      border-bottom: 0.02rem solid #d0d3d9;
      padding-bottom: 0.38rem;
      margin-bottom: 0.4rem;
      border-radius: 3px;
      overflow: hidden;
      position: relative;
      .wap-pic-index {
        position: absolute;
        top: 0.15rem;
        right: 0.17rem;
        width: 2rem;
        height: 0.34rem;
        img {
          float: right;
          width: 0.74rem;
          margin: 0.04rem 0 0 0;
        }
      }
      img {
        width: 100%;
        height: auto;
        border: 0 none;
        float: left;
        margin: 0 0 2px 0;
        border-radius: 3px;
        -moz-border-radius: 3px;
        -webkit-border-radius: 3px;
      }
      h2 {
        color: #333;
        font-size: 0.31rem;
        a {
          color: #333;
          margin: 0.13rem 0 0.08rem 0.18rem;
          display: inline-block;
          line-height: 24px;
          font-weight: normal;
        }
      }
      .tags {
        margin-left: 0.18rem;
        overflow: hidden;
        padding-bottom: 0.03rem;
        .inbox {
          float: left;
          width: 4.7rem;
          height: 0.4rem;
          overflow: hidden;
          .in {
            color: #a4a4a4;
            font-size: 0.18rem;
            border: 1px solid #c1c1c1;
            float: left;
            margin: 0 1px;
            border-radius: 15px;
            padding: 0 0.14rem 0.01rem 0.14rem;
          }
        }
        .look {
          display: block;
          float: right;
          font-size: 0.18rem;
          color: #b8b8b8;
          margin: 0.04rem 0.15rem 0 0;
          font-family: "Arial";
          img {
            width: 0.2rem;
            height: auto;
            position: relative;
            margin-top: 0.06rem;
            margin-right: 0.05rem;
          }
        }
      }
    }
  }
}
</style>