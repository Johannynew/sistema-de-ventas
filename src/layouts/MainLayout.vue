<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />

        <q-toolbar-title>
          Repuesto Las Chicas
        </q-toolbar-title>

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
    >
      <q-list>
        <q-item-label
          header
          class="text-grey-8"
        >
          Menu
        </q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksData = [
  {
    title: 'Dashboard',
    caption: 'quasar.dev',
    icon: 'assessment',

    link: 'https://quasar.dev'
  },
  {
    title: 'Almacen',
    caption: 'github.com/quasarframework',


  },
  {
    title: 'Almacen',
    icon: 'analytics',
    link: 'https://github.com/quasarframework'
  },
  {
    title: 'Compras',

    caption: 'chat.quasar.dev',


    icon: 'shopping_cart',
    link: 'https://chat.quasar.dev'
  },
  {
    title: 'Ventas',

    caption: 'forum.quasar.dev',

    icon: 'leaderboard',
    link: 'https://forum.quasar.dev'
  },
  {
    title: 'Productos',

    caption: '@quasarframework',
    icon: 'build_circle',
    link: 'https://twitter.quasar.dev'
  },
  {
    title: 'Administrar accesos',

    caption: '@QuasarFramework',

    icon: 'accessibility',
    link: 'https://facebook.quasar.dev'
  },
  {
    title: 'Configuracion',

    caption: 'Community Quasar projects',


    icon: 'settings',
    link: 'https://awesome.quasar.dev'

  }
];

export default {
  name: 'MainLayout',
  components: { EssentialLink },
  data () {
    return {
      leftDrawerOpen: false,
      essentialLinks: linksData
    }
  }
}
</script>
