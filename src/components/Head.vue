<template>
  <div class="header">
    <nav class="top-nav bg navbar navbar-default">
      <div id="top-nav" class="container" role="navigation">
        <a href="/" class="top-logo">
          <img src="../../static/images/icon/moon.png" alt="Moon" />
        </a>
        <ul id="top-nav-main" class="top-nav-main nav nav-pills">
          <li
            role="presentation"
            class=""
            v-for="(items, index) in nav"
            :key="index"
            :class="navIndex === index ? 'active' : ''"
          >
            <!-- <router-link :to="{ path: items.path }">{{
              items.title
            }}</router-link> -->
            <a @click="routerLink(index, items.path)">{{ items.title }}</a>
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
    $(this).tab('show')
  })
})

export default {
  name: 'myHeader',
  data () {
    return {
      hello: 'hahaha',
      nav: [
        { title: 'Home', path: '/' },
        { title: 'Game', path: '/game' },
        { title: 'Animation', path: '/animation' },
        { title: 'Music', path: '' },
        { title: 'Community', path: '' }
      ],
      navIndex: 0
    }
  },
  mounted () {
    console.log('HEAD')
    this.checkRouterLocal(this.$route.path)
  },
  methods: {
    routerLink (index, path) {
      // 点击哪个路由就赋值给自定义的下标
      this.navIndex = index
      // 路由跳转
      this.$router.push(path)
    },
    checkRouterLocal (path) {
      // 查找当前路由的下标
      this.navIndex = this.nav.findIndex(item => item.path === path)
    }
  },
  watch: {
    '$route' () {
      // 获取当前路径
      let path = this.$route.path
      console.log('------------------------')
      console.log(path)
      // 检索当前路径
      this.checkRouterLocal(path)
    }
  }
}

</script>

<style lang="less">
@import url('../../static/css/myStyle.less');

@navColorOne: #b51574;
.top-nav {
  /* 超小屏幕（手机，小于 768px） */
  /* 没有任何媒体查询相关的代码，因为这在 Bootstrap 中是默认的（还记得 Bootstrap 是移动设备优先的吗？） */
  display: none;

  /* 小屏幕（平板，大于等于 768px） */
  @media (min-width: 768px) {
    display: none;
  }

  /* 中等屏幕（桌面显示器，大于等于 992px） */
  @media (min-width: 992px) {
    display: block;
  }

  /* 大屏幕（大桌面显示器，大于等于 1200px） */
  @media (min-width: 1200px) {
    display: block;
  }
}
#top-nav {
  position: relative;
  #top-nav-main,
  .top-nav-login {
    > li {
      > a {
        padding: 10px 20px;
        line-height: 40px;
        transition: all 0.3s;
        cursor: pointer;
      }
      &.active > a,
      > a.router-link-exact-active,
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
