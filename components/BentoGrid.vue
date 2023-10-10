<template>
  <div class="bento-grid">
    <slot />
  </div>
</template>
<style lang="scss" scoped>
.bento-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}
</style>
