<template>
	<div class="vuex">
		vuex {{$store.state.count}}
		<button type="button" name="button" @click="increment">增加</button>
		<button type="button" name="button" @click="decrement">删减</button>
		<div @click="show">增加</div>
	</div>  
</template>

<script>
import {mapActions} from 'vuex'
export default {
	methods:{
		...mapActions([
		    'increment', 
		    'decrement'
	    ]),
	    show(){
	    	this.$store.dispatch('increment')
	    }
	}
}
</script>

<style lang="css">
	
</style>