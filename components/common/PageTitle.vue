<template>
    <div class="container">
      <p class="title">{{title}}</p>
    </div>
</template>

<script>
    export default {
        name: "PageTitle",
        props: {
          title: {
            type: String,
            default: '',
          }
        }
    }
</script>

<style lang="scss" scoped>
.title {
  margin-top: 30px;
  border-bottom: 2px solid $green;
  padding-bottom: 15px;
  @media screen and (min-width:1140px) {
    margin-top: 82px;
  }
}
</style>
