<script>
	import TodoList from './TodoList.svelte';
</script>

<div id="app">
	<h1>Todo App with Svelte</h1>
	<TodoList/>
</div>

<style>
	#app {
		font-family: Avenir, Helvetica, Arial, sans-serif;
  	-webkit-font-smoothing: antialiased;
  	-moz-osx-font-smoothing: grayscale;
  	color: #2c3e50;
  	display: flex;
  	flex-direction: column;
  	align-items: center;
	}
</style>
