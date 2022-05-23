<template>
  <div class="hello">
    <h1 class="highlight">{{ textmsg }}</h1>
    <img src="../../assets/img/download.jpeg" @click="countNumber" />
    <p>{{counter}}</p>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "TestWorld",
  components: {},
  props: {
    msg: String
  },
  setup() {
    const textmsg = "I am Test World Component";
    const selected = ref(new Date());
    const counter = ref(0);
    const countNumber = (): void => {
      counter.value = counter.value + 1;
    }
    return {
      textmsg,
      selected,
      counter,
      countNumber,
    };
  }
});
</script>

<style lang="css" scoped>
@import "./testworld.css";
</style>
