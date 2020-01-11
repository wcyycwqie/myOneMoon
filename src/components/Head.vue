<template>
  <div class="header">
    <nav class="top-nav bg navbar navbar-default">
      <div id="top-nav" class="container" role="navigation">
        <a href="/" class="top-logo">
          <img src="../../static/images/icon/moon.png" alt="Moon" />
        </a>
        <ul id="top-nav-main" class="top-nav-main nav nav-pills">
          <li role="presentation" class="active" :title="$route.name">
            <router-link :to="{ name: 'root' }">Home</router-link>
          </li>
          <li role="presentation" class="">
            <router-link :to="{ name: 'myGame' }">Game</router-link>
          </li>
          <li role="presentation" class="">
            <router-link :to="{ name: 'myAnimation' }">Animation</router-link>
          </li>
          <li role="presentation" class="">
            <a href="#">Music</a>
          </li>
          <li role="presentation" class="">
            <a href="#">Other</a>
          </li>
          <li role="presentation" class="">
            <a href="#">Community</a>
          </li>
        </ul>
        <ul class="top-nav-login nav nav-pills">
          <li role="presentation" class="">
            <a href="">
              <span class="icon iconfont">&#xe6b6;</span>
            </a>
          </li>
          <li role="presentation" class="">
            <a href="#"> <span class="icon iconfont">&#xe6af;</span>登录</a>
          </li>
          <li role="presentation" class="">
            <a href="#"> <span class="icon iconfont">&#xe664;</span> 注册</a>
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>

<script>
import $ from 'jquery'
$(function () {
  $('#top-nav-main a, .top-nav-login').click(function (e) {
    console.log($(this))
    e.preventDefault()
    $(this).parent().addClass('active').siblings('li').removeClass('active')
    $(this).tab('show')
  })
})

export default {
  name: 'myHeader',
  data () {
    return {
      hello: 'hahaha'
    }
  },
  mounted () {

  },
  methods: {
    testClick () { }
  },
  watch: {
    '$route' () {
      // 获取当前路径
      let path = this.$route.path
      // 检索当前路径
      console.log('******************************')
      console.log(path)
      // this.checkRouterLocal(path)

    }
  }
}

</script>

<style lang="less">
@import url('../../static/css/myStyle.less');

@navColorOne: #b51574;
#top-nav {
  position: relative;
  #top-nav-main,
  .top-nav-login {
    > li {
      > a {
        padding: 10px 20px;
        line-height: 40px;
        transition: all 0.3s;
      }
      &.active > a,
      > a:hover,
      > a:focus {
        color: #fff;
        background: linear-gradient(30deg, @navColorOne, transparent);
      }
    }
  }
  .top-nav-main {
    margin-left: 100px;
    background: none;
  }
  .top-nav-login {
    li {
      a {
        > .icon {
          margin-right: 10px;
        }
      }
    }
  }
}
</style>

<style>
.header {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 80px;
  /*background: url('../../static/images/flowers/17.png');*/
  background-size: cover;
  text-align: none;
}
/*头部*/
.top-nav {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 999;
  width: 100%;
  height: 60px;
  border: none;
}
.top-logo {
  position: absolute;
  top: 4px;
  left: 25px;
}
#top-img {
  background: url('../../static/images/flowers/2.png') repeat-x;
  background-size: cover;
  height: 240px;
}

.nav-main {
  margin-left: 100px;
  background: none;
}
.bg,
.top-nav {
  background: #a5329b99;
}

.top-nav-login {
  position: absolute;
  top: 0;
  right: 15px;
  background: none;
}

.icon-icon_geren {
  font-size: 32px;
}
.area-one {
  height: 600px;
}
.area-one .layui-tab .layui-tab-title li {
  background: #ea54dd;
}
.area-one .layui-tab .layui-tab-title .layui-this {
  background: #66ccff;
}
.itemChange-img {
  width: 100%;
}
</style>
