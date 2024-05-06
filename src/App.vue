<script setup lang="ts">
const buttonText = 'Spara';
const clickable = true;
const myClass = "testing";
const showP = true;
const numbers = [1,2,3,3,4,5];

function yeah (){
  console.log('yeah');
}
</script>

<template>
  <div class="wrapper">
    //v-bind and v-on
    <button :disabled="!clickable" :class="myClass" @click="yeah">{{ buttonText }}</button>

    //v-if
    <p v-if="showP">This is a paragraph</p>

    <span v-else>hello</span>

    <ul>
      //v-for
      <li v-for="n in numbers">{{ n }}</li>
    </ul>

    </div>
    
</template>

<style scoped>
</style>
