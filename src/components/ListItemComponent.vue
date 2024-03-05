<template>
  <q-item clickable v-ripple @click="$emit('alClickar')">
    <q-item-section>
      <q-item-label>{{titulo}}</q-item-label>
      <q-item-label caption>{{subtitulo}}</q-item-label>
    </q-item-section>
  </q-item>
</template>

<script setup>
const props = defineProps(["titulo", "subtitulo"])
const emits = defineEmits(["alClickar"])
</script>
