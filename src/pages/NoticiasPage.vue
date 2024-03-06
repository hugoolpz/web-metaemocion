<script setup>
import { ref } from "vue";

const slide = ref(1)
const fullscreen = ref(false)
</script>

<template>
  <q-page>
    <div class="column q-gutter-y-xl">
      <div class="row flex-center q-gutter-xl">
        <q-card class="tarjeta-noticia q-my-md">
          <q-card-section class="bg-me-negro text-white text-h5 text-weight-bold">
            {{ $t('tenemos_nuestro_logo') }}
          </q-card-section>
          <q-card-section class="text-justify">
            {{ $t('ya_se_ha_votado_logo_proyecto') }} <span><a href="https://www.linkedin.com/in/rubendedirey/">Rubén De Diego Rey</a></span>! {{ $t('enhorabuena') }}
          </q-card-section>
          <q-carousel
            animated
            v-model="slide"
            v-model:fullscreen="fullscreen"
            arrows
            infinite
            class="shadow-2 rounded-border"
            control-color="me-rojo-claro"
            autoplay
            thumbnails>
            <q-carousel-slide :name="1" :img-src="$t('/foto-noticia-logo.jpg')"/>
            <q-carousel-slide :name="2" :img-src="$t('/foto-noticia-logo2.jpg')" />
            <q-carousel-slide :name="3" :img-src="$t('/foto-noticia-logo3.jpg')" />

            <template v-slot:control>
              <q-carousel-control
                position="bottom-right"
                :offset="[18, 18]"
              >
                <q-btn
                  push round dense color="white" text-color="me-rojo-claro"
                  :icon="fullscreen ? 'fullscreen_exit' : 'fullscreen'"
                  @click="fullscreen = !fullscreen"
                />
              </q-carousel-control>
            </template>
          </q-carousel>
        </q-card>

        <q-card class="tarjeta-noticia q-my-md">
          <q-card-section class="bg-me-negro text-white text-h5 text-weight-bold">
            ¡Hemos hecho un primer trailer para Met@emoción!
          </q-card-section>
          <q-card-section class="text-justify">
            Podemos mostraros un primer sneak peek de nuestro gran proyecto, ¡esperamos que os guste! Podeis verlo aquí:
          </q-card-section>
          <q-video
            :ratio="16/9"
            src="https://www.youtube.com/embed/k3_tw44QsZQ?rel=0"
          />
        </q-card>
      </div>
    </div>
  </q-page>
</template>
