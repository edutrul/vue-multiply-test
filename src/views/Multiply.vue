<template>
  <div class="multiply">
    <h1>This is multiply</h1>
  </div>
  Value A
  <input name="value_a" placeholder="6" type="text" v-model="value_a"><br>
  Value B
  <input name="value_b" placeholder="5" type="text" v-model="value_b"><br>
  <button @click="multiply" type="submit" class="btn btn-primary">Multiply</button>
  <p v-if = "result" class="multiply--result">The result is something {{ result }}</p>
</template>
<script>
  export default {
    name: 'Multiply.vue',
    data () {
      return {
        value_a: null,
        value_b: null,
        result: null,
      }
    },
    methods: {
      multiply() {
        this.result = this.value_a * this.value_b;
      }
    }
  }
</script>
