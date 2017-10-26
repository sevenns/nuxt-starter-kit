<template lang='pug'>

.page-loader__wrapper
  transition(name='page-loader')
    .page-loader(v-if='loading')
      icon(name='bubbles', color='#35495E', width='172', height='172')

</template>

<script>

export default {
  data: () => ({
    loading: false
  }),

  methods: {
    start () {
      this.loading = true
    },
    finish () {
      setTimeout(() => {
        this.loading = false
      }, 500)
    }
  }
}
</script>

<style lang='sass' scoped>

.page-loader
  align-items: center
  background-color: #fff
  display: flex
  height: 100%
  justify-content: center
  left: 0
  position: fixed
  top: 0
  width: 100%
  z-index: 99999

.page-loader-enter-active,
.page-loader-leave-active
  transition: opacity .5s ease, transform .5s ease

.page-loader-enter,
.page-loader-leave-to
  opacity: 0
  transform: scale(1.2)

</style>
