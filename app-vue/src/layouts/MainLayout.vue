<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar class="colornew">
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />

        <q-avatar class="foto">
          <img src="../assets/logoamanda.png" />
        </q-avatar>
        <q-toolbar-title> Amanda Fonseca </q-toolbar-title>

        <scrollactive
          ref="scrollactive"
          :offset="offset"
          :always-track="alwaysTrack"
          :duration="duration"
          :click-to-scroll="clickToScroll"
          :bezier-easing-value="easing"
          ><ul
            class="nav-center menu-top"
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

        <!--<div>Quasar v{{ $q.version }}</div>-->
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

<style scoped>
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
</style>co


<script lang="ts">
import EssentialLink from "components/EssentialLink.vue";

const linksData = [
  {
    title: "Banner",
    caption: "quasar.dev",
    icon: "school",
    link: "#banner",
  },
  {
    title: "Sobre",
    caption: "github.com/quasarframework",
    icon: "code",
    link: "#sobre",
  },
  {
    title: "Skills",
    caption: "chat.quasar.dev",
    icon: "chat",
    link: "#skills",
  },
  {
    title: "Contatos",
    caption: "forum.quasar.dev",
    icon: "record_voice_over",
    link: "#contatos",
  }
];

export default {
  name: "MainLayout",
  components: { EssentialLink },
  data() {
    return {
      leftDrawerOpen: false,
      essentialLinks: linksData,
    };
  },
};
</script>
