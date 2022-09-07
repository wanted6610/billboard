<template>
    <div class="offer">
      <div class="container">
        <div class="offer-main">
          <div class="offer-main__list list-main">
            <h3 class="list-main__title">Мы предлагаем:</h3>
            <div class="list-main__content">
              <div class="list-main__row">
                <div class="list-main__item">
                  <p class="list-main__text">Согласование информациооных конструкций</p>
                </div>
                <div class="list-main__item">
                  <p class="list-main__text">Согласование рекламных конструкций</p>
                </div>
              </div>
            </div>
            <div class="list-main__row">
              <div class="list-main__item">
                <p class="list-main__text">Подготовка технической документации</p>
              </div>
              <div class="list-main__item">
                <p class="list-main__text">Разработка дизайн-проектов</p>
              </div>
            </div>
          </div>
          <div class="offer-main__list list-main">
            <h3 class="list-main__title">Ваши выгоды</h3>
            <div class="list-main__content">
              <div class="list-main__row">
                <div class="list-main__item">
                  <p class="list-main__text">Вы можете получить документы в минимальные сроки (от одной недели)</p>
                </div>
                <div class="list-main__item">
                  <p class="list-main__text">Вы гарантированно получите разрешение (если Ваши планы не противоречат закону)</p>
                </div>
              </div>
            </div>
            <div class="list-main__row">
              <div class="list-main__item">
                <p class="list-main__text">Оптимизируем Ваши затраты, так как мы знаем правильные шаги</p>
              </div>
              <div class="list-main__item">
                <p class="list-main__text">Оплата за результат! Вы оплачиваете
                  сразу только проектные работы, оплата за согласование только перед
                  подачей Вам уже подписанных разрешительных документов
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
    export default {
        name: "IndexOffer"
    }
</script>

<style lang="scss" scoped>
.list-main {
  margin-top: 40px;
  @media screen and (min-width:1140px) {
    margin-top: 60px;
  }
  &:first-child {
    margin-top: 0;
  }
  &__title {
    font-size: $big;
    font-weight: bold;
    @media screen and (min-width:1140px) {
      font-size: $biggest;
    }
  }
  &__content {
    margin-top: 30px;
    @media screen and (min-width:1140px) {
      margin-top: 60px;
    }
  }
  &__row {
    @media screen and (min-width:1140px) {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      @media screen and (min-width:1140px) {
        gap: 146px;
        &:first-child {
          .list-main__item {
            margin-top: 0;
          }
        }
      }
    }
  }
  &__item {
    margin-top: 20px;
    position: relative;
    padding-left: 55px;
    @media screen and (min-width:1140px) {
      margin-top: 46px;
    }
    &::before {
      content: '';
      position: absolute;
      left: 0;
      top: 0;
      width: 32px;
      height: 32px;
      border-radius: 50%;
      background: $green;
    }
    @media screen and (min-width:1140px) {
      width: 50%;
    }
  }
}
</style>
