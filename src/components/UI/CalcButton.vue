<template>
  <button class="calc__btn">
    {{ name }}
  </button>
</template>

<script>
export default {
  name: "CalcButton",
  props: {
    color: {
      type: String,
      default: 'grey'
    },
    name: {
      type: String,
      default: ''
    }
  }
}
</script>

<style scoped lang="scss">
@import '@/scss/colors';

.calc__btn {
  border-radius: 10px;
  background: $calc__btn_released_color_light;
  border: 1px solid $calc__btn_border_color_light;

  &:active {
    background: $calc__btn_pressed_color_light;
  }
}
</style>