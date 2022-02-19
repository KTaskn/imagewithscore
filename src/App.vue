<template>
  <v-app>
    <v-main>
      <s-scroller :items="items" />
    </v-main>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';
import SScroller from './components/SScroller.vue';

export default Vue.extend({
  name: 'App',
  components: {
    SScroller
  },
  data: () => ({
    items: Array.from({length: 100}, (_, i) => ({
        id: i,
        image: `https://picsum.photos/id/${i}/${100}/${100}`,
        score: Math.random(),
    }))
  }),
});
</script>
