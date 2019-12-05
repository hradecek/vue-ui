<template>
  <div id="app" class="flex flex-col h-screen bg-gray-100">
    <TopBar />
    <MainContent />
  </div>
</template>

<script>
import TopBar from './components/TopBar.vue';
import MainContent from './components/MainContent.vue';

export default {
  name: 'app',
  components: {
    TopBar,
    MainContent,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
