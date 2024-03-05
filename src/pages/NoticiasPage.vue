<script setup>
import { ref } from "vue";

const slide = ref(1)
</script>

<template>
  <q-page>
    <div class="column q-mt-xs q-mb-xl q-gutter-y-xl">
      <div class="row flex-center">
        <q-card class="tarjeta-noticia">
          <q-card-section class="bg-me-negro text-white text-h5 text-weight-bold">
            {{ $t('tenemos_nuestro_logo') }}
          </q-card-section>
          <q-card-section class="text-justify">
            {{ $t('ya_se_ha_votado_logo_proyecto') }} <span><a href="https://www.linkedin.com/in/rubendedirey/">Rubén De Diego Rey</a></span>! {{ $t('enhorabuena') }}
          </q-card-section>
          <q-carousel
            animated
            v-model="slide"
            arrows
            navigation
            infinite
            class="shadow-2 rounded-border"
            control-color="me-rojo-claro"
            autoplay
          >
            <q-carousel-slide :name="1" :img-src="$t('src/assets/tarjetas/foto-noticia-logo.jpg')" />
            <q-carousel-slide :name="2" :img-src="$t('src/assets/tarjetas/foto-noticia-logo2.jpg')" />
            <q-carousel-slide :name="3" :img-src="$t('src/assets/tarjetas/foto-noticia-logo3.jpg')" />
            <q-carousel-slide :name="4" :img-src="$t('src/assets/tarjetas/foto-noticia-logo4.jpg')" />
          </q-carousel>
        </q-card>
      </div>
    </div>
  </q-page>
</template>
