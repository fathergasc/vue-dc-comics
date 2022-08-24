<template>
  <div id="app">
    <MyHeader/> 
    <MyMain/>
    <MyFooterTop/>
    <MyFooterBot/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'
import MyFooterTop from './components/MyFooterTop.vue'
import MyFooterBot from './components/MyFooterBot.vue'


export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain,
    MyFooterTop,
    MyFooterBot,
  }
}
</script>


<style lang="scss">

  @import '~bootstrap/scss/bootstrap.scss';
  @import './styles/vars.scss';
  @import './styles/general.scss';
  @import './styles/typo.scss';

  ul {
    list-style: none;
  }
  a {
    text-decoration: none;
  }



</style>
