<script setup lang="ts">
const props = defineProps<{
    isOpen: boolean
}>()
</script>

<template>
  <div class="flyout" :class="{ isOpen }">
    <slot />
  </div>
</template>

<style scoped>
.flyout {
  position: fixed;
  top: 56px;
  right: 0;
  width: 20rem;
  height: 100%;
  background-color: #ffffff7e;
  box-shadow: 10px 10px 0 rgba(255, 255, 255, 1);
  z-index: 1000;
  transform: translate(90%);
  transition: transform 0.3s ease;
}
.flyout:hover,
.flyout.isOpen {
  transform: translateX(0);
}
</style>
