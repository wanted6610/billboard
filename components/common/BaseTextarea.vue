<template>
  <textarea :placeholder="placeholder" name="" id="" cols="30" rows="10" class="textarea"></textarea>
</template>

<script>
    export default {
        name: "BaseTextarea",
        props: {
          placeholder: {
            type: String,
            default: '',
          }
        }
    }
</script>

<style lang="scss" scoped>
.textarea {
  background: #E3E3E3;
  width: 100%;
  border: none;
  resize: none;
  padding: 30px 20px;
  font-size: $normal;
  color: #373737;
  max-height: 98px;
}
</style>
