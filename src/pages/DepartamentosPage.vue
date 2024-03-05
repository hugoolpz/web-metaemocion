<template>
  <q-page>
    <transition name="fade" mode="out-in" appear>
      <div class="column q-mt-xl q-pt-lg" v-show="departamento === ''">
        <div class="row flex-center q-gutter-xl">
          <div class="col-auto col-md-auto col-sm-auto">
            <tarjeta-em-component @al-clickar="departamento = 'programacion'" :sobrelinea="$t('codigo_que_emociona')" :titulo="$t('programacion')" foto="src/assets/tarjetas/ScriptingIntroPic.jpg"
                                  :subtitulo="$t('desde_creacion_mecanicas_juego')"></tarjeta-em-component>
          </div>
          <div class="col-auto col-md-auto col-sm-auto">
            <tarjeta-em-component @al-clickar="departamento = 'diseno'" :sobrelinea="$t('maxima_creatividad')" :titulo="$t('diseno')" foto="src/assets/tarjetas/blender.jpg"
                                  :subtitulo="$t('desde_creacion_mundos_impresionantes')"></tarjeta-em-component>
          </div>
          <div class="col-auto col-md-auto col-sm-auto">
            <tarjeta-em-component @al-clickar="departamento = 'sonido'" :sobrelinea="$t('gran_acustica')" :titulo="$t('sonido')" foto="src/assets/tarjetas/sonido.jpg"
                                  :subtitulo="$t('desde_composicion_bandas_sonoras')"></tarjeta-em-component>
          </div>
          <div class="col-auto col-md-auto col-sm-auto">
            <tarjeta-em-component @al-clickar="departamento = 'sistemas'" :sobrelinea="$t('nuestra_infraestructura_virtual')" :titulo="$t('sistemas')" foto="src/assets/tarjetas/sistemas.png"
                                  :subtitulo="$t('desde_gestion_servidores')"></tarjeta-em-component>
          </div>
        </div>
      </div>
    </transition>

    <transition name="fade" mode="out-in">
    <div class="column q-mt-xl q-pt-lg" v-show="departamento === 'programacion'">
      <div class="row flex-center q-gutter-x-xl">
        <div class="col-auto col-md-auto col-sm-auto">
          <tarjeta-miembro-component nombre="Hugo López Fernández" foto="src/assets/miembros/foto-hugo.jpg" linkedin="https://www.linkedin.com/in/hugo-l%C3%B3pez-fern%C3%A1ndez-b208a717b/"></tarjeta-miembro-component>
        </div>
        <div class="col-auto col-md-auto col-sm-auto">
          <tarjeta-miembro-component nombre="Pablo Hermida Gómez" foto="src/assets/miembros/foto-pablo.jpeg" linkedin="https://www.linkedin.com/in/pablo-hermida-g%C3%B3mez/"></tarjeta-miembro-component>
        </div>
        <div class="col-auto col-md-auto col-sm-auto">
          <tarjeta-miembro-component nombre="Diego Arroyo Portela" foto="src/assets/miembros/foto-diego.jpeg" linkedin="https://www.linkedin.com/in/diegoarroyoportela/"></tarjeta-miembro-component>
        </div>
      </div>
      <div class="row flex-center q-mt-xl q-pt-xl">
        <div class="col-auto"><q-btn class="bg-me-gradiente text-white" label="Volver" icon="fas fa-arrow-left" @click="departamento = ''"></q-btn></div>
      </div>
    </div>
    </transition>
    <transition name="fade" mode="out-in">
    <div class="column q-mt-xl q-pt-lg" v-show="departamento === 'diseno'">
      <div class="row flex-center q-gutter-x-xl">
        <div class="col-auto col-md-auto col-sm-auto">
          <tarjeta-miembro-component nombre="Verónica de Antonio Filippova" foto="src/assets/miembros/foto-veronica.jpg" linkedin="https://www.linkedin.com/in/ver%C3%B3nica-de-antonio-filippova-491306274/"></tarjeta-miembro-component>
        </div>
        <div class="col-auto col-md-auto col-sm-auto">
          <tarjeta-miembro-component nombre="Luna Arteaga Toro" foto="src/assets/miembros/foto-luna.jpeg" linkedin="https://www.linkedin.com/in/luna-arteaga-toro-921745222/"></tarjeta-miembro-component>
        </div>
        <div class="col-auto col-md-auto col-sm-auto">
          <tarjeta-miembro-component nombre="Luis Alfonso Luengo Pascual" foto="src/assets/miembros/foto-luis.jpg" linkedin="https://www.linkedin.com/in/luis-alfonso-luengo-pascual-8167a3223/"></tarjeta-miembro-component>
        </div>
        <div class="col-auto col-md-auto col-sm-auto">
          <tarjeta-miembro-component nombre="Christian Milanés Rodríguez" foto="src/assets/miembros/foto-christian.jpeg" linkedin="https://www.linkedin.com/in/christianmilnesrodriguez/"></tarjeta-miembro-component>
        </div>
      </div>
      <div class="row flex-center q-mt-xl q-pt-xl">
        <div class="col-auto"><q-btn class="bg-me-gradiente text-white" label="Volver" icon="fas fa-arrow-left" @click="departamento = ''"></q-btn></div>
      </div>
    </div>
    </transition>
    <transition name="fade" mode="out-in">
    <div class="column q-mt-xl q-pt-lg" v-show="departamento === 'sonido'">
      <div class="row flex-center q-gutter-x-xl">
        <div class="col-auto col-md-auto col-sm-auto">
          <tarjeta-miembro-component nombre="Juan Burillo Retuerto" foto="src/assets/miembros/foto-juan.jpg" linkedin="https://www.linkedin.com/in/juan-burillo/"></tarjeta-miembro-component>
        </div>
      </div>
      <div class="row flex-center q-mt-xl q-pt-xl">
        <div class="col-auto"><q-btn class="bg-me-gradiente text-white" label="Volver" icon="fas fa-arrow-left" @click="departamento = ''"></q-btn></div>
      </div>
    </div>
    </transition>
    <transition name="fade" mode="out-in">
    <div class="column q-mt-xl q-pt-lg" v-show="departamento === 'sistemas'">
      <div class="row flex-center q-gutter-x-xl">
        <div class="col-auto col-md-auto col-sm-auto">
          <tarjeta-miembro-component nombre="Daniel Sánchez de Arribas" foto="src/assets/miembros/foto-daniel.jpeg" linkedin="https://www.linkedin.com/in/dsancheza/"></tarjeta-miembro-component>
        </div>
        <div class="col-auto col-md-auto col-sm-auto">
          <tarjeta-miembro-component nombre="Marina Esteban Salvador" foto="src/assets/miembros/foto-marina.jpeg" linkedin="https://www.linkedin.com/in/marinaesteban/"></tarjeta-miembro-component>
        </div>
      </div>
      <div class="row flex-center q-mt-xl q-pt-xl">
        <div class="col-auto"><q-btn class="bg-me-gradiente text-white" label="Volver" icon="fas fa-arrow-left" @click="departamento = ''"></q-btn></div>
      </div>
    </div>
    </transition>
  </q-page>
</template>
<script setup>
import TarjetaEmComponent from "components/TarjetaEmComponent.vue";
import TarjetaMiembroComponent from "components/TarjetaMiembroComponent.vue";
import {ref} from "vue";

const departamento = ref('')
</script>
