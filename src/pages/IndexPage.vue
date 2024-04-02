<template>
  <q-page>
    <HeroSection />
    <OnBoardingSection />
    <ActualCollectionSection />
    <CubanStoresSection /> <SwinsuitSection />
  </q-page>
</template>

<script setup lang="ts">
import HeroSection from 'src/components/sections/hero/HeroSection.vue';
import OnBoardingSection from 'src/components/sections/onBoarding/OnBoardingSection.vue';
import ActualCollectionSection from 'src/components/sections/actualCollection/ActualCollectionSection.vue';
import CubanStoresSection from 'src/components/sections/cubanStores/CubanStoresSection.vue';
import SwinsuitSection from 'src/components/sections/swimsuit/SwimsuitSection.vue';
</script>
