<template>
    <div class="reviews">
      <div class="container">
        <h3 class="reviews__title">Отзывы:</h3>
        <div class="carousel">
          <VueSlickCarousel
            :arrows="true"
            :dots="true"
            v-bind="settings"
          >
            <div class="carousel__item">
              <div class="review">
                <p class="review__title">
                  Владимир Александрович, Директор. ООО "ПРОСТО"
                </p>
                <p class="review__text">
                  Благодарю за проделанную раньше оговоренного срока работу!
                  За согласование наружной рекламы в центре города в разгар проведения Ч.М. по футболу!
                  Уверен, что при появлении новых задач по согласованию рекламы - обращусь к Вам!
                </p>
              </div>
              <div class="review">
                <p class="review__title">
                  Ислентьев Роман, Руководитель отдела маркетинга. Группа компаний "Недвижимость бизнеса"
                </p>
                <p class="review__text">
                  Благодарим "АРП Символ" за оперативное пересогласование рекламной конструкции
                  с банером и вывески на нашем логистическом комплексе.
                  Истек срок паспортов и пришло уведомление о демонтаже. Буквально спасли!
                </p>
              </div>
            </div>
            <div class="carousel__item">
              <div class="review">
                <p class="review__title">
                  Владимир Александрович, Директор. ООО "ПРОСТО"
                </p>
                <p class="review__text">
                  Благодарю за проделанную раньше оговоренного срока работу!
                  За согласование наружной рекламы в центре города в разгар проведения Ч.М. по футболу!
                  Уверен, что при появлении новых задач по согласованию рекламы - обращусь к Вам!
                </p>
              </div>
              <div class="review">
                <p class="review__title">
                  Ислентьев Роман, Руководитель отдела маркетинга. Группа компаний "Недвижимость бизнеса"
                </p>
                <p class="review__text">
                  Благодарим "АРП Символ" за оперативное пересогласование рекламной конструкции
                  с банером и вывески на нашем логистическом комплексе.
                  Истек срок паспортов и пришло уведомление о демонтаже. Буквально спасли!
                </p>
              </div>
            </div>
          </VueSlickCarousel>
        </div>
        <div class="reviews__side">
          <p class="reviews__more">Все отзывы</p>
        </div>
      </div>
    </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel';
import 'vue-slick-carousel/dist/vue-slick-carousel.css';
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
  export default {
    name: "IndexReviews",
    components: {
      VueSlickCarousel,
    },
  }
</script>

<style lang="scss" scoped>
.carousel {
  margin-top: 30px;
  &__item {
    margin-bottom: 50px;
  }
}

.review {
  margin-top: 45px;
  &:first-child {
    margin-top: 0;
  }
  &__title {
    color: $green;
    font-weight: bold;
    font-size: $normal;
  }
  &__text {
    margin-top: 16px;
  }
}

.reviews {
  &__title {
    font-size: $big;
    font-weight: bold;
    @media screen and (min-width:1140px) {
      font-size: $biggest;
    }
  }
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
}
</style>
