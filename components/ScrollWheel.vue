<template>
  <img src="~/static/images/scroll_wheel.png" ref="wheel" width="40" alt="" />
</template>

<script lang="ts">
import { Vue, Component, Watch } from 'nuxt-property-decorator'

@Component({})
export default class ScrollWheel extends Vue {
  mounted() {
    window.addEventListener('scroll', this.rotateWheel)
  }
  rotateWheel() {
    let wheel:Element|any = this.$refs.wheel
    wheel.style.transform = `rotate(${window.scrollY}deg)`
  }
}
</script>

<style lang="postcss" scoped>
img{
	transition: all 0.5s ease-out;
}
</style>
