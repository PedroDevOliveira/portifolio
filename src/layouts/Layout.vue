<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-custom">
      <q-toolbar>
        <!-- <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        /> -->

        <q-toolbar-title class="logo">
          Portfolio
        </q-toolbar-title>

        <div class="links">
          <a href="#about">Sobre</a>
          <a href="#services">Serviços</a>
          <a href="#works">Trabalhos</a>
          <a href="#testemonials">Relatos</a>
          <a href="#contact">Contato</a>
        </div>
      </q-toolbar>
    </q-header>

    <!-- <q-drawer
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
          Essential Links
        </q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer> -->

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">
import EssentialLink from "components/EssentialLink.vue";

const linksData = [
  {
    title: "Docs",
    caption: "quasar.dev",
    icon: "school",
    link: "https://quasar.dev"
  },
  {
    title: "Github",
    caption: "github.com/quasarframework",
    icon: "code",
    link: "https://github.com/quasarframework"
  },
  {
    title: "Discord Chat Channel",
    caption: "chat.quasar.dev",
    icon: "chat",
    link: "https://chat.quasar.dev"
  },
  {
    title: "Forum",
    caption: "forum.quasar.dev",
    icon: "record_voice_over",
    link: "https://forum.quasar.dev"
  },
  {
    title: "Twitter",
    caption: "@quasarframework",
    icon: "rss_feed",
    link: "https://twitter.quasar.dev"
  },
  {
    title: "Facebook",
    caption: "@QuasarFramework",
    icon: "public",
    link: "https://facebook.quasar.dev"
  },
  {
    title: "Quasar Awesome",
    caption: "Community Quasar projects",
    icon: "favorite",
    link: "https://awesome.quasar.dev"
  }
];

import { defineComponent, ref } from "@vue/composition-api";

export default defineComponent({
  name: "MainLayout",
  components: { EssentialLink },
  setup() {
    const leftDrawerOpen = ref(false);
    const essentialLinks = ref(linksData);

    return { leftDrawerOpen, essentialLinks };
  }
});
</script>

<style lang="scss">
.bg-custom {
  background-color: #0c0c0e;

  .logo {
    color: #fff;
    font-size: 24px;
    font-weight: 700;
    letter-spacing: 2px;
  }
}

.links a {
  text-decoration: none;
  color: #fff;
  margin: 4px;
  font-weight: 700;
  letter-spacing: 0px;
}

@media (max-width: 991px) {
  .links a {
    display: none;
  }
}
</style>
