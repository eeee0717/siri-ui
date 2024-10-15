<script setup lang="ts">
import { ref } from 'vue';
import GradientCanvas from './components/GradientCanvas.vue'
const isAnimating = ref(false)
const isStopped = ref(false)
function startClick() {
  isAnimating.value = true
  isStopped.value = false
}
function stopClick() {
  isStopped.value = true
  isAnimating.value = false
}
</script>

<template>
  <main>
    <div>
      <GradientCanvas :start="isAnimating" :stop="isStopped">
      <h1>
        Siri UI
      </h1>
    </GradientCanvas>
    </div>
    <div>
      <button @click="startClick">
        start
      </button>
      <button @click = "stopClick">
        stop
      </button>
    </div>
  </main>
</template>


