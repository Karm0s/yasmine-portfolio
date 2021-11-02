<template>
	<nav class="w-screen flex items-center justify-center py-2">
			<h1 class="brand text-sm">YasRch</h1>
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

</style>