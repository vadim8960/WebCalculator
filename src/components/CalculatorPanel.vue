<template>
  <div class="calc__panel">
    <div class="calc__input_history">история</div>
    <div class="calc__input">входные данные</div>
    <calculator-keyboard :btns_data="btns_data"/>
  </div>
</template>

<script>
import CalculatorKeyboard from "@/components/CalculatorKeyboard";

export default {
  name: "CalculatorPanel",
  components: {CalculatorKeyboard},
  data() {
    return {
      btns_data: [
        {name: 'Del', style: ''},
        {name: '(', style: ''},
        {name: ')', style: ''},
        {name: 'mod', style: ''},
        {name: 'pi', style: ''},
        {name: '7', style: ''},
        {name: '8', style: ''},
        {name: '9', style: ''},
        {name: '/', style: ''},
        {name: 'sqrt', style: ''},
        {name: '4', style: ''},
        {name: '5', style: ''},
        {name: '6', style: ''},
        {name: '*', style: ''},
        {name: 'x^2', style: ''},
        {name: '1', style: ''},
        {name: '2', style: ''},
        {name: '3', style: ''},
        {name: '-', style: ''},
        {name: '=', style: 'grid-area: 4 / 5 / 6 / 5;'},
        {name: '0', style: ''},
        {name: ',', style: ''},
        {name: '%', style: ''},
        {name: '+', style: ''}
      ]
    }
  }
}
</script>

<style scoped>
.calc__panel {
  height: 100%;

  display: flex;
  flex-direction: column;
  justify-content: end;
}

.calc__input_history {
  height: auto;
}

.calc__input {
  height: 10%;
}
</style>