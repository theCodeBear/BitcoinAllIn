<template>
  <Header @change-content="changeContent($event)" />
  <MainContent :topic="topic" />
</template>


<script>
import Header from './Header.vue';
import MainContent from './MainContent.vue';

export default {
  components: {
    Header,
    MainContent
  },
  data() {
    return {
      topic: 'Home'
    }
  },
  methods: {
    changeContent(payload) {
      this.topic = payload
    }
  }
}
</script>


<style>
</style>
