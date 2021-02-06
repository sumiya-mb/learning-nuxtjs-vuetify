vue
<template>
  <div class="container">
    <h4 class="header">Top rated Fire Extinguisher in Niagara</h4>
    <p class="snippent">User say these are the best fire extinguishers to rent if your house is burning down.</p>
    <div class="cards-container"></div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.container {
  margin-top: 2rem;
  padding: 0 15rem;
}

.header {
  font-weight: 700;
  font-size: 1.5rem;
}

.snippet {
  color: grey;
  margin-bottom: 1.5rem;
}

.cards-container {
  display: flex;
  justify-content: space-between;
}
</style>
