<template>
	<div>
		<input v-model="username" />
		<button @click="login">Login</button>
	</div>
</template>

<script>
export default {
	name: 'Login',
	data:() => ({
		username:'',
	}),
	methods: {
		login() {
			if(this.username) {
				this.$emit('login', this.username);
			}
		}
	}
}
</script>