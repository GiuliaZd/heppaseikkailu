<template>
  <div>
    <!-- eslint-disable-next-line vue/require-v-for-key -->
    <div v-for="race in races">
      <h2>{{ race.nimi }}</h2>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import KisaMalli from '../models/KisaMalli.ts';

export default defineComponent({
  name: 'Kisat',
  setup() {
    const races = ref<Array<KisaMalli>>([{ name: 'Vermo' }, { name: 'Killeri' }]);
    return { races };
  }
});
</script>

<style></style>
