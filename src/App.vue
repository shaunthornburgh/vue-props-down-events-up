<template>
  <div class="mx-auto max-w-7xl sm:px-6 lg:px-8">
    <h1 class="text-base font-semibold leading-7 text-gray-900 pt-8">Vue 3 - Props Down, Events Up Demo</h1>
    <ChildComponent :message="parentMessage" @messageClicked="handleMessageClick" />
  </div>
</template>

<script setup>
import { ref } from 'vue';
import ChildComponent from './components/ChildComponent.vue';
const parentMessage = ref("Hello from Parent!");
function handleMessageClick() {
  alert('Message from child was clicked!');
}
</script>