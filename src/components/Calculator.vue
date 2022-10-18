<template>
  <div class="calc full_to_small">
    <div class="calc__header">
      <calc-switch/>
    </div>
    <calculator-panel/>
  </div>
</template>

<script>
import CalculatorPanel from "@/components/CalculatorPanel";
import CalcSwitch from "@/components/UI/CalcSwitch";

export default {
  name: "Calculator",
  components: {
    CalcSwitch,
    CalculatorPanel
  }
}
</script>

<style scoped lang="scss">
@import '@/scss/colors';

.calc {
  width: 600px;
  height: 95vh;
  background: $calc__body_color_light;
  margin: 20px auto;
  border-radius: 20px;

  display: flex;
  flex-direction: column;

  animation-name: calc_small_to_full;
  animation-duration: 0.2s;
  animation-timing-function: cubic-bezier(.3,.53,.35,1);
}

.calc__header {
  width: 100%;
  height: 45px;
  background: $switch_color_light;
  border-radius: 20px 20px 0 0;

  display: flex;
  justify-content: center;

  animation-name: calc__header_small_to_full;
  animation-duration: 0.2s;
  animation-timing-function: cubic-bezier(.3,.53,.35,1);
}

@media (max-width: 600px) {
  .calc {
    margin: 0;
    border-radius: 0;
    height: 100vh;

    animation-name: calc_full_to_small;
  }

  .calc__header {
    border-radius: 0;

    animation-name: calc__header_full_to_small;
  }
}

@keyframes calc_full_to_small {
  from {
    margin: 20px auto;
    border-radius: 20px;
    height: 95vh;
  }
  to {
    margin: 0;
    border-radius: 0;
    height: 100vh;
  }
}

@keyframes calc_small_to_full {
  from {
    margin: 0;
    border-radius: 0;
    height: 100vh;
  }
  to {
    margin: 20px auto;
    border-radius: 20px;
    height: 95vh;
  }
}

@keyframes calc__header_full_to_small {
  from {
    border-radius: 20px 20px 0 0;
  }
  to {
    border-radius: 0;
  }
}

@keyframes calc__header_small_to_full {
  from {
    border-radius: 0;
  }
  to {
    border-radius: 20px 20px 0 0;
  }
}

</style>