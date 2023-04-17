<script setup>
  import { defineProps } from "vue";

  const props = defineProps({
    rate: {
      type: Number,
      required: true,
      default: 0,
    },
  });
</script>

<template>
  <div class="layout">
    <img src="@/assets/icons/illustration-thank-you.svg" alt="" />
    <span class="text-primary-400 bg-neutral-400 fw-regular"
      >You selected {{ props.rate }} out of 5</span
    >
    <h2 class="text-neutral-100 fw-bold fs-pr-heading fs-600">Thank you!</h2>
    <p class="text-neutral-200">
      We appreciate you taking the time to give a rating. If you ever need more
      support,don’t hesitate to get in touch!
    </p>
  </div>
</template>

<style lang="scss" scoped>
  .layout {
    display: grid;
    grid-template-rows: repeat(3, auto);
    place-items: center;
    gap: 1rem;

    padding: 1rem 0;
  }

  p {
    font-size: $fs-400;
  }

  img {
    height: 5rem;
  }

  span {
    padding: 0.4rem 0.75rem;
    padding-bottom: 0.1rem;
    border-radius: 1rem;
    margin: 0.5rem 0;
    font-size: clac($fs-400 - 0.05rem);
  }

  @media (min-width: 350px) {
    p {
      width: 31ch;
    }
  }
</style>
