<template>
	<img alt="Vue logo" src="./assets/logo.png" />
	<div v-if="manyItems.length">
		<HelloWorld
			v-for="item in manyItems"
			:msg="item.msg"
		/>
	</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HelloWorld from './components/HelloWorld.vue';

export default defineComponent( {
	components: {
		HelloWorld,
	},
	computed: {
		manyItems(): { msg: string }[] {
			return [ { msg: `item number 1!` } ];
		},
	},
} );
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
