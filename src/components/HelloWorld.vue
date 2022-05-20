<template>
  <div class="hello">
    <button @click="clickFunction">click {{counter}}</button>
  </div>
</template>

<script lang="ts">
import {defineComponent, ref} from 'vue';

export default defineComponent({
  name: 'HelloWorld',
  setup() {
    const counter = ref(0)
    const clickFunction = (): void => {
      counter.value = counter.value + 1;
    }
    return {
      counter,
      clickFunction
    }
  }
});
</script>
