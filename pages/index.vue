<template>
  <main class="flex flex-col items-center w-full">
    <Navbar/>
    <section class="hero flex items-center justify-center w-full">
      <div class="flex flex-col h-full items-center md:items-start justify-center md:mr-10">
        <div class="flex flex-col items-center md:items-start justify-center">
          <h1 class="leading-3 md:leading-normal">I’m <strong class="font-bold">Yasmine</strong></h1>
          <p class="text-sm">I create things with my keyboard !</p>
        </div>
        <img v-if="this.$mq==='sm'" src="~/static/images/glasses.png" class="w-2/3 -rotate-12" alt="">

        <div class="mt-5 md:mt-20">
          <div class="text-xl md:text-4xl hero-text">
            Designer <span class="text-xs hero-text--thin">&</span> Developer
          </div>
          <p class="text-sm text-center md:text-left md:mt-2">with a bit of fun</p>
        </div>

        <div class="links flex items-center mt-5">
          <a href="" class="mx-2"><img src="~/static/dribbble.svg" width="25" alt=""></a>
          <a href="" class="mx-2"><img src="~/static/github.svg" width="25" alt=""></a>
          <a href="" class="mx-2"><img src="~/static/email.svg" width="25" alt=""></a>
        </div>

        <p class="text-sm mt-10">Contact me via <strong class="font-bold text-black">E-mail</strong></p>
      </div>
      <div v-if="this.$mq!=='sm'" class="h-full flex items-center ml-10">
        <img src="~/static/images/ideas.png" class="hero-image" alt="">
      </div>
    </section>
    <div class="my-20">
      <scroll-wheel></scroll-wheel>
    </div>
    <section class="skills-section flex flex-col md:flex-row justify-center md:justify-around items-center md:items-start">
      <div class="flex md:flex-col items-center justify-end md:justify-center w-full md:w-1/2 mr-5">
        <h2 class="skills-section-title text-right md:text-lg w-1/2">My Skills</h2>
        <img v-if="this.$mq==='sm'" src="~/static/images/skills_image.png" alt="" class="skills-image">
        <img v-else src="~/static/images/skills_image_full.png" alt="" class="skills-image_full">
      
      </div>

      <div class="flex flex-col items-center justify-center w-1/2 ml-5">
        <div class="text-center md:text-left">
          <h3 class="skill-title text-xl md:text-2xl">Front-end <br v-if="this.$mq!=='sm'"> Development</h3>
          <p class="text-sm mt-5 md:mt-2 md:w-2/3">
            Front end developer since 3 years working with the latest technologies  
          </p>
        </div>
        <div class="mt-20 text-center md:text-left">
          <h3 class="skill-title text-xl md:text-2xl">Machine Learning <br> Development</h3>
          <p class="text-sm mt-5 md:mt-2 md:w-2/3">
            Front end developer since 3 years working with the latest technologies</p>
        </div>
        <div class="mt-20 text-center md:text-left">
          <h3 class="skill-title text-xl md:text-2xl">Web design</h3>
          <p class="text-sm mt-5 md:mt-2 md:w-2/3">
            Front end developer since 3 years working with the latest technologies  
          </p>
        </div>
      </div>
    </section>
    <div class="my-20">
      <scroll-wheel></scroll-wheel>
    </div>

  </main>
</template>

<script lang='ts'>
import {Vue, Component} from 'nuxt-property-decorator'
import Navbar from '~/components/layout/Navbar.vue'
import ScrollWheel from '~/components/ScrollWheel.vue'

@Component({
  components: {
    Navbar,
    ScrollWheel
  }
})
export default class Index extends Vue {}
</script>

<style lang='postcss' scoped>
p{
	color: #5C5C5C;
}
.hero{
  min-height: 90vh;
}
.hero-text{
  font-family: 'Satoshi-Black';
}
.hero-text--thin{
  font-family: 'Satoshi-Regular';
}
.hero-image{
  max-width: 350px !important;
}
.divider-line{
  background-color: black;
  width: 100px;
  height: 10px;
  right: 100;
  position: absolute;
}
.skills-section{
  min-height: 100vh;
}
.skill-title{
  font-family: 'Satoshi-Black';
}
.skills-section-title{
  color: #959595;
}
.skills-image{
  max-width: 150px;
}
.skills-image_full{
  max-width: 350px;
}
</style>