<template>
    <div class="clients">
      <div class="container">
        <h3 class="clients__title">Нам доверяют</h3>
        <div class="carousel">
          <VueSlickCarousel
            :arrows="true"
            :dots="true"
            v-bind="settings"
          >
            <div class="carousel__item"><div class="carousel__wrapper"><img src="@/static/clients/tmk-logo.png" /></div></div>
            <div class="carousel__item"><div class="carousel__wrapper"><img src="@/static/clients/nbd-logo.png" /></div></div>
            <div class="carousel__item"><div class="carousel__wrapper"><img src="@/static/clients/ozon-logo.png" /></div></div>
            <div class="carousel__item"><div class="carousel__wrapper"><img src="@/static/clients/sadko-logo.png" /></div></div>
            <div class="carousel__item"><div class="carousel__wrapper"><img src="@/static/clients/tmk-logo.png" /></div></div>
            <div class="carousel__item"><div class="carousel__wrapper"><img src="@/static/clients/nbd-logo.png" /></div></div>
            <div class="carousel__item"><div class="carousel__wrapper"><img src="@/static/clients/ozon-logo.png" /></div></div>
            <div class="carousel__item"><div class="carousel__wrapper"><img src="@/static/clients/sadko-logo.png" /></div></div>
          </VueSlickCarousel>
        </div>
        <div class="clients__side">
          <p class="clients__more">Все наши клиенты</p>
        </div>
      </div>
    </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel';
import 'vue-slick-carousel/dist/vue-slick-carousel.css';
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
export default {
    name: "IndexClients",
    components: {
      VueSlickCarousel,
    },
  data() {
    return {
      settings: {
        "dots": true,
        "infinite": false,
        "speed": 500,
        "slidesToShow": 4,
        "slidesToScroll": 4,
        "initialSlide": 0,
        "responsive": [
          {
            "breakpoint": 1140,
            "settings": {
              "slidesToShow": 2,
              "slidesToScroll": 2,
              "infinite": true,
              "dots": true
            }
          },
          {
            "breakpoint": 768,
            "settings": {
              "slidesToShow": 1,
              "slidesToScroll": 1,
              "infinite": true,
              "dots": true
            }
          },
        ]
      }
    }
  }
}
</script>

<style lang="scss">
.carousel {
  &__wrapper {
    margin: 0px 20px;
  }
  &__item {
    margin-bottom: 30px;
    & img {
      height: 250px;
      width: 100%;
      object-fit: contain;
      pointer-events: none;
    }
  }
}

.slick-dots {
  bottom: 0;
  & .slick-active {
    & button {
      background: $green;
    }
  }
  & li {
    & button {
      width: 23px;
      height: 23px;
      border-radius: 50%;
      border: 2px solid $green;
      &:before {
        display: none;
      }
    }
  }
}

.clients {
  /*padding: 30px;*/
  &__side {
    margin-top: 30px;
    display: flex;
    justify-content: center;
    @media screen and (min-width:1140px) {
      justify-content: flex-end;
    }
  }
  &__more {
    color: $green;
    text-decoration: underline;
    cursor: pointer;
    display: inline-flex;
  }
  &__title {
    font-size: $big;
    font-weight: bold;
    @media screen and (min-width:1140px) {
      font-size: $biggest;
    }
  }
}
</style>
