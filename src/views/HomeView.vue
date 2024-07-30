<script setup>
import TheWelcome from '../components/TheWelcome.vue'
import { computed, ref } from 'vue'

// function square(num) {
//   return num * num
// }

/**
 *
 * @param x Single parameter for lambda function
 */
const square = (x) => x * x

/**
 * Adding two numbers
 * Two parameters
 */
const add = (x, y) => x + y

// List of numbers in an array format..
const numbers = ref([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])

/**
 * Computerd property to double the numbers by mapping each number to its double.
 * @returns Array of doubled numbers
 */
const doubledNumbers = computed(() => numbers.value.map((x) => x * 2))

const evenNumbers = computed(() => numbers.value.filter((n) => n % 2 === 0))
</script>

<template>
  <main>
    <TheWelcome />
    <div>
      <br />
      <br />
      <br />
      <h3>Welcome to Lambda functions in VueJS 3</h3>
      <p>Square of 5: {{ square(5) }}</p>
      <p>Add 3 and 4: {{ add(3, 4) }}</p>
      <p>Doubled Numbers: {{ doubledNumbers }}</p>
      <p>Even Numbers: {{ evenNumbers }}</p>
    </div>
  </main>
</template>
