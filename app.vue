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
          <h1><bold>JAMES</bold></h1>
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
  font-family: "Josefin Sans", sans-serif;
  font-weight: 700;
  font-size: 3rem;
}

h2 {
  color: v-bind("Birch");
  text-align: center;
  font-family: "Josefin Sans", sans-serif;
  font-weight: 400;
  font-size: 3rem;
}
</style>
