<template>
  <div class="home">
    <section class="hero">
      <v-container>
        <v-row no-gutters>
          <v-col md="3" offset-md="1" class="bg-symbol-1 mt-12">
            <h4
              v-scroll-reveal.reset="revealFromBottom"
              class="overline mb-4 mb-5"
            >
              Aluguel para Temporada
            </h4>
            <h1
              v-scroll-reveal.reset="revealFromBottom"
              class="display-1 font-weight-medium"
            >
              Seu cantinho em Bonito/MS para descansar tranquilo
            </h1>
            <v-btn
              v-scroll-reveal="revealFromBottomAt400"
              rounded
              height="auto"
              color="primary"
              class="px-10 py-4 mt-10"
              depressed
            >
              <v-icon left>mdi-hand-pointing-right</v-icon> Reservar
            </v-btn>
          </v-col>
          <v-col md="6" offset-md="2">
            <div
              v-scroll-reveal.reset="revealPointedImg1"
              class="pointed-img-wrap mb-12 mb-md-0"
            >
              <v-img
                :src="require('~/assets/images/fachada/20220223_102950.jpg')"
                class="pointed-img left"
              ></v-img>
            </div>
          </v-col>
        </v-row>
      </v-container>
      <div
        v-scroll-reveal.reset="revealFromRight"
        class="d-none d-md-block dots-map"
      ></div>
    </section>

    <section class="py-12 mt-12">
      <v-container>
        <v-row>
          <v-col offset="2" offset-sm="0" sm="6" md="3">
            <div
              v-scroll-reveal.reset="revealFromRightWithDelay(100)"
              class="icon-box active"
            >
              <div class="icon-box__icon mb-7">
                <v-icon x-large>mdi-leaf</v-icon>
              </div>
              <h4 class="title">
                Aproveite Bonito/MS e durma por um preço justo
              </h4>
            </div>
          </v-col>
          <v-col offset="2" offset-sm="0" sm="6" md="3">
            <div
              v-scroll-reveal.reset="revealFromRightWithDelay(200)"
              class="icon-box"
            >
              <div class="icon-box__icon mb-7">
                <v-icon x-large>mdi-flower-tulip-outline</v-icon>
              </div>
              <h4 class="title">Quartos para temporada construídos em 2022</h4>
            </div>
          </v-col>
          <v-col offset="2" offset-sm="0" sm="6" md="3">
            <div
              v-scroll-reveal.reset="revealFromRightWithDelay(300)"
              class="icon-box"
            >
              <div class="icon-box__icon mb-7">
                <v-icon x-large>mdi-sprout-outline</v-icon>
              </div>
              <h4 class="title">Tudo novinho e limpinho para você</h4>
            </div>
          </v-col>
          <v-col offset="2" offset-sm="0" sm="6" md="3">
            <div
              v-scroll-reveal.reset="revealFromRightWithDelay(400)"
              class="icon-box"
            >
              <div class="icon-box__icon mb-7">
                <v-icon x-large>mdi-flower-outline</v-icon>
              </div>
              <h4 class="title">Copa completa, tanque e varal</h4>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section class="py-12">
      <v-container>
        <v-row align="center" no-gutters>
          <v-col lg="12">
            <div
              v-scroll-reveal.reset="revealPointedImg1"
              class="pointed-img-wrap mb-12 mb-md-0"
            >
              <v-carousel>
                <v-carousel-item
                  v-for="(item, i) in items"
                  :key="i"
                  :src="item.src"
                  reverse-transition="fade-transition"
                  transition="fade-transition"
                ></v-carousel-item>
              </v-carousel>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <!-- <section class="py-12">
      <v-container>
        <v-row align="center" no-gutters>
          <v-col lg="6">
            <div
              v-scroll-reveal.reset="revealPointedImg1"
              class="pointed-img-wrap mb-12 mb-md-0"
            >
              <v-img
                :src="require('~/assets/images/fachada/20220223_102950.jpg')"
                class="pointed-img left"
              ></v-img>
            </div>
          </v-col>
          <v-col lg="6" class="bg-symbol-2">
            <h4 v-scroll-reveal.reset="revealFromBottom" class="overline mb-4">
              Premium Coffee
            </h4>
            <h5 v-scroll-reveal.reset="revealFromBottom" class="display-2">
              Quality coffee <br />
              cultivated by Good
            </h5>
            <p
              v-scroll-reveal.reset="revealFromBottom"
              class="title font-weight-regular py-5 pr-10"
            >
              Our love for specialty coffee is never-ending. With over 365 days
              a year oat origin working with the best growers on the planet,
              only the best beans make the grade.
            </p>
            <v-btn
              v-scroll-reveal.reset="revealFromBottomAt400"
              rounded
              height="auto"
              color="primary"
              class="px-10 py-4"
              depressed
            >
              <v-icon left>mdi-hand-pointing-right</v-icon> Shop now
            </v-btn>
          </v-col>
        </v-row>
      </v-container>
    </section> -->

    <section class="shop amber lighten-5 py-12 my-12 text-center">
      <div class="shop__header mx-auto my-12 py-12">
        <h2 v-scroll-reveal.reset="revealFromBottom" class="overline mb-4">
          Por que ficar conosco?
        </h2>
        <h1 v-scroll-reveal.reset="revealFromBottom" class="display-1">
          Nossos diferenciais
        </h1>
      </div>
      <v-container>
        <v-row justify="center">
          <v-col v-for="card in cards" :key="card.id">
            <v-card color="primary" class="ma-4" height="200" width="300">
              <v-row class="fill-height" align="center" justify="center">
                <v-card-title class="font-weight-black">
                  {{ card.title }}
                </v-card-title>
                <v-card-text class="font-weight-light mx-2">
                  {{ card.description }}
                </v-card-text>
              </v-row>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section class="gallery pt-0 pt-md-12 text-center">
      <div class="gallery__header mx-auto bg-symbol-2 pt-0 pt-md-12 pb-2 my-12">
        <h1
          v-scroll-reveal.reset="revealFromBottom"
          class="display-2 font-weight-black"
        >
          Localização
        </h1>
        <p
          v-scroll-reveal.reset="revealFromBottom"
          class="mx-auto title font-weight-regular mt-2 mb-12"
        >
          Rua Luiz Da Costa Leite, 444, Bonito;MS
        </p>
      </div>
      <v-row no-gutters>
        <v-col>
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3738.626422359317!2d-54.57885428444837!3d-20.4394489863206!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x9486e8f75f9a4e01%3A0xe20e685d40e22b3a!2sR.%20Mario%20de%20Andrade%2C%20473%20-%20Vila%20do%20Polones%2C%20Campo%20Grande%20-%20MS%2C%2079032-260!5e0!3m2!1spt-BR!2sbr!4v1646456437075!5m2!1spt-BR!2sbr"
            width="600"
            height="450"
            style="border: 0"
            allowfullscreen=""
            loading="lazy"
          ></iframe>
        </v-col>
      </v-row>
    </section>

    <!-- <section class="shop amber lighten-5 py-12 my-12 text-center">
      <v-container>
        <div class="shop__header mx-auto my-12 py-12 bg-symbol-1">
          <h2 v-scroll-reveal.reset="revealFromBottom" class="overline mb-4">
            Reviews
          </h2>
          <h1 v-scroll-reveal.reset="revealFromBottom" class="display-1">
            Opinião de nossos clientes
          </h1>
          <p
            v-scroll-reveal.reset="revealFromBottom"
            class="mt-7 title font-weight-regular mb-12"
          >
            Encontre aqui nossos anúncios e  verifique a avaliação dos nossos usuários. Você pode reservar nestes links ou entrar em contato diretamente
          </p>
        </div>
        <v-row align="center" justify="center" no-gutters>
          <v-col cols="12" md="4" class="mb-12 mb-md-0">
            <img
              v-scroll-reveal.reset="revealFromTopWithDelay(100)"
              src="~assets/images/products/amber.png"
              alt=""
            />
            <h4
              v-scroll-reveal.reset="revealFromBottomAt400"
              class="overline my-3"
            >
              
            </h4>
            <h3 v-scroll-reveal.reset="revealFromBottomAt400" class="title">
              
            </h3>
            <v-btn
              v-scroll-reveal.reset="revealFromBottomAt400"
              rounded
              height="auto"
              color="primary"
              class="px-7 py-2 mt-3"
              depressed
            >
              <v-icon left>mdi-hand-pointing-right</v-icon> AirBNB
            </v-btn>
          </v-col>
          <v-col cols="12" md="4" class="mb-12 mb-md-0">
            <img
              v-scroll-reveal.reset="revealFromTopWithDelay(200)"
              src="~assets/images/products/black.png"
              alt=""
            />
            <h4
              v-scroll-reveal.reset="revealFromBottomAt400"
              class="overline my-3"
            >
         
            </h4>
            <h3 v-scroll-reveal.reset="revealFromBottomAt400" class="title">
         
            </h3>
            <v-btn
              v-scroll-reveal.reset="revealFromBottomAt400"
              rounded
              height="auto"
              color="primary"
              class="px-7 py-2 mt-3"
              depressed
            >
              <v-icon left>mdi-hand-pointing-right</v-icon> Booking
            </v-btn>
          </v-col>
          <v-col cols="12" md="4" class="mb-12 mb-md-0">
            <img
              v-scroll-reveal.reset="revealFromTopWithDelay(300)"
              src="~assets/images/products/white.png"
              alt=""
            />
            <h4
              v-scroll-reveal.reset="revealFromBottomAt400"
              class="overline my-3"
            >
           
            </h4>
            <h3 v-scroll-reveal.reset="revealFromBottomAt400" class="title">
            
            </h3>
            <v-btn
              v-scroll-reveal.reset="revealFromBottomAt400"
              rounded
              height="auto"
              color="primary"
              class="px-7 py-2 mt-3"
              depressed
            >
              <v-icon left>mdi-hand-pointing-right</v-icon> WhatsApp
            </v-btn>
          </v-col>
        </v-row>
      </v-container>

      <div class="d-none d-md-block dots-map left"></div>
    </section>

    <section class="py-12 my-12">
      <v-container>
        <v-row align="center" no-gutters>
          <v-col md="6" class="bg-symbol-2">
            <h4 v-scroll-reveal.reset="revealFromBottom" class="overline mb-4">
              Premium Coffee
            </h4>
            <h5 v-scroll-reveal.reset="revealFromBottom" class="display-2">
              The secret lies <br />
              within the bean
            </h5>
            <p
              v-scroll-reveal.reset="revealFromBottom"
              class="title font-weight-regular py-5 pr-10"
            >
              You can't imagine a day without a cup of coffee and we believe
              that your office and on-the-go coffee should never be a
              compromise.
            </p>
            <v-btn
              v-scroll-reveal.reset="revealFromBottomAt400"
              rounded
              height="auto"
              color="primary"
              class="px-10 py-4"
              depressed
            >
              <v-icon left>mdi-hand-pointing-right</v-icon> Shop now
            </v-btn>
          </v-col>
          <v-col md="6">
            <div
              v-scroll-reveal.reset="revealPointedImg2"
              class="pointed-img-wrap mt-12 mt-md-0 left"
            >
              <v-img
                :src="require('~/assets/images/gallery/pic3.jpg')"
                class="pointed-img"
              ></v-img>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </section>

    <section class="gallery pt-0 pt-md-12 text-center">
      <div class="gallery__header mx-auto bg-symbol-2 pt-0 pt-md-12 pb-2 my-12">
        <h1
          v-scroll-reveal.reset="revealFromBottom"
          class="display-2 font-weight-black"
        >
          #NOANSACOFFEE
        </h1>
        <p
          v-scroll-reveal.reset="revealFromBottom"
          class="mx-auto title font-weight-regular mt-2 mb-12"
        >
          Coffee Perfection Since 1927.
        </p>
      </div>
      <v-row no-gutters>
        <v-col v-for="image in gallery" :key="image.id" cols="4" md="2">
          <v-img
            v-scroll-reveal.reset="revealFromRightWithDelay(image.revealDelay)"
            :src="require(`~/assets/images/tipo1/${image.filename}`)"
            aspect-ratio="1"
            class="grey lighten-2"
          ></v-img>
        </v-col>
      </v-row>
    </section> -->

    <section class="grey darken-3 py-12 white--text text-center">
      <v-container class="my-12">
        <h1 class="display-2">Contato</h1>
        <p class="mx-auto mt-5 title font-weight-regular">
          Mande-nos um WhatsApp e iremos te atender
        </p>

        <v-row justify="center" no-gutters>
          <v-col cols="8" md="4">
            <v-btn block color="green ligthen-2">
              <v-icon>mdi-whatsapp</v-icon>
              WhatsApp
            </v-btn>
          </v-col>
        </v-row>
      </v-container>
    </section>
  </div>
</template>

<script>
export default {
  layout: 'landing-page',
  data() {
    return {
      email: '',
      items: [
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
        },
      ],
      revealFromBottom: {
        origin: 'bottom',
        distance: '100%',
      },
      revealFromBottomAt400: {
        origin: 'bottom',
        distance: '100%',
        delay: 400,
      },
      revealFromRight: {
        distance: '100%',
        origin: 'right',
      },
      revealPointedImg1: {
        distance: '30%',
        origin: 'left',
      },
      revealPointedImg2: {
        distance: '30%',
        origin: 'right',
      },

      cards: [
        {
          id: 1,
          title: 'Estacionamento interno',
          color: 'blue lighten-4',
          description:
            '1 vaga de carro para cada apartamento. Portão elétrico acionado manualmente.',
        },
        {
          id: 2,
          color: 'purple lighten-4',
          title: 'Copa completa',
          description:
            'Cozinha equipada com geladeira grande, microondas, cooktop a gás, panelas, frigideiras, chaleira e talheres.',
        },
        {
          id: 3,
          color: 'blue lighten-4',
          title: 'WiFi e SmartTV',
          description: 'TVs com apps Netflix, Youtube, entre outros',
        },
        {
          id: 4,
          color: 'blue lighten-4',
          title: 'Camas grandes',
          description:
            'Colchão tamanho queen com toda roupa de cama e banho inclusa',
        },
        {
          id: 5,
          color: 'green lighten-4',
          title: 'Lave sua roupa',
          description:
            'Todos apartamentos possuem tanque o local para pendurar roupa',
        },
        {
          id: 6,
          color: 'red lighten-4',
          title: 'Ar Condicionado',
          description: 'Ar Split para gelar seu quarto rapidinho',
        },
      ],

      gallery: [
        {
          id: 1,
          filename: '20220222_181618.jpg',
          revealDelay: 100,
        },
        {
          id: 2,
          filename: '20220222_181703.jpg',
          revealDelay: 200,
        },
        {
          id: 3,
          filename: '20220222_181730.jpg',
          revealDelay: 300,
        },
        {
          id: 4,
          filename: '20220222_181703.jpg',
          revealDelay: 400,
        },
        {
          id: 5,
          filename: '20220222_181703.jpg',
          revealDelay: 500,
        },
        {
          id: 6,
          filename: '20220222_181703.jpg',
          revealDelay: 600,
        },
        {
          id: 7,
          filename: '20220222_181703.jpg',
          revealDelay: 700,
        },
        {
          id: 8,
          filename: '20220222_181703.jpg',
          revealDelay: 800,
        },
        {
          id: 9,
          filename: '20220222_181703.jpg',
          revealDelay: 900,
        },
        {
          id: 10,
          filename: '20220222_181703.jpg',
          revealDelay: 1000,
        },
        {
          id: 11,
          filename: '20220222_181703.jpg',
          revealDelay: 1100,
        },
        {
          id: 12,
          filename: '20220222_181703.jpg',
          revealDelay: 1200,
        },
      ],
    }
  },

  methods: {
    revealFromRightWithDelay(delay) {
      return {
        distance: '100%',
        origin: 'right',
        delay,
      }
    },
    revealFromTopWithDelay(delay) {
      return {
        distance: '50%',
        origin: 'top',
        delay,
      }
    },
  },
}
</script>

<style lang="scss">
@import '~vuetify/src/styles/styles.sass';

.bg-symbol-1,
.bg-symbol-2 {
  position: relative;
  z-index: 2;

  &::before {
    background-repeat: no-repeat;
    width: 470px;
    height: 400px;
    content: '';
    z-index: -1;
    position: absolute;
  }

  @media #{map-get($display-breakpoints, 'sm-and-down')} {
    &::before {
      display: none;
    }
  }
}

.bg-symbol-1 {
  &::before {
    background-image: url(~assets/images/symbol-bg1.png);
    top: -75px;
    left: 100px;
    z-index: -1;
  }
}
.bg-symbol-2 {
  &::before {
    background-image: url(~assets/images/symbol-bg2.png);
    top: -125px;
    left: -50px;
  }
}

.hero {
  background-color: #f3f0e6;
  height: 590px;
  padding-top: 85px;
  position: relative;

  .hero__image {
    position: relative;
    top: -117px;
    right: -100px;
  }

  .bg-symbol-1 {
    &::before {
      background-image: url(~assets/images/symbol-bg-hero.png);
      left: -240px;
      top: -135px;
      z-index: -1;
    }
  }
}

.dots-map {
  position: absolute;
  right: 0;
  bottom: -100px;
  height: 205px;
  width: 200px;
  margin-left: auto;
  background-image: url(~assets/images/dots.png);

  &.left {
    right: initial;
    left: 0;
  }
}

.icon-box {
  max-width: 250px;
  margin-right: 20px;
  padding: 40px;
  position: relative;
  overflow: hidden;
  border-radius: 0 60px 0 0;

  .icon-box__icon {
    position: relative;
    z-index: 2;
    padding-top: 25px;
  }

  &:hover {
    background-color: rgba(map-get($amber, 'darken-1'), 0.1);
  }

  &.active {
    background-color: rgba(map-get($amber, 'darken-1'), 0.2);

    &::before {
      content: '';
      position: absolute;
      z-index: 1;
      top: -60px;
      left: -40px;
      width: 125%;
      height: 178px;
      background-color: map-get($amber, 'darken-1');
      border-radius: 50%;
    }
  }
}

.shop {
  position: relative;

  .shop__header {
    width: 60%;

    &::before {
      background-image: url(~assets/images/symbol-bg-shop.png);
    }
  }
}

.pointed-img-wrap {
  position: relative;

  &::before {
    position: absolute;
    left: -50px;
    content: '';
    height: 205px;
    width: 200px;
    background-image: url(~assets/images/dots.png);
  }

  &::after {
    content: '';
    position: absolute;
    bottom: -67px;
    right: 130px;
    width: 40px;
    height: 200px;
    background-color: rgba(map-get($amber, 'darken-1'), 0.7);
    border-radius: 20px;
    transform: rotate(45deg);

    @media #{map-get($display-breakpoints, 'sm-and-down')} {
      display: none;
    }
  }

  .pointed-img {
    height: 470px;
    width: 470px;
    border-radius: 50% 50% 0 50%;
  }

  &.left {
    .pointed-img {
      border-radius: 50% 50% 50% 0;
    }

    &::before {
      left: initial;
      right: 55px;
    }

    &::after {
      transform: rotate(-45deg);
      right: initial;
      left: 20px;
    }
  }
}

.gallery {
  .gallery__header {
    width: 30%;

    @media #{map-get($display-breakpoints, 'sm-and-down')} {
      width: 100%;
    }
  }
}
</style>
