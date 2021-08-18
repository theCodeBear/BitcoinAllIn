<template>
  <div style='height: 100vh; display: flex; justify-content: center; align-items: center; flex-direction: column;'>
    <div style='font-size: 32px; margin-bottom: 10px;'>
      <!-- {{ showPage(topic) }} -->
      <Home v-if="topic==='Home'" />
      <WhatsBitcoin v-if="topic==='What is Bitcoin?'" />
      <Charts v-if="topic==='Charts'" />
      <Articles v-if="topic==='Articles'" />
      <History v-if="topic==='History'" />
      <About v-if="topic==='About'" />
    </div>
  </div>
</template>


<script>
import { defineProps } from 'vue'
import Home from './Home.vue';
import WhatsBitcoin from './WhatsBitcoin.vue';
import Charts from './Charts.vue';
import Articles from './Articles.vue';
import History from './History.vue';
import About from './About.vue';

defineProps({
  topic: String
})

export default ({
  components: {
    Home,
    WhatsBitcoin,
    Charts,
    Articles,
    History,
    About
  },
  props: {
    topic: String
  },
  // methods: {
  //   showPage(topic) {
  //     switch (topic) {
  //       case "What is Bitcoin?":
  //         return WhatsBitcoin
  //         // "Charts",
  //         // "Articles",
  //         // "History",
  //         // "About",
  //         // "Bayne's Corner"
  //     }
  //   }
  // }
})
</script>


<style>
</style>