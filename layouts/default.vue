<template lang='pug'>
  nuxt
</template>

<script>
import '~/assets/icons/dist'

export default {
  name: 'default'
}
</script>

<style lang='sass'>
@import '../assets/sass/variables'
@import '../assets/sass/mixins'


*, *::after, *::before
  box-sizing: border-box

html
  @include font(default)
  font-size: $base-fsize !important

body
  color: $gray
  font-size: $base-fsize !important
  line-height: 1.6
  min-width: 320px
  overflow: hidden
  position: relative
  @include font(default)

ul
  margin: 0
  padding: 0

textarea, input, select
  -webkit-appearance: none !important
  border-radius: 0 !important
</style>
