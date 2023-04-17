<script setup></script>

<template>
  <div class="container">
    <slot></slot>
  </div>
</template>

<style lang="scss" scoped>
  .container {
    border-radius: 1rem;
    padding: 1.5rem 1.7rem;
    margin: 1rem;
    background-color: hsla(213, 19%, 18%, 0.65);
  }

  @media (min-width: 450px) {
    .container {
      padding: 2rem;
    }
  }
</style>
