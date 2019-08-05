<template>

  <div id="app">
    <img style="width: 200px; height: 150px;" src="./assets/ViollierLogo.svg">

    <HelloWorld msg="Welcome v-team"/>
    <konva></konva>
    <story></story>

  </div>

</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from './components/HelloWorld.vue';
import konva from './components/konva.vue';
import story from './components/story.vue';


@Component({
  components: {
    konva,
    HelloWorld,
    story,
  },
})
export default class App extends Vue {}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0;

}
</style>
