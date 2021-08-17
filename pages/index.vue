/* eslint-disable vue/attribute-hyphenation */
<template>
  <div>
    <div class="container">
      <Hero />
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo"
        :key="cardInfo.id"
        :cards-section="cardInfo"
      />

      <SmallCardDisplay
        v-for="smallCardInfo in smallCardSections"
        :key="smallCardInfo.id"
        :cards-section="smallCardInfo"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '@/assets/data.js'

export default {
  data () {
    return {
      largeCardInfo: largeCardSections,
      smallCardSections
    }
  }
}
</script>
