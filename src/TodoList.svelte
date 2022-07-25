<script>
	import TodoItem from './TodoItem.svelte';
	
	// views
	let ref = "";
	function handleClick() {
		if (input === "") return;
		
		addTodo();
    input = "";
		ref.focus();
	}
	
	// models
	let input = "";
	let todos = ["first-todo", "second-todo", "third-todo"];
	
	function addTodo() {
		todos = [input, ...todos];
	}
	
	function deleteTodo(id) {
		todos = todos.filter((_, i) => i !== id);
	}
</script>

<div class="main">
	<div class="form">
		<input bind:this={ref} type="text" placeholder="Add a new todo..." bind:value={input} />
		<button type="button" on:click={handleClick}>Add</button>
	</div>
	<div class="todolist">
		{#each todos as todo, i}
		<TodoItem id={i} todo={todo} deleteTodo={deleteTodo} />
		{/each}
	</div>
</div>

<style>
	.main,
	.todolist {
  	display: flex;
  	flex-direction: column;
  	gap: 15px;
	}
</style>
