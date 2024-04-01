<template>
  <section class="HeroSection">
    <header>
      <div class="Logo"></div>

      <nav>
        <ul>
          <li
            @pointerenter="linkHover = 'one'"
            @pointerleave="linkHover = 'none'"
          >
            <div v-if="linkHover == 'one'" class="Adorno"></div>
            <span> Olivia </span>
            <div v-if="linkHover == 'one'" class="Adorno"></div>
          </li>
          <li
            @pointerenter="linkHover = 'two'"
            @pointerleave="linkHover = 'none'"
          >
            <div v-if="linkHover == 'two'" class="Adorno"></div>
            <span> Luka </span>
            <div v-if="linkHover == 'two'" class="Adorno"></div>
          </li>
          <li
            @pointerenter="linkHover = 'three'"
            @pointerleave="linkHover = 'none'"
          >
            <div v-if="linkHover == 'three'" class="Adorno"></div>
            <span> Sobre Nosotros </span>
            <div v-if="linkHover == 'three'" class="Adorno"></div>
          </li>
          <q-space></q-space>
          <li
            @pointerenter="linkHover = 'four'"
            @pointerleave="linkHover = 'none'"
          >
            <div v-if="linkHover == 'four'" class="Adorno"></div>
            <span> Tienda </span>
            <div v-if="linkHover == 'four'" class="Adorno"></div>
          </li>
        </ul>
      </nav>
    </header>
    <div class="BackdropFilter"></div>
    <div class="TitleContainer">
      <h1>Olivia Shop</h1>
      <h2>
        Viste con
        <div class="SpanContainer">
          <transition name="slide-up-two">
            <span v-if="text2 == 'one'">estilo</span>
            <span v-else-if="text2 == 'two'">gracia</span>
          </transition>
          <div class="Adorno"></div>
        </div>

        , camina con
        <div class="SpanContainer">
          <transition name="slide-up">
            <span v-if="text1 == 'one'">elegancia</span>
            <span v-else-if="text1 == 'two'">fortaleza</span>
          </transition>
          <div class="Adorno"></div>
        </div>
      </h2>
      <div class="CallToActionContainer">
        <div class="Adorno"></div>

        <q-btn
          class="CallToAction"
          no-caps
          label="Visitanos"
          flat
          dense
        ></q-btn>
        <div class="Adorno"></div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { onMounted, ref } from 'vue';

const text1 = ref('one');
const text2 = ref('one');

const linkHover = ref('none');

onMounted(() => {
  setInterval(() => {
    text1.value == 'one' ? (text1.value = 'two') : (text1.value = 'one');
  }, 4500);

  setInterval(() => {
    text2.value == 'one' ? (text2.value = 'two') : (text2.value = 'one');
  }, 6000);
});
</script>

<style src="./style/desktop.css"></style>
