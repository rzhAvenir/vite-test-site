<script setup lang="ts">
import { ref } from 'vue';
import XhSwitch from './components/Switch/Switch.vue';
import DarkIcon from './assets/svg/dark.svg?component';
import DayIcon from './assets/svg/day.svg?component';

const data = ref(true);
const test = () => {
  data.value = !data.value;
};
</script>

<template>
  <div>
    <XhSwitch 
      v-model="data" 
      @change="test" 
      :active-icon="DayIcon" 
      :inactive-icon="DarkIcon"
      inlinePrompt>
    </XhSwitch>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
