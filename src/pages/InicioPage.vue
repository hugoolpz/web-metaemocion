<template>
  <q-page padding>
    <transition appear mode="out-in" name="fade">
      <img v-show="!tarjetas" alt="logo-metaemocion" class="absolute-center"
           src="/logoMetaemocion.png" style="width: 35vh;">
    </transition>

    <transition mode="out-in" name="fade">
      <div v-show="tarjetas" class="column">
        <div class="row flex-center q-gutter-lg">
          <div class="col-auto col-md-auto col-sm-auto">
            <tarjeta-em-component :sobrelinea="$t('quien_forma_metaemocion')"
                                  :subtitulo="$t('adentrate_corazon_metaemocion')"
                                  :titulo="$t('departamentos')"
                                  foto="/foto-departamento.jpeg"
                                  @al-clickar="$router.push('/departamentos')"></tarjeta-em-component>
          </div>
          <div class="col-auto col-md-auto col-sm-auto">
            <tarjeta-em-component :sobrelinea="$t('ve_como_crece_metaemocion')"
                                  :subtitulo="$t('acompananos_viaje_tiempo')"
                                  :titulo="$t('trayectoria')"
                                  foto="/foto-saludo.png"
                                  @al-clickar="$q.notify({
                                    message: 'En construcción',
                                    color: 'warning',
                                    position: 'top',
                                    timeout: 1000,
                                    icon: 'fas fa-warning'
                                  })"></tarjeta-em-component>
          </div>
          <div class="col-auto col-md-auto col-sm-auto">
            <tarjeta-em-component :sobrelinea="$t('lee_sobre_metaemocion')"
                                  :subtitulo="$t('explora_mas_alla_titulares')"
                                  :titulo="$t('noticias')"
                                  foto="/foto-noticia-logo.jpg"
                                  @al-clickar="$router.push('/noticias')"></tarjeta-em-component>
          </div>
        </div>
      </div>
    </transition>
  </q-page>
</template>

<script setup>
import {ref} from "vue";
import TarjetaEmComponent from "components/TarjetaEmComponent.vue";
import {useI18n} from "vue-i18n";

const tarjetas = ref(false)
setTimeout(() => {
  tarjetas.value = true
}, 1500)
</script>
