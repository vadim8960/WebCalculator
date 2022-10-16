<template>
  <div class="calc__output">
    <div class="calc__output__content">
      5 + 10 = 15
    </div>
  </div>
</template>

<script>
export default {
  name: "CalcOutput"
}
</script>

<style scoped lang="scss">
@import '@/scss/colors';

.calc__output {
  width: 500px;
  height: 200px;
  display: flex;
  justify-content: right;
  align-items: end;
  background: $calc__output_color_light;
}

.calc__output__content {
  margin: 20px 20px;
}
</style>