<script setup>
const props = defineProps({
  title: {
    type: String,
    default: "Link",
  },
  url: {
    type: String,
    default: "https://google.com",
  },
  backgroundColor: {
    type: String,
    default: "Charcoal",
  },
  textColor: {
    type: String,
    default: "Birch",
  },
});
</script>

<template>
  <div class="link-card">
    <a :href="url" target="_blank" rel="noopener noreferrer">
      <!-- TODO: replace with icons -->
      <h2>{{ title }}</h2>
    </a>
  </div>
</template>

<style lang="scss" scoped>
@use "./styles/_variables_colors.scss" as colors;

.link-card {
  --background-color: v-bind("backgroundColor");

  background-color: var(--background-color);
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex: 1;

  a {
    --text-color: v-bind("textColor");

    text-decoration: none;
    color: var(--text-color);
    font-family: "Josefin Sans", sans-serif;
    font-size: 1rem;
  }
}
</style>
