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
            <video width="100%" height="" controls autoplay loop>
              <source src="../../static/video/home2.webm" type="video/webm" />
              <source src="../../static/video/home2.mp4" type="video/mp4" />
              您的浏览器不支持Video标签。
            </video>
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
@RateG: 0.618;

.Gwh(@width) {
  width: @width;
  height: @width * @rateG;
}

.contentBgTwo {
  .smallBox {
    > a {
      img {
        display: block;
        width: 100%;
        height: 350px * @RateG;
      }
    }
  }
}
.favorArea {
  img {
    margin: 15px 0;
    width: 100%;
    height: 555px * @RateG;
  }
  .page-header {
    h1 {
      margin-left: 15px;
    }
  }
}
</style>

<style lang="less" scoped>
/* 移动端适配 媒体查询*/
@RateG: 0.618;

/* 超小屏幕（手机，小于 768px） */
@media (min-width: 320px) {
  .favorArea {
    img {
      height: 290px * @RateG;
    }
  }
}
/* 小屏幕（平板，大于等于 768px） */
@media (min-width: 768px) {
  .favorArea {
    img {
      height: 555px * @RateG;
    }
  }
}

/* 中等屏幕（桌面显示器，大于等于 992px） */
@media (min-width: 992px) {
}

/* 大屏幕（大桌面显示器，大于等于 1200px） */
@media (min-width: 1200px) {
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
  width: 100%;
  height: 450px;
  text-align: center;
}
.contentBlock p {
  color: #fff;
}
.contentBg {
  background: #66ccff33;
}
.contentBgTwo {
  background: #ffffff99;
  height: auto;
}
.content-title {
  position: relative;
  top: 50%;
  font-family: 'Microsoft Yahei';
  font-size: 24px;
  font-weight: bold;
  vertical-align: middle;
  transform: translateY(-50%);
  -webkit-transform: translateY(-50%);
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
