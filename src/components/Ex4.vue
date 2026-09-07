<script setup>
import { ref } from 'vue'

// Part 1
const blueBox = ref(true)
const blueBtn = ref(true)

// Part 2
const activeColor = ref('blue')
const redBtn = ref(false)

function changeColor() {
  if (blueBox.value) {
    blueBox.value = false
    blueBtn.value = false
  } else {
    blueBox.value = true
    blueBtn.value = true
  }
}

function changeTextColor() {
  if (activeColor.value === 'blue') {
    activeColor.value = 'red'
    redBtn.value = true
  } else {
    activeColor.value = 'blue'
    redBtn.value = false
  }
}
</script>

<template>
  <div id="part1">
    <div :class="blueBox ? 'blueBox' : 'redBox'">
      div ID : demo
    </div>
    <button type="button" @click="changeColor">
      Change Color
    </button>
  </div>

  <br>

  <!-- Part 2: Style Binding (Text Color Only) -->
  <div id="part2">
    <div id="demo2" :style="{ color: activeColor }">
      div ID : demo2
    </div>
    <!-- Remove the :class binding so it stays a default grey button -->
    <button type="button" v-on:click="changeTextColor">
      Change Text Color
    </button>
  </div>
</template>

<style scoped>
.redBox {
  background-color: red;
  color: white;
}

.blueBox {
  background-color: blue;
  color: white;
}

.btn-primary {
  background-color: blue;
  color: white;
}

.btn-danger {
  background-color: red;
  color: white;
}
</style>