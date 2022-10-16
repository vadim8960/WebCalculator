<template>
  <div class="main">
    <calculator/>
  </div>
</template>

<script>
import Calculator from "@/components/Calculator";
export default {
  name: 'App',
  components: {
    Calculator
  }
}
</script>

<style lang="scss">
@import "@/scss/colors";
body {
  padding: 0;
  margin: 0;
}

.main {
  display: flex;
  justify-content: center;
  height: 100vh;
  background: $main_color_light;
}
</style>
