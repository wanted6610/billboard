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

a.nuxt-link-active {
  font-weight: 600;
  position: relative;
  &:after {
    content: '';
    position: absolute;
    left: 0;
    right: 0;
    height: 3px;
    background: $purple;
    bottom: -12px;
    border-radius: 30px;
  }
}

</style>
