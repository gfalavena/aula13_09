<template>
  <NavPage></NavPage>
  <ContentPage></ContentPage>
  <FooterPage></FooterPage>
  <LoopComponent></LoopComponent>
  <ObjectComponent></ObjectComponent>
</template>

<script>
import NavPage from './components/default/NavPage.vue';
import ContentPage from './components/default/ContentPage.vue';
import FooterPage from './components/default/FooterPage.vue';
import LoopComponent from './components/default/LoopComponent.vue';
import ObjectComponent from './components/default/ObjectComponent.vue';

export default {
  name: 'App',
  components: {
    NavPage, ContentPage, FooterPage, LoopComponent, ObjectComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #4f8dcb;
  margin-top: 60px;
}
</style>
