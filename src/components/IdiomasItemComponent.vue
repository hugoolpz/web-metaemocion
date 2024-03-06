<template>
  <q-item :active="codIdioma === idioma" active-class="bg-em-gradiente text-white" clickable v-close-popup
          @click="$emit('alClickar')">
    <q-item-section avatar>
      <q-avatar>
        <img :src="urlFoto">
      </q-avatar>
    </q-item-section>
    <q-item-section>
      <q-item-label class="text-me-negro">{{ titulo }}</q-item-label>
    </q-item-section>
  </q-item>
</template>

<script setup>
import { ref } from 'vue';
const props = defineProps(["titulo", "codBandera", "codIdioma", "idioma"])
const emits = defineEmits(['alClickar'])
const urlFoto = ref(`/${props.codBandera}.png`)
</script>
