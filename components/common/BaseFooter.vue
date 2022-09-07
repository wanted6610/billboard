<template>
  <div class="footer-wrapper">
    <footer class="footer">
      <div class="container">
        <div class="footer-content">
          <div class="footer-copy">
            <p class="footer-copy__title">АРП СИМВОЛ © 2017-2022</p>
            <p class="footer-copy__side">
              Копирование любых материалов
              и информации с сайта запрещено
              и охраняется авторским правом.
            </p>
          </div>
          <div class="footer-goods">
            <p class="footer-goods__title">НАШИ УСЛУГИ:</p>
            <div class="footer-goods__list">
              <p class="footer-goods__item">Согласование рекламы и информации</p>
              <p class="footer-goods__item">Разработка технической документации</p>
              <p class="footer-goods__item">
                Разработка концепций
                (дизайн-проектов комплексного оформлениия)
              </p>
              <p class="footer-goods__item">Изготовление и монтаж рекламных конструкций</p>
            </div>
          </div>
          <div class="footer-address">
            <p class="footer-address__title">ул. Ильинская, д. 29, оф. 1</p>
            <p class="footer-address__phone">+7 (831) 4300-006</p>
            <p class="footer-address__mail">info@reklama-soglasovanie.ru</p>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
    export default {
        name: "BaseFooter"
    }
</script>

<style lang="scss" scoped>
.footer {
  &-wrapper {
    border-top: 2px solid $green;
  }
  max-width: 1512px;
  margin: 0 auto;
  padding: 30px 0;
  width: 100%;
  position: relative;
  @media screen and (min-width:1140px) {
    padding: 52px 0;
  }
  &-content {
    text-align: center;
    @media screen and (min-width:1140px) {
      display: flex;
      text-align: left;
      justify-content: space-between;
      align-items: flex-start;
    }
  }
  &-copy {
    &__title {
      font-size: $medium;
      margin-bottom: 14px;
      font-weight: bold;
    }
    @media screen and (min-width:1140px) {
      max-width: 340px;
    }
  }
  &-goods {
    margin-top: 30px;
    &__title {
      margin-bottom: 14px;
      font-weight: bold;
    }
    @media screen and (min-width:1140px) {
      max-width: 483px;
      margin: 0 20px 0;
    }
  }
  &-address {
    margin-top: 30px;
    &__title {
      margin-bottom: 14px;
    }
    @media screen and (min-width:1140px) {
      margin-top: 0;
    }
  }
}
</style>
