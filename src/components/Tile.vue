<script setup lang="ts">
defineProps<{ title: string, text: string }>()
</script>

<template>
  <div>
    <div class="tile-title">{{ title }}</div>
    <div class="tile-text">{{ text }}</div>
  </div>
</template>

<style scoped>
.tile-title {
  font-weight: 600;
  font-size: 12px;

}

.tile-text {
  font-size: 10px;
  line-height: 16px;
}
</style>
