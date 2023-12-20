<script setup>
import ProductCard from '@/components/ProductCard.vue'
import { ref } from 'vue'

const products = ref([
  {
    id: 22797,
    name: 'Ekol Ketchup Krav',
    brand: 'FELIX',
    size: '2500',
    unit_abbr: 'g',
    image_url:
      'https://s3-eu-west-1.amazonaws.com/valstorage.consupedia.com/products.320x320/498/07310240084498.product.320x320.000.png',
    country_alpha2: 'SE',
    is_eco: 1,
    ethic_id: 3,
    for_you: 'CANT_TELL',
    average_price: null,
    currency: 'kr',
    climate_score: 52,
    water_score: null,
    health_score: 35,
    fairness_score: 75
  },
  {
    id: 22794,
    name: 'Krav Eko Ketchup Msms Sentomat',
    brand: 'FELIX',
    size: '2500',
    unit_abbr: 'g',
    image_url:
      'https://s3-eu-west-1.amazonaws.com/valstorage.consupedia.com/products.320x320/399/07310240084399.product.320x320.000.png',
    country_alpha2: 'SE',
    is_eco: 1,
    ethic_id: 3,
    for_you: 'CANT_TELL',
    average_price: null,
    currency: 'kr',
    climate_score: 52,
    water_score: null,
    health_score: 55,
    fairness_score: 75
  },
  {
    id: 2271151394,
    name: 'Ketchup Ekologisk',
    brand: 'Heinz',
    size: '1015',
    unit_abbr: 'g',
    image_url:
      'https://s3-eu-west-1.amazonaws.com/images.consupedia.com/products/08715700413341.jpg',
    country_alpha2: 'NL',
    is_eco: 1,
    ethic_id: 3,
    for_you: 'CANT_TELL',
    average_price: 30,
    currency: 'kr',
    climate_score: 51,
    water_score: null,
    health_score: 35,
    fairness_score: 74
  }
])
</script>

<template>
  <h1>Products for good</h1>
  <div class="products">
    <ProductCard v-for="product in products" :key="product.id" :product="product" />
  </div>
</template>

<style scoped>
.products {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
