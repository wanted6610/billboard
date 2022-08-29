<template>
    <header class="header">
      <div class="container">
        <div class="header-top">
          <img src="@/static/logo.png" alt="Ваша реклама" class="header__logo">
          <svg-icon
            class="header-top__burger"
            :class="{'active': openMenu}"
            @click="openMenu = !openMenu"
            :name="openMenu ? 'burger-open' : 'burger-close'"
            :fill="openMenu ? '#fff' : '#000'"
            width="35"
            height="35"
          />
          <div class="header-top__contacts contacts">
            <a class="contacts__link" href="tel:78314300006">+7 (831) 4300 006</a>
            <div class="contacts-address">
              <p class="contacts-address__text">г. Нижний Новгород<br>с 10:00 до 17:30 по МСК</p>
            </div>
          </div>
          <transition name="fade">
            <div v-if="openMenu" class="header-top__menu menu">
              <div class="menu-wrapper">
                <div class="menu-list">
                  <div class="menu__link">
                    <nuxt-link exact to="/">Согласование рекламы</nuxt-link>
                  </div>
                  <div class="menu__link">
                    <nuxt-link to="/advertising">Реклама в МФЦ</nuxt-link>
                  </div>
                  <div class="menu__link">
                    <nuxt-link to="/panel">Световые панели</nuxt-link>
                  </div>
                  <div class="menu__link">
                    <nuxt-link to="/company">О компании</nuxt-link>
                  </div>
                  <div class="menu__link">
                    <nuxt-link to="/reviews">Отзывы</nuxt-link>
                  </div>
                  <div class="menu__link">
                    <nuxt-link to="/contacts">Контакты</nuxt-link>
                  </div>
                </div>
                <div class="menu__separator"></div>
                <div class="menu-contacts">
                  <div class="menu-contacts__phone">
                    <svg-icon stroke="#fff" name="phone" width="35" height="35" />
                    <a class="menu-contacts__link" href="tel:78314300006">+7 (831) 4300 006</a>
                  </div>
                  <div class="menu-contacts__geo">
                    <svg-icon name="geo" fill="#fff" width="35" height="35"/>
                    <div class="menu-contacts__geolocation">
                      <p class="menu-contacts__text">г. Нижний Новгород</p>
                      <p class="menu-contacts__text">с 10:00 до 17:30 по МСК</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </transition>
        </div>
      </div>
      <div class="header-menu">
        <div class="container">
          <div class="header-menu__wrapper">
            <nuxt-link class="header-menu__item" exact to="/">Согласование&nbsp;рекламы</nuxt-link>
            <nuxt-link class="header-menu__item" to="/advertising">Реклама в МФЦ</nuxt-link>
            <nuxt-link class="header-menu__item" to="/panel">Световые панели</nuxt-link>
            <nuxt-link class="header-menu__item" to="/company">О компании</nuxt-link>
            <nuxt-link class="header-menu__item" to="/reviews">Отзывы</nuxt-link>
            <nuxt-link class="header-menu__item" to="/contacts">Контакты</nuxt-link>
          </div>
        </div>
      </div>
      <div class="header-main" :class="{'minimal': $route.path !== '/'}">
        <h2 v-if="$route.path === '/'" class="header-main__title">Согласовать вашу рекламу возможно!</h2>
      </div>
    </header>
</template>

<script>
    export default {
        name: "BaseHeader",
        data() {
            return {
              openMenu: false,
            }
        },
      watch: {
          $route() {
            this.openMenu = false;
          }
      }
    }
</script>

<style lang="scss" scoped>
.contacts {
  display: none;
  @media screen and (min-width:1140px) {
    display: block;
  }
  &__link {
    font-size: $big;
  }
  &-address {
    &__text {
      line-height: 24px;
    }
  }
}

.menu {
  position: fixed;
  left: 0;
  top: 0;
  right: 0;
  bottom: 0;
  background: $green;
  justify-content: center;
  align-items: center;
  display: flex;
  flex-direction: column;
  padding: 16px;
  @media screen and (min-width:1140px) {
    display: none;
  }
  &-wrapper {
    overflow: auto;
    width: 100%;
  }
  &__separator {
    height: 1px;
    width: 100%;
    background: $white;
    margin: 20px 0;
  }
  &-contacts {
    display: flex;
    flex-direction: column;
    align-items: center;
    &__phone {
      display: flex;
      align-items: center;
    }
    &__geo {
      margin-top: 15px;
      display: flex;
      align-items: center;
    }
    &__geolocation {
      margin-left: 10px;
    }
    &__text {
      color: $white;
      margin-top: 5px;
      &:first-child  {
        margin-top: 0;
      }
    }
    &__link {
      margin-left: 10px;
      color: $white;
    }
  }
  &__link {
    color: $white;
    text-align: center;
    margin-top: 10px;
    &:first-child {
      margin-top: 0;
    }
    & a {color: inherit}
  }
}

.header {
  &-menu {
    display: none;
    @media screen and (min-width:1140px) {
      display: flex;
      max-width: 1512px;
      margin: 0 auto;
      justify-content: center;
      border-top: 2px solid $green;
      &__item {
        cursor: pointer;
        padding: 24px 10px;
        flex: 1;
        text-align: center;
        font-size: 16px;
      }
      &__wrapper {
        display: flex;
        align-items: center;
      }
    }
    @media screen and (min-width:1280px) {
      &__item {
        padding: 24px 30px;
        &:hover {
          color: $green;
        }
      }
    }
  }
  &-main {
    min-height: 300px;
    background: url("@/static/header__bg.png");
    background-size: cover;
    background-repeat: no-repeat;
    display: flex;
    align-items: flex-end;
    max-width: 1512px;
    margin: 0 auto;
    @media screen and (min-width:1140px) {
      min-height: 439px;
    }
    &.minimal {
      height: 114px;
      min-height: auto;
    }
    &__title {
      color: $white;
      background: rgba(0, 0, 0, 0.6);
      padding: 20px;
      width: 100%;
      @media screen and (min-width:1140px) {
        padding: 44px 39px;
        font-size: $super-big;
      }
    }
  }
  &__logo {
    width: 100px;
    @media screen and (min-width:1140px) {
      width: 204px;
      height: 126px;
    }
   }
  &-top {
    position: relative;
    margin: 15px 0;
    display: flex;
    justify-content: space-between;
    align-items: center;
    @media screen and (min-width:1140px) {
      margin: 40px 0;
    }
    &__burger {
      &.active {
        z-index: 1;
        position: fixed;
        right: 16px;
      }
      @media screen and (min-width:1140px) {
        display: none;
      }
    }
  }
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}
</style>
