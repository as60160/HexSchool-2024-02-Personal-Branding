<template>
  <div class="service-card" v-for="(service, id) in services" :key="id">
    <img :src="service.src" :alt="service.title" class="icon" />
    <h3 class="fs-3">{{ service.title }}</h3>
  </div>
</template>

<script setup>
  const props = defineProps(['services']);
</script>

<style scoped lang="scss">
  .service-card {
    width: 23%;
    max-width: 300px;
    height: 23vw;
    max-height: 306px;
    padding: 20px 30px;
    border-radius: 16px;
    background: linear-gradient(315deg, #1E1E1E 0%, #1E1E1E 49.97%, #000000 50%);
    color: #fff;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 24px;

    @media screen and (max-width: 992px) {
      width: 48%;
      max-width: 450px;
      height: 48vw;
      max-height: 450px;
    }
  }
</style>
