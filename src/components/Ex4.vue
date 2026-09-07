<script setup>
import { ref } from 'vue'

// Part 1
const isBlue = ref(true)

// Part 2
const activeColor = ref('blue')

function changeColor() {
  isBlue.value = !isBlue.value
}

function changeTextColor() {
  activeColor.value = activeColor.value === 'blue' ? 'red' : 'blue'
}
</script>

<template>
  <div id="part1">
    <div id="demo" :class="{ blue: isBlue, red: !isBlue }">
      div ID : demo
    </div>
    <button type="button" @click="changeColor">
      Change Color
    </button>
  </div>

  <br>

  <div id="part2">
    <div id="demo2" :style="{ color: activeColor }">
      div ID : demo2
    </div>
    <button type="button" @click="changeTextColor">
      Change Text Color
    </button>
  </div>
</template>

<style scoped>
.red {
  background-color: red;
  color: white;
}

.blue {
  background-color: blue;
  color: white;
}
</style>