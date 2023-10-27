<template>
  <p class="mt-2">Message from parent: {{ message }}</p>
  <button
      @click="sendMessageClick"
      type="button"
      class="rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600 mt-6"
  >Click me to emit to parent component</button>
</template>

<script setup>
import { defineProps, defineEmits } from 'vue';

const { message } = defineProps(['message']);
const emit = defineEmits();

function sendMessageClick() {
  emit('messageClicked');
}
</script>