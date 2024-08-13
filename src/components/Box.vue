<script setup lang="ts">
defineProps<{
  texts: string[],
  img: { fileName: string, alt: string },
  isReversed?: boolean
}>()


</script>

<template>
  <div class="d-flex" :class="[isReversed ? 'flex-row-reverse' : 'flex-row']">
    <img :alt="img.alt" :src="`/src/assets/${img.fileName}`" />
    <div class="d-flex flex-column justify-center">
      <slot></slot>
      <p v-for="text in texts" :key="text">{{ text }}</p>
    </div>
  </div>
</template>

<style scoped>
img {
  aspect-ratio: 1;
  width: 50%;
  margin: 0.5rem
}

</style>
