<script setup>
  import RateLayout from "@/layouts/RateLayout.vue";
  import { ref, defineAsyncComponent } from "vue";

  const userRate = ref(0);

  const TheRateMenu = defineAsyncComponent(() =>
    import("@/common/TheRateMenu.vue")
  );

  const TheThankYouMenu = defineAsyncComponent(() =>
    import("@/common/TheThankYouMenu.vue")
  );

  const comp = ref(TheRateMenu);
  const handleComp = (rate) => {
    comp.value = TheThankYouMenu;
    userRate.value = rate;
  };
</script>

<template>
  <RateLayout>
    <component :is="comp" @changeComp="handleComp" :rate="userRate"></component>
  </RateLayout>
  <div class="attribution">
    Challenge by
    <a href="https://www.frontendmentor.io?ref=challenge" target="_blank"
      >Frontend Mentor</a
    >. Coded by
    <a href="https://github.com/manialCode" target="_blank">Juan Martin Monti</a
    >.
  </div>
</template>

<style lang="scss">
  .attribution {
    font-size: 11px;
    text-align: center;
    a {
      color: hsl(228, 45%, 44%);
    }
  }
</style>
