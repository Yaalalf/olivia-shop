<template>
  <q-page>
    <HeroSection />
    <OnBoardingSection />
    <ActualCollectionSection />
    <CubanStoresSection />
  </q-page>
</template>

<script setup lang="ts">
import HeroSection from 'src/components/sections/hero/HeroSection.vue';
import OnBoardingSection from 'src/components/sections/onBoarding/OnBoardingSection.vue';
import ActualCollectionSection from 'src/components/sections/actualCollection/ActualCollectionSection.vue';
import CubanStoresSection from 'src/components/sections/cubanStores/CubanStoresSection.vue';
</script>
