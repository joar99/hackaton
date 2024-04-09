<template>
  <div class="hello">
    <button @click="increment">Click Me</button>
    <h1>{{number}}</h1>
  </div>
</template>

<script setup>
import {ref} from "vue";
const number = ref(0)

const increment = () => {
  number.value += 1
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
