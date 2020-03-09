<template>
	<div>
		<section>
			<p>Create Game</p>
			<input v-model="gameName" />
			<button @click="$emit('create-game', gameName)">Create Game</button>
		</section>
		<section>
			<p>Join Game</p>
			<input v-model="gameId" placeholder="Enter an existing game" />
			<button @click="$emit('join-game', gameId)">Join Game</button>	
		</section>
	</div>
</template>
<script>
export default {
	data:() => ({
		gameName:'',
		gameId:'',
	})
}
</script>
<style scoped>
div {
	display: flex;
}
p {
  margin: 4px;
}

section {
  padding: 16px;
  background-color: whitesmoke;
  margin: 16px;
}
</style>