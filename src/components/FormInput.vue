<script setup lang="ts">
import { ref } from 'vue'

interface FormInputProps {
  type: 'text' | 'postal' | 'phone' | 'email';
  placeholder: string;
}

const props = defineProps<FormInputProps>()
const value = ref('')
</script>

<template>

  <input
    :id="`input-${props.type}`"
    :type="type"
    v-model="value"
    :placeholder="placeholder"

  />

</template>

<style scoped>
@import '../assets/base.css';

input {
  border: 1px solid var(--tertiary);
  border-radius: 10px;
  line-height: 3rem;
}

input:focus-visible::placeholder {
  color: black;
}


</style>
