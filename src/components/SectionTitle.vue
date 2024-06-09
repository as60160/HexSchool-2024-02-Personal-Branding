<template>
  <div class="text-center">
    <h2 class="title h2w d-inline-block">{{ content }}</h2>
  </div>
</template>

<script setup>
  const props = defineProps({
    content: {
      type: String,
    }
  });
</script>

<style scoped lang="scss">
.title {
    &::before,
    &::after {
      content: '';
      display: block;
      width: 100px;
      height: 6px;
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
    }

    &::before {
      left: -116px;
      background-image: url('../assets/icons/title-deco-left-lg.svg');
    }

    &::after {
      right: -116px;
      background-image: url('../assets/icons/title-deco-right-lg.svg');
    }
  }
</style>