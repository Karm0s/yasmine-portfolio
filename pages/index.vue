<template>
  <main class="flex flex-col items-center">
    <Navbar/>
    <section class="hero flex flex-col items-center justify-center h-screen">
      <div class="flex flex-col items-center justify-center">
        <h1 class="leading-3">I’m <strong class="font-bold">Yasmine</strong></h1>
        <p class="text-sm">I create things with my keyboard !</p>
      </div>
      <img v-if="this.$mq==='sm'" src="~/static/images/glasses.png" class="w-2/3 -rotate-12" alt="">

      <div class="mt-5">
        <div class="text-xl hero-text">
          Designer <span class="text-xs hero-text--thin">&</span> Developer
        </div>
        <p class="text-sm text-center">with a bit of fun</p>
      </div>

      <div class="links flex items-center mt-5">
        <a href="" class="mx-2"><img src="~/static/dribbble.svg" width="25" alt=""></a>
        <a href="" class="mx-2"><img src="~/static/github.svg" width="25" alt=""></a>
        <a href="" class="mx-2"><img src="~/static/email.svg" width="25" alt=""></a>
      </div>

      <p class="text-sm mt-10">Contact me via <strong class="font-bold text-black">E-mail</strong></p>
    </section>
  </main>
</template>

<script lang='ts'>
import {Vue, Component} from 'nuxt-property-decorator'
import Navbar from '~/components/layout/Navbar.vue';

@Component({
  components: {
    Navbar,
  }
})
export default class Index extends Vue {

}
</script>

<style lang='postcss' scoped>
p{
	color: #5C5C5C;
}
.hero-text{
  font-family: 'Satoshi-Black';
}
.hero-text--thin{
  font-family: 'Satoshi-Regular';
}
</style>