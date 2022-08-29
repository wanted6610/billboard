<template>
  <div class="main">
    <base-header />
    <div class="content"><nuxt /></div>
    <base-footer />
  </div>
</template>

<script>
import BaseHeader from "~/components/common/BaseHeader";
import BaseFooter from "~/components/common/BaseFooter";

export default {
  name: "default",
  components: {
    BaseFooter,
    BaseHeader,
  }
}
</script>

<style lang="scss">

a.nuxt-link-active {
  font-weight: 700;
  position: relative;
  text-decoration: underline;
  @media screen and (min-width:1140px) {
    font-weight: 400;
    color: $white !important;
    background: $green;
    text-decoration: none;
  }
}

.content {flex: 1}

.main {
  height: 100%;
  display: flex;
  flex-direction: column;
}

html,body, #__nuxt, #__layout{
  height:100%!important;
  width: 100%!important;
}

</style>
