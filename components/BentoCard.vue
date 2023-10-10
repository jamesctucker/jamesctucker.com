<script setup>
const props = defineProps({
  backgroundColor: {
    type: String,
    default: "white",
  },
});
</script>

<template>
  <div class="bento-card">
    <slot name="content" />
  </div>
</template>
<style lang="scss" scoped>
.bento-card {
  --background-color: v-bind("backgroundColor");

  background-color: var(--background-color);
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  padding: 16px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex: 1;
}
</style>
