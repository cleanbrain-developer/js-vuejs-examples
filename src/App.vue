<!--
Modal component with customizable slots and CSS transitions.
-->

<script setup>
import DemoModal from './DemoModal.vue'
import { ref } from 'vue'

const showModal = ref(false)
</script>

<template>
  <button id="show-modal" @click="showModal = true">Show Modal</button>

  <Teleport to="body">
    <!-- use the modal component, pass in the prop -->
    <DemoModal :show="showModal" @close="showModal = false">
      <template #header>
        <h3>custom header</h3>
      </template>
    </DemoModal>
  </Teleport>
</template>