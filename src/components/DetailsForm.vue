<script setup lang="ts">
import FormInput from '@/components/FormInput.vue'
</script>

<template>
  <div class="form-container">
    <div class="d-flex justify-center">
      <h3 class="text-primary">Enter details</h3>
    </div>
    <form class="d-flex flex-column">
      <div class="d-flex flex-row">
        <form-input class="w-50" placeholder="First name" type="text" />
        <form-input class="w-50" placeholder="Last name" type="text" />
      </div>
      <form-input placeholder="Street" type="text" />
      <div class="d-flex flex-row">
        <form-input class="w-50" placeholder="Postal code" type="postal" />
        <form-input class="w-50" placeholder="City" type="text" />
      </div>
      <form-input placeholder="Phone number" type="phone" />
      <form-input placeholder="E-mail" type="email" />
      <input type="button" value="PROCEED TO PAYMENT">
    </form>
    <div class="d-flex justify-center"><img alt="Safety features" src="/src/assets/frame.png" /></div>
  </div>

</template>

<style scoped>
input {
  margin: 0.5rem;
}

input[type='button'] {
  background-color: var(--primary);
  color: white;
  font-weight: 600;
  height: 48px;
  padding: 12px 16px 12px 16px;
  border-radius: 10px;

}

.form-container {
  border-radius: 20px;
  border: 1px solid var(--tertiary);
  padding: 2rem;
}
</style>
