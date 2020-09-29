<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar class="colornew">
        <q-avatar class="foto">
          <img src="../assets/logoamanda.png" />
        </q-avatar>
        <q-toolbar-title> Amanda Fonseca </q-toolbar-title>

        <q-space />

        <scrollactive
          ref="scrollactive"
          :offset="offset"
          :always-track="alwaysTrack"
          :duration="duration"
          :click-to-scroll="clickToScroll"
          :bezier-easing-value="easing"
          ><ul
            class="nav-center"
            style="
              padding: 0px;
              margin: 0px;
              list-style: none;
              display: inline-flex;
            "
          >
            <li>
              <a href="#banner" class="scrollactive-item nav-item">Banner</a>
            </li>
            <li>
              <a href="#sobre" class="scrollactive-item nav-item">Sobre</a>
            </li>
            <li>
              <a href="#skills" class="scrollactive-item nav-item">Skills</a>
            </li>
            <li>
              <a href="#contatos" class="scrollactive-item nav-item"
                >Contatos</a
              >
            </li>
          </ul>
        </scrollactive>
        <ul
          class="nav-center-midia"
          style="
            padding: 0px;
            margin: 0px;
            list-style: none;
            display: inline-flex;
          "
        >
          <li>
            <a
              class="whatsap"
              href="https://api.whatsapp.com/send?phone=5511989743490"
              target="_blank"
              ><i class="fa fa-whatsapp"></i
            ></a>
          </li>
          <li>
            <a class="instagram" href="#"
              ><i class="fa fa-instagram" target="_blank"></i
            ></a>
          </li>
          <li>
            <a
              class="linkedin"
              href="https://www.linkedin.com/in/amanda-fonseca-12b578101/"
              target="_blank"
              ><i class="fa fa-linkedin"></i
            ></a>
          </li>
          <li>
            <a
              class="github"
              href="https://github.com/AmandaFonseca"
              target="_blank"
              ><i class="fa fa-github"></i
            ></a>
          </li>
        </ul>
      </q-toolbar>
    </q-header>

    <!--    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"
    >
      <q-list>
        <q-item-label header class="text-grey-8">
          Essential Links
        </q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>-->

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>
<style scoped>
.colornew {
  background: #ff9999;
}
.q-avatar.foto {
  background: white;
}
ul.nav-center li {
  padding-left: 50px;
  padding-right: 50px;
}
ul.nav-center-midia li {
  padding-left: 20px;
  padding-right: 20px;
}
ul.nav-center-midia li a {
  font-size: 18px;
  color: white;
  font-weight: bold;
}
a.scrollactive-item.nav-item {
  color: white;
  font-weight: bold;
  text-decoration: none;
}
scrollactive ul li a:hover {
  background-color: pink;
  color: #6d6d6d;
  color: #f3ba35;
  padding: 1em;
}
</style>
<script lang="ts">
import EssentialLink from "components/EssentialLink.vue";

const linksData = [
  {
    title: "Docs",
    caption: "quasar.dev",
    icon: "school",
    link: "https://quasar.dev",
  },
  {
    title: "Github",
    caption: "github.com/quasarframework",
    icon: "code",
    link: "https://github.com/quasarframework",
  },
  {
    title: "Discord Chat Channel",
    caption: "chat.quasar.dev",
    icon: "chat",
    link: "https://chat.quasar.dev",
  },
  {
    title: "Forum",
    caption: "forum.quasar.dev",
    icon: "record_voice_over",
    link: "https://forum.quasar.dev",
  },
  {
    title: "Twitter",
    caption: "@quasarframework",
    icon: "rss_feed",
    link: "https://twitter.quasar.dev",
  },
  {
    title: "Facebook",
    caption: "@QuasarFramework",
    icon: "public",
    link: "https://facebook.quasar.dev",
  },
  {
    title: "Quasar Awesome",
    caption: "Community Quasar projects",
    icon: "favorite",
    link: "https://awesome.quasar.dev",
  },
];

import { defineComponent, ref } from "@vue/composition-api";

export default defineComponent({
  name: "MainLayout",
  components: { EssentialLink },
  setup() {
    const leftDrawerOpen = ref(false);
    const essentialLinks = ref(linksData);

    return { leftDrawerOpen, essentialLinks };
  },
  methods: {
    onItemChanged(event, currentItem, lastActiveItem) {
      // your logic
    },
  },
});
</script>
