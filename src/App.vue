<script setup lang="ts">
import { onMounted, ref } from 'vue';

const buttonText = 'Spara';
const clickable = true;
const myClass = "testing";
let showP = ref(true);
const numbers = [1, 2, 3, 3, 4, 5];
const names = ['John', 'Doe', 'Jane', 'Dee'];

onMounted(() => {
  console.log('mounted');
});

function yeah() {
  console.log('yeah');
  showP.value = !showP.value;
}
</script>

<template>
  <div class="wrapper">
    <!-- v-bind and v-on -->
    <button :disabled="!clickable" :class="myClass" @click="yeah">{{ buttonText }}</button>

    <!-- v-if -->
    <p v-if="showP">This is a paragraph</p>

    <span v-else>hello</span>

    <ul>
      <!-- v-for -->
      <li v-for="n in numbers">{{ n }}</li>
    </ul>

    <div v-for="n in names">
      <h1>{{ n }}</h1>
    </div>

  </div>

</template>

<style scoped></style>
