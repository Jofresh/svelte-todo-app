<script>
	// props
	export let todo;
	export let id;
	export let deleteTodo;
	
	import CloseIcon from "./CloseIcon.svelte";
</script>

<div class="todo">
	<div>{todo}</div>
	<CloseIcon handleClick={() => deleteTodo(id)}></CloseIcon>
</div>

<style>
	.todo {
		display: flex;
  	align-items: center;
  	justify-content: space-between;
  	padding: 10px;
  	border-radius: 5px;
  	box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 4px;
	}
</style>