<template>
  <div class="ActualCollectionSection">
    <div
      class="BackgroundContainer"
      :class="{ One: step == 1, Two: step == 2, Three: step == 3 }"
    >
      <div
        class="Background One"
        :class="{ Animate: step == 1, After: step == 2 }"
      ></div>
      <div
        class="Background Two"
        :class="{ Animate: step == 2, After: step == 3 }"
      ></div>
      <div
        class="Background Three"
        :class="{ Animate: step == 3, After: step == 1 }"
      ></div>
    </div>
    <div class="Adorno"></div>

    <div class="Content">
      <h3>Renacimiento: Colección de Primavera</h3>
      <p>
        Renueva tu estilo con nuestra colección de primavera: colores vibrantes,
        estampados frescos y diseños que te harán brillar en esta temporada.
        Descubre la moda que te inspira y te invita a disfrutar de la primavera
        con estilo y elegancia. ¡Déjate cautivar por la frescura de la temporada
        y encuentra tu look perfecto con nosotros
      </p>
    </div>
    <div class="ActualCollectionImageContainer">
      <transition
        enter-active-class="animated fadeIn slower"
        leave-active-class="animated fadeOut slower"
      >
        <div v-if="step == 1" class="ActualCollectionImage One"></div>
        <div v-else-if="step == 2" class="ActualCollectionImage Two"></div>
        <div v-else-if="step == 3" class="ActualCollectionImage Three"></div
      ></transition>
    </div>
  </div>
</template>

<script setup lang="ts">
import { onMounted } from 'vue';
import { ref } from 'vue';

const step = ref(1);

onMounted(() => {
  setInterval(() => {
    switch (step.value) {
      case 1:
        step.value = 2;
        break;
      case 2:
        step.value = 3;
        break;
      case 3:
        step.value = 1;
        break;
    }
  }, 3000);
});
</script>

<style src="./style/desktop.css"></style>
