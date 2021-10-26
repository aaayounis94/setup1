<template>
  <div class="item">
    <h2>{{ item }}</h2>
    <img :src="url" :alt="item" width="235" height="350" />
    <div class="quantity">
      <button class="dec" @click="counter > 0 ? counter-- : 0"></button>
      <span class="quant-text">Quantity: {{ counter }}</span>
      <button class="inc" @click="counter++"></button>
    </div>
    <button class="submit">submit</button>
  </div>
</template>

<script>
export default {
  props: ["item", "url"],
  data() {
    return {
      counter: 0,
    };
  },
};
</script>
