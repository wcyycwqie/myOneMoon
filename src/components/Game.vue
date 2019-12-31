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
        >
          Tooltip on left
        </button>
      </div>
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
      num: '1'
    }
  },
  mounted () {
    console.log('Game Start')
    $('[data-toggle="tooltip"]').tooltip()
  },
  methods: {
  }
}
</script>
