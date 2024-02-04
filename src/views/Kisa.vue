<template>
  <div>
    <h2>{{ raceMalli.name }}</h2>
    <ul>
      <li v-for="poni of raceMalli.ponit" :key="poni.id">{{ poni.name }}</li>
    </ul>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue';
import { KisaMalli } from '@/models/KisaMalli';

export default defineComponent({
  name: 'Kisa',

  props: {
    raceMalli: {
      type: Object as PropType<KisaMalli>,
      required: true
    }
  }
});
</script>
<style></style>
