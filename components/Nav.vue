<template>
  <div>
    <v-app-bar
      color="deep-purple accent-4"
      dense
      dark
    >
      <v-toolbar-title class="title">
        <NuxtLink to="/" class="nav_text">Fireegii</NuxtLink>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-list class="items">
        <NuxtLink to="products" class="nav_text">Products</NuxtLink>
      </v-list>

      <v-list class="items">
        <NuxtLink to="my-items" class="nav_text">My Items</NuxtLink>
      </v-list>

      <v-menu
        left
        bottom
      >

      </v-menu>
    </v-app-bar>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.title {
  margin-left: 2.5rem;
}

.items {
  margin: 0 2rem;
}

.nav_text {
  text-decoration: none;
  color: white;
}

</style>
