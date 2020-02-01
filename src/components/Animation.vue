<template>
	<div class="Animation">
		<div>
			<h1 style="text-align: center;">Animation?</h1>
		</div>
		<div>
			<p>ID: {{$route.params.id}}</p>
		</div>
	</div>
</template>

<script>
import myCarousel from './Carousel'
export default {
	name: 'Animation',
	components: {
		myCarousel
	},
	data () {
		return {
		}
	}
}
</script>
