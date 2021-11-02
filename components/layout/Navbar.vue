<template>
	<nav class="w-screen md:w-2/3 flex items-center justify-center md:justify-around py-2">
			<a href="" class="link">My projects</a>
			<a href="" class="link">Contact</a>
			<h1 class="brand text-sm md:text-xl">YasRch</h1>
			<a href="" class="link">My skills</a>
			<a href="" class="link">About</a>
	</nav>
</template>

<script lang='ts'>
import {Vue, Component} from 'nuxt-property-decorator'

@Component({})
export default class Navbar extends Vue {

}
</script>

<style lang='postcss' scoped>
.brand{
    font-family: 'Satoshi-Black';
}
.link{
	@apply text-sm;
}
</style>