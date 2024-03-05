<template>
  <q-layout>
    <q-page-container>
      <q-header>
        <q-toolbar class="bg-me-gradiente">
          <q-btn class="text-me-negro bg-white" icon="fas fa-list" @click="menuIzq = !menuIzq"></q-btn>
          <q-toolbar-title class="text-weight-bold cursor-pointer" @click="$router.push('/')">MET@EMOCIÓN <q-avatar><img src="src/assets/iconoMetaemocion.jpg" alt="icono-metaemocion"></q-avatar></q-toolbar-title>
          <q-btn-dropdown v-model="idioma" class="text-me-negro bg-white" dropdown-icon="none" auto-close>
            <template v-slot:label>
              <div class="row absolute-center">
                <q-icon name="fas fa-globe" />
              </div>
            </template>
            <q-list>
              <q-scroll-area style="width: 160px; height: 112px;">
                <idiomas-item-component :titulo="$t('espanol')" idioma="Español" :cod-idioma="locale"
                                        cod-bandera="es-ESP" @al-clickar="cambiarIdioma('es')"
                ></idiomas-item-component>
                <idiomas-item-component :titulo="$t('ingles')" idioma="Inglés" :cod-idioma="locale" cod-bandera="en-US" @al-clickar="cambiarIdioma('en')"
                ></idiomas-item-component>
                <idiomas-item-component :titulo="$t('frances')" idioma="Francés" :cod-idioma="locale"
                                        cod-bandera="fr-FR" @al-clickar="cambiarIdioma('fr')"
                ></idiomas-item-component>
                <idiomas-item-component :titulo="$t('aleman')" idioma="Alemán" :cod-idioma="locale" cod-bandera="de-DE" @al-clickar="cambiarIdioma('de')"
                ></idiomas-item-component>
                <idiomas-item-component :titulo="$t('italiano')" idioma="Italiano" :cod-idioma="locale"
                                        cod-bandera="it-IT" @al-clickar="cambiarIdioma('it')"
                ></idiomas-item-component>
                <idiomas-item-component :titulo="$t('chino')" idioma="Chino" :cod-idioma="locale" cod-bandera="zh-CN" @al-clickar="cambiarIdioma('zh')"
                ></idiomas-item-component>
              </q-scroll-area>
            </q-list>
          </q-btn-dropdown>
        </q-toolbar>
      </q-header>
      <router-view/>
    </q-page-container>

    <q-drawer
      v-model="menuIzq"
      bordered
      :width="350"
      :breakpoint="30"
    >
      <q-scroll-area class="fit">
        <q-list bordered separator>
          <list-item-component :titulo="$t('departamentos')"
                               :subtitulo="$t('conoce_quien_detras_metaemocion')" @al-clickar="$router.push('/departamentos')"></list-item-component>
          <list-item-component :titulo="$t('trayectoria')"
                               :subtitulo="$t('observa_como_metaemocion_progresa')" @click="$router.push('/trayectoria')"></list-item-component>
          <list-item-component :titulo="$t('noticias')"
                               :subtitulo="$t('lee_sobre_novedades_sociales_metaemocion')" @click="$router.push('/noticias')"></list-item-component>
        </q-list>
      </q-scroll-area>
    </q-drawer>
  </q-layout>
</template>

<script setup>
import { ref } from "vue";
import { useI18n } from "vue-i18n";
import ListItemComponent from "components/ListItemComponent.vue";
import IdiomasItemComponent from "components/IdiomasItemComponent.vue";

function cambiarIdioma(idioma) {
  locale.value = idioma
}

const { locale } = useI18n()
const menuIzq = ref(false)
const idioma = ref(false)
</script>
