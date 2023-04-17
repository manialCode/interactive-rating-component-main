<script setup></script>

<template>
  <input
    type="submit"
    value="submit"
    class="uppercase bg-primary-400 text-neutral-100 no-select" />
</template>

<style lang="scss" scoped>
  input {
    width: 100%;
    font-size: $fs-500;
    font-weight: $fw-bold;
    border-radius: 2rem;
    padding: 0.8rem;
    padding-bottom: 0.45rem;
    cursor: pointer;
    letter-spacing: 0.15rem;
  }

  @media (min-width: 350px) {
    input {
      padding: 0.5rem;
      border-radius: 1rem;
      padding-bottom: 0.25rem;
      letter-spacing: 0.12rem;
      font-weight: $fw-regular;
      font-size: $fs-400;
    }
  }

  input:hover {
    color: $clr-primary-400;
    background-color: $clr-neutral-100;
  }
</style>
