<template>
  <input class="input" :placeholder="placeholder" type="text">
</template>

<script>
    export default {
        name: "BaseInput",
        props: {
          placeholder: {
            type: String,
            default: '',
          }
        }
    }
</script>

<style scoped>
.input {
  width: 100%;
  padding: 16px 20px;
  background: #E3E3E3;
}
</style>
