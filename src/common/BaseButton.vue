<script setup>
  import { defineProps } from "vue";
  const props = defineProps({
    option: {
      type: String,
      required: true,
      default: "X",
    },
  });
</script>

<template>
  <button class="no-select">{{ props.option }}</button>
</template>

<style lang="scss" scoped>
  button {
    background-color: $clr-neutral-300;
    color: $clr-neutral-200;
    border-radius: 100%;

    width: 2.5rem;
    height: 2.5rem;
    padding-top: 0.25rem;

    font-size: $fs-button;
    cursor: pointer;
  }

  @media (min-width: 350px) {
    button {
      width: 3rem;
      height: 3rem;
      padding-top: 0.3rem;
    }
  }

  button:hover {
    background-color: $clr-primary-400;
    color: $clr-neutral-100;
  }

  button:focus {
    background-color: $clr-neutral-200;
    color: $clr-neutral-100;
  }

  button:focus-visible {
    background-color: $clr-neutral-200;
    color: $clr-neutral-100;
  }

  button:focus-within {
    background-color: $clr-neutral-200;
    color: $clr-neutral-100;
  }
</style>
