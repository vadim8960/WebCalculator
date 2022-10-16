<template>
  <div class="calc">
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
}

.calc__header {
  width: 100%;
  height: 45px;
  background: $switch_color_light;
  border-radius: 20px 20px 0 0;
  display: flex;
  justify-content: center;
}

@media (max-width: 600px) {
  .calc {
    margin: 0;
    border-radius: 0;
    height: 100vh;

  }

  .calc__header {
    border-radius: 0;
  }
}

</style>