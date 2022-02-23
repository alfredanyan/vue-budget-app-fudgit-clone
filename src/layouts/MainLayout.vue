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
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title> Quasar App </q-toolbar-title>

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <q-item-label header> Essential Links </q-item-label>

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
import { ref } from "vue";

export default {
  name: "MainLayout",

  setup() {
    const leftDrawer = ref(false);

    return {
      leftDrawer,
      navLinks: [
        {
          title: "Budgets",
          icon: "la la-wallet",
          link: "/budgets",
        },
        {
          title: "Starred",
          icon: "lar la-star",
          link: "/starred",
        },
        {
          title: "Settings",
          icon: "las la-cog",
          link: "/settings",
        },
        {
          title: "Account",
          icon: "lar la-user",
          link: "/account",
        },
      ],
    };
  },
};
</script>
