<template>
  <div>
    yoyo i'm products/id
    {{ product }}
  </div>
</template>

<script>

export default {
  computed: {
    product () {
      return this.$store.getters.getProductById(this.$route.params.id)
    }
  }
}
</script>

<style scoped>

</style>
