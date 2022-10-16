<template>
  <div class="calc__keyboard">
    <calc-button
        v-for="btn_data in btns_data"
        :style="btn_data.style"
        :key="btn_data.name"
        :name="btn_data.name"
    />
  </div>
</template>

<script>
export default {
  name: "CalculatorKeyboard",
  props: {
    btns_data: {
      type: Array,
      default: []
    }
  }
}
</script>

<style scoped>
.calc__keyboard {
  height: 250px;
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-template-rows: repeat(5, 1fr);
  grid-row-gap: 5px;
  grid-column-gap: 5px;
  padding: 15px;
}
</style>