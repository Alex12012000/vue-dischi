<template>
  <div id="app">
    <PageHeader/>
    <main>
      <MainContent/>
      <MusicCard/>
    </main>

  </div>
</template>

<script>
// import PageContent from './components/PageContent.vue'
import PageHeader from './components/PageHeader.vue';
import MainContent from './components/MainContent.vue';
import MusicCard from './components/MusicCard.vue';

export default {
  name: 'App',
  components: {
    PageHeader,
    MainContent,
    MusicCard,
  }
}
</script>

<style lang="scss">
@import './style/common.scss'
</style>
