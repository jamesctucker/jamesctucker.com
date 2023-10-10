<script setup>
import BentoCard from "./components/BentoCard.vue";
import BentoGrid from "./components/BentoGrid.vue";
import {
  Birch,
  GoldenHour,
  Charcoal,
  Gunmetal,
} from "./styles/variables.module.scss";
import "./styles/app.scss";
</script>

<template>
  <div>
    <BentoGrid>
      <BentoCard :background-color="GoldenHour">
        <template #content>
          <h1>JAMES</h1>
        </template>
      </BentoCard>
      <BentoCard :background-color="Charcoal">
        <template #content>
          <h2>IS</h2>
        </template>
      </BentoCard>
      <BentoCard :background-color="Charcoal">
        <template #content>
          <h2>A</h2>
        </template>
      </BentoCard>
      <BentoCard :background-color="Charcoal">
        <template #content>
          <h2>SOFTWARE ENGINEER.</h2>
        </template>
      </BentoCard>
    </BentoGrid>
  </div>
</template>
<style lang="scss" scoped>
h1 {
  color: v-bind("Gunmetal");
  text-align: center;
}

h2 {
  color: v-bind("Birch");
  text-align: center;
}
</style>
