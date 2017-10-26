<template lang='pug'>
  section.container
    logo
    a.title(:href='link', target='_blank')
      | {{ msg }}
      icon.link(name='github', width='28', height='28')
</template>

<script>
import Logo from '~/components/Logo'

export default {
  components: { Logo },

  data () {
    return {
      msg: 'NuxtFire Starter Kit',
      link: 'https://github.com/sevenns/nuxtfire-starter-kit'
    }
  }
}
</script>

<style lang='sass' scoped>
@import '../assets/sass/variables'
@import '../assets/sass/mixins'


.container
  height: 100vh
  display: flex
  justify-content: center
  align-items: center
  text-align: center

.title
  display: flex
  align-items: center
  @include font(light)
  font-size: 30px
  text-decoration: none
  color: $gray
  margin-top: 15px

.link
  color: $gray
  margin-left: 10px
</style>
