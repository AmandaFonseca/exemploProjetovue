<template>
  <q-page class="flex-center">
    <div id="q-app">
      <section id="banner" class="section hero is-primary is-fullheight">
        <div class="q-gutter-md">
          <div class="row justify-between">
            <q-parallax id="parallax" src="../assets/computer.jpg">
              <div class="rise-text">
                <h1>Amanda Fonseca</h1>
                <h6>
                  <strong>Desenvolvedora de front-end/ Web design</strong>
                </h6>
              </div>
            </q-parallax>
          </div>
        </div>
      </section>
    </div>

    <div id="q-app">
      <section id="sobre" class="section hero is-primary is-fullheight">
        <div class="column" style="">
          <div class="col col-sub-titulo">
            <img class="sub-titulo" src="../assets/logoamandadefinition.png" />
            <h3 class="titulo">Sobre</h3>
          </div>
        </div>

        <div class="q-col-gutter-md row items-start">
          <div class="col-6">
            <div class="box">
              <q-img
                src="../assets/formatura.jpg"
                class="eu-photo"
                style="border-radius: 50%"
              >
                <div class="absolute-bottom text-subtitle1 text-center">
                  <small> Formatura Análise de sistemas</small>
                </div>
              </q-img>
            </div>
          </div>

          <div class="col-6" id="texto">
            <h3>Amanda Fonseca</h3>

            <p>
              Programadora e desenvolvedora há mais de 3 anos atuando
              diretamente no mercado.
            </p>

            <p>
              Comecei minha carreira no mercado de T.I dando suporte telefônico
              aos usuários de um CRM voltado para a área de saúde quando fui
              descobrir um novo passatempo/fonte de renda: O desenvolvimento de
              códigos.
            </p>

            <p>
              Esse primeiro emprego foi a porta de entrada para esse novo e até
              então desconhecido mundo, a partir daí comecei a desenvolver
              Websites, Aplicativos, Sistemas, e assim fui adquirindo
              conhecimento em linguagens de programação, metodologias e
              paradigmas hoje utilizadas no mercado.
            </p>

            <p>
              Participei do desenvolvimento de formulários que usam inteligência
              artificial, landing pages, web forms e diversas aplicações.
            </p>

            <p>
              Gosto de desafios, de aprender novas tecnologias, desenvolver meus
              códigos ao som de uma playlist bem maluca que vai de Jimmy hendrix
              a Bruno e Marrone.
            </p>
          </div>
        </div>
      </section>
    </div>

    <div id="q-app">
    <section id="skills" class="section hero is-primary is-fullheight">
      <div class="column" style="">
        <div class="col col-sub-titulo">
          <img class="sub-titulo" src="../assets/logoamandadefinition.png" />
          <h3 class="titulo">Skills</h3>
        </div>

        <div class="row row-card">
          <div
            v-for="(card, index) in cards"
            :key="index"
            :ref="`card_${index}`"
            @mouseover="hoverCard(index)"
            @mouseout="hoverCard(-1)"
          >
            <template v-if="index <= 3">
              <div class="col card">
                <a :href="card.site" target="_blank">
                  <img
                    class="card-image"
                    :class="{ selected: isSelected(index) }"
                    :src="card.image"
                  />
                </a>

                <div class="card-footer">
                  <h3 class="card-title">{{ card.title }}</h3>
                  <p class="card-text">
                    by
                    <span
                      class="card-site"
                      :class="{ selected: isSelected(index) }"
                      >{{ card.site }}</span
                    >
                  </p>
                </div>
              </div>
            </template>
          </div>
        </div>

        <div class="row row-card">
          <div
            v-for="(card, index) in cards"
            :key="index"
            :ref="`card_${index}`"
            @mouseover="hoverCard(index)"
            @mouseout="hoverCard(-1)"
          >
            <template v-if="index > 3 && index <= 6">
              <div class="col card">
                <a :href="card.site" target="_blank">
                  <img
                    class="card-image"
                    :class="{ selected: isSelected(index) }"
                    :src="card.image"
                  />
                </a>

                <div class="card-footer">
                  <h3 class="card-title">{{ card.title }}</h3>
                  <p class="card-text">
                    by
                    <span
                      class="card-site"
                      :class="{ selected: isSelected(index) }"
                      >{{ card.site }}</span
                    >
                  </p>
                </div>
              </div>
            </template>
          </div>
        </div>
      </div>
    </section>
    </div>


    <div id="q-app">
      <section id="contatos" class="section hero is-primary is-fullheight">


        <div class="row">
          <div class="col">
            <q-card
              class="my-card text-white"
              style="
                background: #ff9999;
              "
            >
                    <div class="column" style="">
          <div class="col col-sub-titulo">
            <img class="sub-titulo" src="../assets/logoamandadefinition.png" />
            <h3 class="titulo">Contatos</h3>
          </div>
        </div>
              <q-card-section class="center">
                <div class="text-h6">Envie uma mensagem</div>
                <div class="text-subtitle2">
                  <a style="color: white; text-decoration: none; font-size: 17px;" href="https://wa.me/5521982994565" target="_blank">
										WhatsApp: (11) 989743490
									</a></br>
                  <span style="font-size: 13px;">
										amandafonseca207@gmail.com
									</span>
                </div>
              </q-card-section>

              <q-card-section class="q-pt-none">
                {{ lorem }}
              </q-card-section>
            </q-card>
          </div>
        </div>
        
      </section>
    </div>


    <div id="q-app">
      <section id="contatos" class="section hero is-primary is-fullheight">


        <div class="row">
          <div class="col" style=" background: radial-gradient(circle, rgb(255 153 153) 0%, #cc005291 100%);" >
          <footer class="site-footer">
            <div class="container">
              <div class="row">
                    <div class="col-md-8 col-sm-6 col-xs-12">
                      <p class="copyright-text">Copyright &copy; 2020 All Rights Reserved by 
                  <a href="#" style="color:white">amandafonseca.github.io</a>.
                      </p>
                    </div>

                    <div class="col-md-4 col-sm-6 col-xs-12">
                      <ul class="social-icons">
                        <li><a class="whatsap" href="https://api.whatsapp.com/send?phone=5511989743490" target="_blank"><i class="fa fa-whatsapp"></i></a></li>
                        <li><a class="instagram" href="#"><i class="fa fa-instagram" target="_blank"></i></a></li>
                        <li><a class="linkedin" href="https://www.linkedin.com/in/amanda-fonseca-12b578101/" target="_blank"><i class="fa fa-linkedin"></i></a></li> 
                        <li><a class="github" href="https://github.com/AmandaFonseca" target="_blank"><i class="fa fa-github"></i></a></li>     
                      </ul>
                    </div>
              </div>
            </div>
          </footer>

          </div>
        </div>
        
      </section>
    </div>


  </q-page>
</template>


<style scoped>
@-webkit-keyframes rise {
  0% {
    padding-top: 100%;
  }
  60% {
    padding-top: 0.5%;
  }
  80% {
    padding-top: 0.5%;
    border-bottom: 0px solid black;
    opacity: 0.5;
    text-shadow: 2px 2px 5px black;
  }
  100% {
    padding-top: 0.5%;
    border-bottom: 0.35em solid black;
    opacity: 1;
    text-shadow: 0;
  }
}

@keyframes rise {
  0% {
    padding-top: 100%;
  }
  60% {
    padding-top: 0.5%;
  }
  80% {
    padding-top: 0.5%;
    opacity: 0.5;
    text-shadow: 2px 2px 200px rgba(255, 255, 255, 1);
  }
  100% {
    padding-top: 0.5%;
    opacity: 1;
    text-shadow: 200px 200px 200px rgba(255, 255, 255, 0);
  }
}

.rise-text {
  position: relative;
  text-align: center;
  margin: auto;
  opacity: 0;
  padding-top: 100%;
  color: black;
  border-bottom: 0;
  text-shadow: 2px 2px 5px black;
  font-family: Trebuchet MS, sans-serif;
  font-size: 6em;
  font-weight: normal;
  -webkit-animation-name: rise;
  -webkit-animation-duration: 10s;
  -webkit-animation-delay: 1s;
  -webkit-animation-iteration-count: 1;
  -webkit-animation-timing-function: cubic-bezier(0, 0.25, 0.55, 1);
  -webkit-animaiton-fill-mode: forwards;
  animation-name: rise;
  animation-duration: 2s;
  animation-delay: 1s;
  animation-iteration-count: 1;
  animation-timing-function: cubic-bezier(0, 0.25, 0.55, 1);
  animation-fill-mode: forwards;
}

.q-img__image.absolute-full {
  border-radius: 50%;
}
.box {
  width: 65%;
  margin: auto;
}

.col.col-sub-titulo {
  margin: auto;
}
img.sub-titulo {
  float: left;
}
h3.titulo {
  float: right;
}
.card-row {
  display: flex;
  justify-content: center;
  align-items: center;
  min-width: 780px;
  width: 100%;
  height: 500px;
}

.card {
  position: relative;
  background-color: #ffffff;
  height: 370px;
  width: 240px;
  margin: 10px;
  overflow: hidden;
  box-shadow: 0px 2px 4px 0px rgba(0, 0, 0, 0.5);
  transition: height 0.3s, box-shadow 0.3s;
}

.card:hover {
  height: 410px;
  box-shadow: 20px 20px 40px 0px rgba(0, 0, 0, 0.5);
}

.card-image {
  /* center horizontally overflown image */
  position: absolute;
  left: -9999px;
  right: -9999px;
  margin: auto;

  height: 220px;
  min-width: 100%;
  transition: height 0.3s, opacity 0.3s;
}
.card-image.selected {
  height: 410px;
  opacity: 0.3;
}
.card-footer {
  position: absolute;
  bottom: 0;
  height: 130px;
  padding: 10px 15px;
  font-family: Helvetica;
}

.card-text {
  font-size: 14px;
  color: rgba(0, 0, 0, 0.7);
}
.card-title {
  font-family: Serif;
}
.card-site {
  font-size: 14px;
  color: #bab096;
  transition: color 0.3s;
}
.card-site.selected {
  color: #6a6456;
}
.center.q-card__section.q-card__section--vert {
  text-align: center;
}

.site-footer {
  color: white;
  padding: 25px 0 20px;
  font-size: 15px;
  line-height: 24px;
}
.site-footer hr {
  border-top-color: #bbb;
  opacity: 0.5;
}
.site-footer hr.small {
  margin: 20px 0;
}
.site-footer h6 {
  color: #fff;
  font-size: 16px;
  text-transform: uppercase;
  margin-top: 5px;
  letter-spacing: 2px;
}
.site-footer a {
  color: #737373;
}
.site-footer a:hover {
  color: #3366cc;
  text-decoration: none;
}
.footer-links {
  padding-left: 0;
  list-style: none;
}
.footer-links li {
  display: block;
}
.footer-links a {
  color: #737373;
}
.footer-links a:active,
.footer-links a:focus,
.footer-links a:hover {
  color: #3366cc;
  text-decoration: none;
}
.footer-links.inline li {
  display: inline-block;
}
.site-footer .social-icons {
  text-align: right;
}
.site-footer .social-icons a {
  width: 40px;
  height: 40px;
  line-height: 40px;
  margin-left: 6px;
  margin-right: 0;
  border-radius: 100%;
  background-color: #ff9999;
}
.copyright-text {
  margin: 0;
}



@media (max-width: 762px) {
  .row > .col-6,
  .row > .col-xs-6 {
    height: auto;
    width: 100%;
  }
  div#texto {
    text-align: center;
  }
  .row.row-card {
    margin: auto;
    width: 50%;
}
}

@media (min-width: 991px) {
  .row.row-card {
    margin: auto;

}

  div#texto {
    text-align: initial;
    padding-left: 1em;
    padding-right: 1em;
  }
}
@media (max-width: 991px) {
  .site-footer [class^="col-"] {
    margin-bottom: 30px;
  }
}
@media (max-width: 767px) {
  .site-footer {
    padding-bottom: 0;
  }
  .site-footer .copyright-text,
  .site-footer .social-icons {
    text-align: center;
  }
}
.social-icons {
  padding-left: 0;
  margin-bottom: 0;
  list-style: none;
}
.social-icons li {
  display: inline-block;
  margin-bottom: 4px;
}
.social-icons li.title {
  margin-right: 15px;
  text-transform: uppercase;
  color: #96a2b2;
  font-weight: 700;
  font-size: 13px;
}
.social-icons a {
  background-color: #eceeef;
  color: white;
  font-size: 16px;
  display: inline-block;
  line-height: 44px;
  width: 44px;
  height: 44px;
  text-align: center;
  margin-right: 8px;
  border-radius: 100%;
  -webkit-transition: all 0.2s linear;
  -o-transition: all 0.2s linear;
  transition: all 0.2s linear;
}
.social-icons a:active,
.social-icons a:focus,
.social-icons a:hover {
  color: #fff;
  background-color: #29aafe;
}
.social-icons.size-sm a {
  line-height: 34px;
  height: 34px;
  width: 34px;
  font-size: 14px;
}
.social-icons a.facebook:hover {
  background-color: #3b5998;
}
.social-icons a.twitter:hover {
  background-color: #00aced;
}
.social-icons a.linkedin:hover {
  background-color: #007bb6;
}
.social-icons a.dribbble:hover {
  background-color: #ea4c89;
}
@media (max-width: 767px) {
  .social-icons li.title {
    display: block;
    margin-right: 0;
    font-weight: 600;
  }
}
.col-md-8.col-sm-6.col-xs-12 {
  float: left;
}
</style>

<script lang="ts">
const cards = [
  {
    title: "CSS3",
    site: "https://www.w3.org/Style/CSS/Overview.en.html",
    image:
      "data:image/png;base64,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",
  },
  {
    title: "Javascript",
    site: "https://developer.mozilla.org/pt-BR/docs/Web/JavaScript",
    image:
      "data:image/png;base64,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x9tY/kLAy2vy91CqB8Hhh7pMvbSUT5xWjO/3/bTNcTJXjXjksTZ+dn8rb2yMcjpZeW98H0YcaDjj5Difu7iCQw708368SsFSsBSs/zhlM4SRZdnKLp54uoNX1iR54umA9Ztye1hnnuRy2EifD48u4MTjChlc7ZHu5cnG+Rr5eJ6huSVk2QtdPLO0g7UbAla+FPDcin2rymknuowa4TFqRJwTxhQy4uDYHk8iV7AULAWrj55wtztcm+sD3qwL2FiXZtOWgDfr0qzfGPLaGyErXrZE3ef8jTzIcPBwhwOHe7xvqMfgWo8DBvsMHexxwBCf0hKHILT77Z0yYzIxDkJLfWPIlvqAzVsDNm8J2NKQeYzrNoSsXR++5cTmIw41HDTc5cD3uRwwxKe22mNorUdtTeb/QeUuYWT7JFQKloKlYGUzrTJgHEMQWJKpzL902hIEmfjYHt/nupkD3zHfEI8ZYt3XfLJ2YC2WzFx9IXOfkklLKp35l05nohPZ7jttMi9/x8nEzvcgFjPEYw5+96fW99djU7CymCVoE7x3RRYILcZAIm5IxHu/3wzUdUfW7pq2+b7B9w1F2W4XrakauH9ktQlERMESEVGwRETBEhFRsEREFCwRUbBERBQsEREFS0QULBERERERERERERERERERERERERERERGR/vf/VqxZsetObqQAAAAASUVORK5CYII=",
  },
  {
    title: "Git",
    site: "https://git-scm.com/",
    image:
      "data:image/png;base64,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",
  },
  {
    title: "Node js",
    site: "https://nodejs.org/",
    image:
      "data:image/png;base64,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",
  },
  {
    title: "Mysql",
    site: "https://www.mysql.com/",
    image:
      "data:image/png;base64,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",
  },
  {
    title: "Webpack",
    site: "https://webpack.js.org/",
    image:
      "data:image/png;base64,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",
  },
  {
    title: "Vue.js",
    site: "https://vuejs.org/",
    image:
      "data:image/png;base64,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",
  },
];

import { Todo, Meta } from "components/models";
import ExampleComponent from "components/CompositionComponent.vue";
import { defineComponent, ref } from "@vue/composition-api";
import { TweenMax } from "gsap";

export default defineComponent({
  data() {
    return {
      cards: cards,
      selectedCard: -1,
    };
  },
  methods: {
    hoverCard(selectedIndex) {
      this.selectedCard = selectedIndex;
      this.animateCards();
    },
    animateCards() {
      this.cards.forEach((card, index) => {
        const direction = this.calculateCardDirection(index, this.selectedCard);
        TweenMax.to(this.$refs[`card_${index}`], 0.3, { x: direction * 50 });
      });
    },
    calculateCardDirection(cardIndex, selectedIndex) {
      if (selectedIndex === -1) {
        return 0;
      }

      const diff = cardIndex - selectedIndex;
      return diff === 0 ? 0 : diff / Math.abs(diff);
    },
    isSelected(cardIndex) {
      return this.selectedCard === cardIndex;
    },
  },

  name: "PageIndex",
  components: { ExampleComponent },
  setup() {
    const todos = ref<Todo[]>([
      {
        id: 1,
        content: "ct1",
      },
      {
        id: 2,
        content: "ct2",
      },
      {
        id: 3,
        content: "ct3",
      },
      {
        id: 4,
        content: "ct4",
      },
      {
        id: 5,
        content: "ct5",
      },
    ]);
    const meta = ref<Meta>({
      totalCount: 1200,
    });
    return { todos, meta };
  },
});
</script>
