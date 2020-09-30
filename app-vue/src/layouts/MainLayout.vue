<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar class="colornew">
        <Slide class="slider" style="background-color: #dfdfdf!important">
          <a id="banner" href="#banner">
            <span>Banner</span>
          </a>
          <a id="Sobre" href="#sobre">
            <span>Sobre</span>
          </a>
          <a id="Skills" href="#skills">
            <span>Skills</span>
          </a>
          <a id="Contatos" href="#contatos">
            <span>Contatos</span>
          </a>
        </Slide>

        <q-avatar class="foto" style="margin-left:2em;">
          <img src="../assets/logoamanda.png" />
        </q-avatar>
        <q-toolbar-title> Amanda Fonseca </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<style scoped>
span.bm-burger-bars.line-style {
    background-color: white;
}
.slider {
  top: -50%;
  position: absolute;
  left: 0%;

}
.colornew {
  background: #ff9999;
}
.q-avatar.foto {
  background: white;
}
ul.nav-center li {
  padding-left: 30px;
  padding-right: 30px;
}
ul.nav-center-midia li {
  padding-left: 20px;
  padding-right: 20px;
}
ul.nav-center-midia li a {
  font-size: 18px;
  font-weight: bold;
}
a.scrollactive-item.nav-item,
ul.nav-center li a {
  font-weight: bold;
  text-decoration: none;
}
ul.nav-center.menu-top li a {
  display: none;
  color: white;
}
scrollactive .menu-top li a:hover {
  background-color: pink;
  color: white;
  color: #6d6d6d;
  color: #f3ba35;
  padding: 1em;
}

ul.nav-center.menu-top li a,
.nav-center-midia {
  color: white;
  list-style: none;
}
ul.nav-center-midia li a {
  color: white;
}
.bg-grey-1 {
  background: #ffa6a6 !important;
}
.q-drawer__content.fit.scroll {
  background-color: #ebebe0;
}
li {
  list-style: none;
}
ul.nav-lateral li a {
  color: #ff9999;
}
@media (min-width: 22em) {
}

@media (min-width: 68em) {
  ul.nav-center.menu-top li a {
    display: inline-block;
  }
}

.bm-burger-button {
  top: 10px !important;
  width: 36px;
}
</style>co


<script lang="ts">
import EssentialLink from "components/EssentialLink.vue";
import { Slide } from "vue-burger-menu";
var url = window.location.origin;
url = `${url}/`;
const linksData = [
  {
    title: "Banner",
    caption: "quasar.dev",
    icon: "school",
    link: `${url}#banner`,
  },
  {
    title: "Sobre",
    caption: "github.com/quasarframework",
    icon: "code",
    link: `${url}#sobre`,
  },
  {
    title: "Skills",
    caption: "chat.quasar.dev",
    icon: "chat",
    link: `${url}#skills`,
  },
  {
    title: "Contatos",
    caption: "forum.quasar.dev",
    icon: "record_voice_over",
    link: `${url}#contatos`,
  },
];

export default {
  name: "MainLayout",
  components: { EssentialLink, Slide },
  data() {
    return {
      leftDrawerOpen: false,
      essentialLinks: linksData,
      urllocal: window.location.origin,
    };
  },
};
</script>
