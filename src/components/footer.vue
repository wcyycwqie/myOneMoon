<template>
  <div class="Footer">
    <div class="footer-copy container-fluid">
      <div>
        <h1>Happy new year <i>2020 !</i></h1>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data () {
    return {

    }
  }
}
</script>

<style lang="less" scoped>
.footer-copy  {
  margin: 100px 0 30px;
  text-align: center;
  color: red;
  h1 {
    color: #337ab7;
  }
  i {
    color: #F00;
  }
}
</style>
