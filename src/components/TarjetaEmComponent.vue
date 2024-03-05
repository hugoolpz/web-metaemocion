<template>
  <q-card class="tarjeta-em cursor-pointer" bordered v-ripple @click="$emit('alClickar')">
    <q-img
      :src="foto || 'https://cdn.quasar.dev/img/parallax2.jpg'"
      style="max-height: 200px"
    />

    <q-card-section>
      <div class="text-overline text-me-azul">{{sobrelinea}}</div>
      <div class="text-h5 q-mt-sm q-mb-xs">{{titulo}}</div>
      <div class="text-caption text-me-negro text-justify">
        {{subtitulo}}
      </div>
    </q-card-section>
  </q-card>
</template>

<script setup>
const props = defineProps(["sobrelinea", "titulo", "subtitulo", 'foto'])
const emits = defineEmits(["alClickar"])
</script>
