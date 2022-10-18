<template>
  <div class="switch">
    <div class="switch_button left_switch">Светлая тема</div>
    <div class="switch_button right_switch">Темная тема</div>
  </div>
</template>

<script>
export default {
  name: "CalcSwitch"
}
</script>

<style scoped lang="scss">
@import "@/scss/colors";

.switch {
  background: white;
  padding: 0 20px;
  border-radius: 20px;

  display: flex;
  align-items: center;
  justify-content: space-between;
}

.switch_button {
  text-align: center;
  display: flex;
  align-items: center;

  background: grey;
}

.left_switch {
  margin-right: 5px;
  height: 100%;

  animation-name: active_button;
  animation-duration: 1s;
  animation-iteration-count: infinite;
}

.right_switch {
  margin-left: 5px;
  height: 100%;

  animation-name: active_button_2;
  animation-duration: 1s;
  animation-iteration-count: infinite;
}

@keyframes active_button {
  from {
    background: grey;
  }
  50% {
    background: white;
  }
  to {
    background: grey;
  }
}

@keyframes active_button_2 {
  from {
    background: white;
  }
  50% {
    background: grey;
  }
  to {
    background: white;
  }
}
</style>