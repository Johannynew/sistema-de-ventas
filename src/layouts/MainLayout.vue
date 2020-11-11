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
    icon: 'assessment',

  },
  {
    title: 'Almacen',
<<<<<<< HEAD
=======

>>>>>>> f333d045184f8730575fbed876b1fe7c88271dea
    icon: 'analytics',
    link: 'https://github.com/quasarframework'
  },
  {
    title: 'Compras',
<<<<<<< HEAD
=======

>>>>>>> f333d045184f8730575fbed876b1fe7c88271dea
    icon: 'shopping_cart',
    link: 'https://chat.quasar.dev'
  },
  {
    title: 'Ventas',
<<<<<<< HEAD
=======

>>>>>>> f333d045184f8730575fbed876b1fe7c88271dea
    icon: 'leaderboard',
    link: 'https://forum.quasar.dev'
  },
  {
    title: 'Productos',
<<<<<<< HEAD
=======

>>>>>>> f333d045184f8730575fbed876b1fe7c88271dea
    icon: 'build_circle',
    link: 'https://twitter.quasar.dev'
  },
  {
    title: 'Administrar accesos',
<<<<<<< HEAD
=======

>>>>>>> f333d045184f8730575fbed876b1fe7c88271dea
    icon: 'accessibility',
    link: 'https://facebook.quasar.dev'
  },
  {
    title: 'Configuracion',
<<<<<<< HEAD
=======

>>>>>>> f333d045184f8730575fbed876b1fe7c88271dea
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
