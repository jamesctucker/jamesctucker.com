<script setup>
const props = defineProps({
  backgroundColor: {
    type: String,
    default: "white",
  },
  padding: {
    type: String,
    default: "16px",
  },
});
</script>

<template>
  <div class="bento-card">
    <slot name="content" />
  </div>
</template>
<style lang="scss" scoped>
@use "./styles/_variables_colors.scss" as colors;
.bento-card {
  --background-color: v-bind("backgroundColor");
  --padding: v-bind("padding");

  background-color: var(--background-color);
  border-radius: 8px;
  padding: var(--padding);
  display: flex;
  align-items: center;
  justify-content: center;
  flex: 1;
}

// on hover, mimic pushing a key down on a typewriter
.bento-card:hover {
  animation: keypress 0.2s linear;
  cursor: pointer;
}

// remove box shadow gradually to mimic key being released
@keyframes keypress {
  0% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(4px);
  }
  100% {
    transform: translateY(0px);
  }
}

// TODO: add hover style that has a custom cursor (I want to add a paper airplane icon)
// .bento-card:hover {
//   cursor: pointer;
// }
</style>
