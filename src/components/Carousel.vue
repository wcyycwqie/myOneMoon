<template>
  <div class="Carousel">
    <div class="container">
      <div class="row topTitle">
        <h1 @click="imgRandom()">{{ Carousel }}</h1>
      </div>
      <!-- 轮播图 -->
      <div class="row">
        <div id="carousel-main" class="carousel slide" data-ride="carousel">
          <!-- Indicators -->
          <ol class="carousel-indicators">
            <li
              data-target="#carousel-main"
              data-slide-to="0"
              class="active"
            ></li>
            <li data-target="#carousel-main" data-slide-to="1"></li>
            <li data-target="#carousel-main" data-slide-to="2"></li>
            <li data-target="#carousel-main" data-slide-to="3"></li>
            <li data-target="#carousel-main" data-slide-to="4"></li>
          </ol>

          <!-- Wrapper for slides -->
          <div class="carousel-inner" role="listbox">
            <!-- <div class="item">
              <img v-bind:src="imgSrc" alt="pic" />
              <div class="carousel-caption">
                <h2>hello</h2>
              </div>
            </div> -->
            <!-- 循环遍历轮播图的图片元素 -->
            <div
              class="item"
              v-for="(ele, i) in imgList"
              :key="i"
              :class="{ active: i == 0 }"
            >
              <!-- <img v-bind:src="ele.src" alt="pic" /> -->
              <img v-bind:src="ele.src" alt="pic" />
              <div class="carousel-caption">{{ i + 1 }} {{ ele.caption }}</div>
            </div>
          </div>

          <!-- Controls -->
          <a
            class="left carousel-control"
            href="#carousel-main"
            role="button"
            data-slide="prev"
          >
            <span
              class="glyphicon glyphicon-chevron-left"
              aria-hidden="true"
            ></span>
            <span class="sr-only">Previous</span>
          </a>
          <a
            class="right carousel-control"
            href="#carousel-main"
            role="button"
            data-slide="next"
          >
            <span
              class="glyphicon glyphicon-chevron-right"
              aria-hidden="true"
            ></span>
            <span class="sr-only">Next</span>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import $ from 'jquery'

export default {
  name: 'Carousel',
  props: ['Carousel'],
  data () {
    return {
      num: 1,
      imgList: [],
      rdNum: 888,
      aFlag: true
    }
  },
  mounted () {
    console.log('start')
    console.log('*********************')
    console.log(this.Carousel)

    $('#carousel-main').carousel({
      interval: 5000
    })
    this.imgRandom()
  },
  computed: {
  },
  methods: {
    imgRandom () {
      let imgSrc = '../../static/images/flowers/'
      let imgNum = [1, 2, 3, 4, 5]
      let imgArrLen = 5
      let imgMax = (this.Carousel === 'Game' && 12) || 52
      imgSrc = (this.Carousel === 'Game' && '../../static/images/dota2/carousel/') || '../../static/images/flowers/'
      // 图片随机函数
      let randomNum = (n, max) => {
        let arr = []
        let tempS
        for (let i = 0; ; i++) {
          arr.push(parseInt(Math.random() * max) + 1)
          tempS = new Set(arr)
          if (tempS.size >= n || i > 999) {
            arr = Array(...tempS)
            console.log(arr)
            return arr
          }
        }
      }
      imgNum = randomNum(imgArrLen, imgMax)
      this.imgList = [{
        src: imgSrc + imgNum[0] + '.png',
        caption: ''
      },
      {
        src: imgSrc + imgNum[1] + '.png',
        caption: ''
      },
      {
        src: imgSrc + imgNum[2] + '.png',
        caption: ''
      },
      {
        src: imgSrc + imgNum[3] + '.png',
        caption: ''
      },
      {
        src: imgSrc + imgNum[4] + '.png',
        caption: ''
      }
      ]
    }

  }
}
</script>
<style>
.topTitle {
  margin: 5px 0;
  text-align: center;
}
.topTitle h2 .label {
  font-weight: bold;
  background-color: #b51574;
}
.itemChange {
  margin: 20px 0;
}
#itemChangeOne .itemChange-img {
  width: 100%;
}
.icTwo-imgBg {
  background: url('../../static/images/flowers/28.png');
  background-size: cover;
  background-repeat: no-repeat;
}
</style>
