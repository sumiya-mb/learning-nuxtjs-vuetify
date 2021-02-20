<template>
  <div>
    <v-container>
      <Hero/>
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
      <SmallCardDisplay
        v-for="cardInfo in cardsSection"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
    </v-container>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '@/assets/data.js'

export default {
  data () {
    return {
      largeCardInfo: largeCardSections,
      cardsSection: smallCardSections
    }
  }
}
</script>
