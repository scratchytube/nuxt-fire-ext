<template>
  <div class="container">
    <LargeCardDisplay
      v-for="lgCard in largeCardInfo"
      :key="lgCard.id"
      :cards-section="lgCard"
    />
    <SmallCardDisplay
      v-for="smCard in smallCardInfo"
      :key="smCard.id"
      :cards-section="smCard"
    />
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '@/assets/data.js'
export default {
  data () {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
    }
  }
}
</script>

<style scoped>

</style>
