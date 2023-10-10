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
      <BentoCard :background-color="Charcoal" padding="0">
        <template #content>
          <img src="./assets/images/headshot.jpg" alt="James" />
        </template>
      </BentoCard>
      <BentoCard :background-color="Charcoal">
        <template #content>
          <h2>IS A</h2>
        </template>
      </BentoCard>
      <BentoCard :background-color="Charcoal">
        <template #content>
          <h2>SOFTWARE ENGINEER</h2>
        </template>
      </BentoCard>
      <BentoCard :background-color="Charcoal">
        <template #content>
          <h2>IN</h2>
        </template>
      </BentoCard>
      <BentoCard :background-color="GoldenHour">
        <template #content>
          <h2 class="location">MINNESOTA</h2>
        </template>
      </BentoCard>
      <BentoCard :background-color="Charcoal">
        <template #content>
          <h2>"To be or not to be, that is the question."</h2>
        </template>
      </BentoCard>
      <BentoCard :background-color="Charcoal">
        <template #content>
          <h2>I occasionally write words.</h2>
        </template>
      </BentoCard>
      <BentoCard :background-color="Charcoal">
        <template #content>
          <h2>I like to take photos.</h2>
        </template>
      </BentoCard>
      <BentoCard :background-color="GoldenHour">
        <template #content>
          <h2 class="contact">SAY HELLO</h2>
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

// TODO: stop hardcoding this class
.location,
.contact {
  color: v-bind("Gunmetal");
}

img {
  width: 100%;
  min-width: 300px;
  border-radius: 8px;
}
</style>
