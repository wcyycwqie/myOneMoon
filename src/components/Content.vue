<template>
  <div class="Content">
    <div>
      <div class="container">
        <div class="row contentBlock contentBg" style="">
          <div class="content-title">
            <h2><b>Welcome</b></h2>
            <p>Here, you will find somethings which are fun and interesting</p>
            <p>I hope you will enjoy it, have fun!</p>
          </div>
        </div>
        <div class="row veidoArea">
          <div class="col-xs-12 col-sm-12 col-md-12">
            <video src="//player.bilibili.com/player.html?aid=85576992&cid=146361395&page=1" width="100%" height="">
              您的浏览器不支持Video标签。
            </video>
            <iframe src="//player.bilibili.com/player.html?aid=85576992&cid=146361395&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" style="width:100%;height:760px;"> </iframe>
            <!-- <video src="blob:https://www.bilibili.com/7ef8a828-fcd7-4539-99d2-54264dcb69e5" width="100%" height="">
              <source src="blob:https://www.bilibili.com/7ef8a828-fcd7-4539-99d2-54264dcb69e5" type="video/mp4">
              <source src="blob:https://www.bilibili.com/7ef8a828-fcd7-4539-99d2-54264dcb69e5" type="video/webm">
              您的浏览器不支持Video标签。
            </video> -->
          </div>
        </div>
        <div class="row contentBlock contentBgTwo">
          <div class="col-xs-12 col-sm-12 col-md-4">
            <div class="smallBox">
              <a href="/#"
                ><img
                  src="/static/images/flowers/23.png"
                  alt=""
                  height="270px"
                  width="340px"
              /></a>
              <span class="smallBox-tips">
                Here, you will find somethings which are fun and
                interestingHere, you will find somethings which are fun and
                interestingHere, you will find somethings which are fun and
                interesting
              </span>
            </div>
          </div>
          <div class="col-xs-12 col-sm-6 col-md-4">
            <div class="smallBox">
              <a href="/#"
                ><img
                  src="/static/images/flowers/25.png"
                  alt=""
                  height="270px"
                  width="340px"
              /></a>
              <span class="smallBox-tips">news</span>
            </div>
          </div>
          <div class="col-xs-12 col-sm-6 col-md-4">
            <div class="smallBox">
              <a href="/#"
                ><img
                  src="/static/images/flowers/22.png"
                  alt=""
                  height="270px"
                  width="340px"
              /></a>
              <span class="smallBox-tips">news</span>
            </div>
          </div>
        </div>
        <div class="row favorArea">
          <div class="page-header">
            <h1>My Favor <small></small></h1>
          </div>
          <div class="col-xs-12 col-sm-6 col-md-6">
            <span>
              <div>
                <img src="/static/images/flowers/12.png" alt="" />
              </div>
              <div></div>
            </span>
          </div>
          <div class="col-xs-12 col-sm-6 col-md-6">
            <span>
              <div>
                <img src="/static/images/flowers/16.png" alt="" />
              </div>
              <div></div>
            </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Content',
  data () {
    return {

    }
  },
  mounted () {

  }
}
</script>
<style lang="less" scoped>
.favorArea {
  img {
    width: 100%;
    height: 380px;
  }
}
</style>
<style>
* {
  margin: 0;
  padding: 0;
}
body,
h1,
h2,
h3,
h4,
h5,
h6,
p,
b {
  color: #fff;
}
.content {
  color: #fff;
}
.contentBlock {
  margin: 50px 0;
  /*padding: 30px 0;*/
  width: 100%;
  height: 450px;
  text-align: center;
  /*box-sizing: border-box;*/
}
.contentBlock p {
  color: #fff;
}
.contentBg {
  background: #66ccff33;
}
.contentBgTwo {
  background: #ffffff99;
}
.content-title {
  position: relative;
  top: 50%;
  /*top:calc(50% - 66px);*/
  font-family: 'Microsoft Yahei';
  font-size: 28px;
  font-weight: bold;
  vertical-align: middle;
  transform: translateY(-50%);
  -webkit-transform: translateY(-50%);
  /*color: #EE5500AA;*/
}
.smallBox {
  margin: 30px 0;
}
.smallBox .smallBox-tips {
  margin-top: 15px;
  display: block;
  height: 120px;
  line-height: 24px;
  overflow: hidden;
}
</style>
