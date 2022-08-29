<template>
    <div class="consultation">
      <div class="container">
        <div class="consultation-main">
          <div class="consultation-offer">
            <div class="consultation-list">
              <div class="consultation-list__item item-list">
                <img src="@/static/consultation/ico_1.png" alt="" class="item-list__ico">
                <div class="item-list__content">
                  <p class="item-list__title">Консультация</p>
                  <p class="item-list__side">
                    Определяем перспективы в конкретном случае
                    и подбираем для Вас
                    оптимальные варианты размещения и оформления
                    рекламной или информационной конструкции
                  </p>
                </div>
              </div>
              <div class="consultation-list__item item-list">
                <img src="@/static/consultation/ico_2.png" alt="" class="item-list__ico">
                <div class="item-list__content">
                  <p class="item-list__title">Подготовка</p>
                  <p class="item-list__side">
                    Подготавливаем необходимые документы,
                    заявления и фотоматериалы, разрабатываем эскизы,
                    дизайн-проекты и технические расчеты
                  </p>
                </div>
              </div>
              <div class="consultation-list__item item-list">
                <img src="@/static/consultation/ico_3.png" alt="" class="item-list__ico">
                <div class="item-list__content">
                  <p class="item-list__title">Согласование</p>
                  <p class="item-list__side">
                    Согласовываем документы в нужных инстанциях,
                    проходим необходимые процедуры,
                    при необходимости вносим правки.
                    Передаем Вам согласованные документы
                  </p>
                </div>
              </div>
            </div>
            <p class="consultation__more">Подробнее о согласовании наружной рекламы</p>
          </div>
          <div class="consultation-form">
            <p class="consultation-form__title">Беплатная консультация</p>
            <div class="consultation-form__list">
              <div class="consultation-form__item">
                <BaseInput placeholder="Имя"/>
              </div>
              <div class="consultation-form__item">
                <BaseInput placeholder="Телефон"/>
              </div>
              <div class="consultation-form__item">
                <BaseInput placeholder="Email"/>
              </div>
              <div class="consultation-form__item">
                <BaseInput placeholder="Адрес объекта"/>
              </div>
            </div>
            <div class="consultation-form__textarea">
              <BaseTextarea
                placeholder="Предпологаемое место расположения информационной и\или рекламной конструкции"
                />
            </div>
            <div class="consultation-form__button">
              <p class="consultation-form__text">Выбрать файл</p>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
    import BaseInput from "~/components/common/BaseInput";
    import BaseTextarea from "~/components/common/BaseTextarea";
    export default {
        name: "IndexConsultation",
      components: {BaseTextarea, BaseInput}
    }
</script>

<style lang="scss" scoped>
.item-list {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin-top: 30px;
  &__content {
    @media screen and (min-width:1140px) {
      margin-left: 13px;
    }
  }
  &__ico {
    @media screen and (min-width:1140px) {
      transform: translateY(-30%);
    }
  }
  @media screen and (min-width:1140px) {
    flex-direction: row;
    align-items: flex-start;
    text-align: left;
  }
  &:first-child {
    margin-top: 0;
  }
  &__title {
    font-size: $medium;
  }
  &__side {
    margin-top: 15px;
  }
}

.consultation {
  padding: 30px 0;
  &__more {
    color: $green;
    text-decoration: underline;
    text-align: center;
    margin-top: 30px;
    @media screen and (min-width:1140px) {
      text-align: left;
      margin-top: 132px;
    }
  }
  &-main {
    @media screen and (min-width:1140px) {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
  }
  &-form {
    border: 1px solid $green;
    margin-top: 30px;
    padding: 38px;
    text-align: center;
    @media screen and (min-width:1140px) {
      min-width: 462px;
      margin-left: 50px;
    }
    &__button {
      margin-top: 45px;
      background: #E3E3E3;
      display: flex;
      justify-content: flex-end;
    }
    &__text {
      padding: 16px 18px;
      color: #636363;
      background: #C4C4C4;
    }
    &__item {
      display: flex;
      margin-top: 45px;
      &:first-child {
        margin-top: 53px;
      }
    }
    &__textarea {
      display: flex;
      margin-top: 45px;
    }
    &__title {
      font-size: $big;
      padding-bottom: 26px;
      border-bottom: 1px solid $green;
    }
  }
}
</style>
