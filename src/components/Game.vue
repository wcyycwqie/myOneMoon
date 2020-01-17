<template>
  <div class="Game">
    <div>
      <myCarousel Carousel="Game"></myCarousel>
    </div>
    <div style="text-align: center;">
      <h1 style="text-align: center;">game?</h1>
    </div>
    <div class="layui-container">
      <div>
        <button
          type="button"
          class="btn btn-default"
          data-toggle="tooltip"
          data-placement="left"
          title="Tooltip on left"
          @click="getInfo"
        >
          GetInfo
        </button>
      </div>
      <ul class="list-group">
        <li
          class="list-group-item"
          v-for="item in heroinfos"
          :key="item.id"
        >
        {{item.name}}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import myCarousel from './Carousel'
import $ from 'jquery'

export default {
  name: 'Game',
  components: {
    myCarousel
  },
  data () {
    return {
      num: '1',
      heroinfos: []
    }
  },
  mounted () {
    console.log('Game Start')
    $('[data-toggle="tooltip"]').tooltip()
  },
  methods: {
    getInfo () {
      console.log('获取信息')
      // console.log(this.$axios)
      this.$axios({
        'method': 'get',
        'url': ' http://localhost:3888/info'
      }).then(res => {
        console.log(res)
        this.heroinfos = res.data
      })
    }
  }
}
</script>
