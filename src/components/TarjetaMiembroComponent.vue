<script setup>
const props = defineProps(['nombre', 'foto', 'linkedin'])

function irHaciaLinkedIn() {
  window.open(props.linkedin, "_blank")
}
</script>

<template>
  <q-card bordered class="tarjeta-miembro q-mt-lg">
    <q-img :src="foto" style="width: 250px; height: 250px">
      <div class="absolute-bottom text-body2">
        {{nombre}}
      </div>
    </q-img>
    <q-card-actions align="right" style="border: 1px solid #333434">
      <q-btn flat label="LinkedIn" style="background-color: #0A66C2" class="text-white" icon="fab fa-linkedin" @click="irHaciaLinkedIn"></q-btn>
    </q-card-actions>
  </q-card>
</template>
