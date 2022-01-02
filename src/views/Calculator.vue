<template>
  <div class="calculator">
    <h1>This is calculator</h1>
  </div>
  Value A
  <input name="value_a" placeholder="6" type="number" v-model="value_a" @change="calculate" ><br>
  Value B
  <input name="value_b" placeholder="5" type="number" v-model="value_b" @change="calculate" ><br>
  Choose operator to calculate...:
  <select @change="calculate" name="operator" v-model="operator">
    <option selected value="+">+</option>
    <option value="-">-</option>
    <option value="*">*</option>
    <option value="/">/</option>
  </select>
  <p v-if = "result" class="multiply--result">The result is something {{ result }}</p>
</template>
<script>
  export default {
    name: 'Calculator.vue',
    data () {
      return {
        value_a: null,
        value_b: null,
        // Operator can be "+", "-", "/", "*".
        operator: '+',
        result: null,
      }
    },
    methods: {
      calculate() {
        console.log(this.value_a);
        console.log(this.value_b);
        console.log(this.operator);
        switch (this.operator) {
          case '+':
            this.result = this.value_a + this.value_b;
            break;
          case '-':
            this.result = this.value_a - this.value_b;
            break;
          case '/':
            this.result = this.value_a / this.value_b;
            break;
          case '*':
            this.result = this.value_a * this.value_b;
            break;
        }
      }
    }
  }
</script>
