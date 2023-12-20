<script setup>
defineProps({
  product: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <div class="product-card">
    <h2>{{ product.name }}</h2>
    <p><b>Märke</b> {{ product.brand }}</p>
    <p><b>Storlek</b> {{ product.size }} {{ product.unit_abbr }}</p>
    <p><b>Ursprung</b> {{ product.country_alpha2 }}</p>
    <p><b>Pris</b> {{ product.average_price }} {{ product.currency }}</p>
    <p><b>Klimat</b> {{ product.climate_score }}</p>
    <p><b>Hälso</b> {{ product.health_score }}</p>
    <p><b>Rättvisa</b> {{ product.fairness_score }}</p>
  </div>
</template>

<style scoped>
.product-card {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #39495c;
  margin-bottom: 18px;
}
.product-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
}
</style>
