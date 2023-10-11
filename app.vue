<script setup>
import BentoCard from "./components/BentoCard.vue";
import BentoGrid from "./components/BentoGrid.vue";
import LinkCard from "./components/LinkCard.vue";
import {
  Birch,
  GoldenHour,
  Charcoal,
  Gunmetal,
} from "./styles/variables.module.scss";
import "./styles/app.scss";
const links = [
  {
    title: "GitHub",
    url: "https://github.com",
  },
  {
    title: "LinkedIn",
    url: "https://linkedin.com",
  },
  {
    title: "Twitter",
    url: "https://twitter.com",
  },
];
</script>
<template>
  <div class="app">
    <BentoGrid>
      <BentoCard :background-color="GoldenHour">
        <template #content>
          <h1><bold>Hi, I'm James.</bold></h1>
        </template>
      </BentoCard>
      <BentoCard :background-color="Charcoal" padding="0">
        <template #content>
          <img src="./assets/images/headshot.jpg" alt="James" />
        </template>
      </BentoCard>
      <BentoCard :background-color="Charcoal">
        <template #content>
          <h2>Software Engineer</h2>
        </template>
      </BentoCard>
      <BentoCard :background-color="GoldenHour">
        <template #content>
          <h2 class="location">📌 Minnesota</h2>
        </template>
      </BentoCard>
    </BentoGrid>
    <BentoGrid>
      <LinkCard
        v-for="link in links"
        :title="link.title"
        :url="link.url"
        :background-color="Charcoal"
        :text-color="Birch"
      />
    </BentoGrid>
    <BentoGrid>
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
          <h2 class="contact">Say Hello 👋</h2>
        </template>
      </BentoCard>
    </BentoGrid>
  </div>
</template>
<style lang="scss" scoped>
.app {
  display: flex;
  flex-direction: column;
  gap: 1rem;

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
}
</style>
