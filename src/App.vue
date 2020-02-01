<template>
  <div id="app">
    <my-header></my-header>
    <transition>
      <router-view name="main"></router-view>
    </transition>
    <!-- <router-view name="main"></router-view> -->
    <myFooter></myFooter>
  </div>
</template>

<script>
import myHeader from './components/Head'
import myContent from './components/Content'
import myFooter from './components/footer'

export default {
  name: 'app',
  components: {
    myHeader,
    myFooter
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
  /*margin-top: 60px;*/
}
body,
div,
span,
a,
p,
ul,
li {
  margin: 0;
  padding: 0;
}
</style>
