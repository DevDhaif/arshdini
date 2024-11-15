<template>
    <input :placeholder="placeholder" :value="modelValue" @input="updateValue" />
  </template>
  
  <script>
  export default {
    props: ['modelValue', 'placeholder'],
    methods: {
      updateValue(event) {
        this.$emit('update:modelValue', event.target.value);
      }
    }
  }
  </script>