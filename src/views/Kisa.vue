<template>
  <div>
    <h2>{{ raceMalli.name }}</h2>
    <!-- <p>{{ alkuAika }}</p> -->
    <ul>
      <li v-for="poni of raceMalli.ponit" :key="poni.id">{{ poni.name }}</li>
    </ul>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType, computed } from 'vue';
import { KisaMalli } from '@/models/KisaMalli';
//import { Alkuun } from '@/utils/Alkuun';//

export default defineComponent({
  name: 'Kisa',

  props: {
    raceMalli: {
      type: Object as PropType<KisaMalli>,
      required: true
    }
  },
  //
  setup(props) {
    const alkuAika = computed(() => Alkuun(props.kisaMalli.startInstant));
    return { alkuAika };
  }
  //
});
</script>
<style></style>
