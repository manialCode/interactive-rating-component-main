<script setup>
  import { defineEmits, ref } from "vue";
  import RateButton from "./BaseButton.vue";
  import BaseSubmitButton from "./BaseSubmitButton.vue";

  const items = [1, 2, 3, 4, 5];
  const number = ref(0);

  const defineItem = (param) => {
    number.value = param;
    console.log(
      "%cMyProject%cline:13%cparam",
      "color:#fff;background:#ee6f57;padding:3px;border-radius:2px",
      "color:#fff;background:#1f3c88;padding:3px;border-radius:2px",
      "color:#fff;background:rgb(161, 23, 21);padding:3px;border-radius:2px",
      number.value
    );
  };

  const emit = defineEmits(["changeComp"]);
  const rated = (rate) => {
    emit("changeComp", rate);
  };
</script>

<template>
  <div class="layout">
    <div id="star-box">
      <img src="@/assets/icons/icon-star.svg" alt="Star icon" />
    </div>
    <div class="headers">
      <h1 class="fs-pr-heading text-neutral-100 text-r">How did we do?</h1>
      <h2 class="text-neutral-200 text-r fs-400">
        Please let us know how we did with your support request. All feedback is
        appreciated to help us improve our offering!
      </h2>
    </div>
    <ul role="list">
      <li v-for="(item, index) in items" :key="index">
        <RateButton :option="item" @click.prevent="defineItem(item)" />
      </li>
    </ul>
    <BaseSubmitButton @click="rated(number)" />
  </div>
</template>

<style lang="scss" scoped>
  .layout {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    .headers {
      h1 {
        margin-bottom: 0.5rem;
        letter-spacing: 0.05rem;
      }
    }
  }

  @media (min-width: 400px) {
    .headers {
      h2 {
        width: 35ch;
      }
    }
  }

  #star-box img {
    background-color: $clr-neutral-300;
    padding: 0.7rem;
    border-radius: 50%;
  }

  ul[role="list"] {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin: 0.25rem 0;
  }
</style>
