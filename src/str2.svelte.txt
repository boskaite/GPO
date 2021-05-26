<script>
	let L1=true;
	let L2=true;
	function B1click() {
	L1=!L1;
	}
	function B2click() {
	L2=!L2;
	}
	function Out (){}//прописать переход на страницу приветствия
</script>

<main>
	<h2>Линия 1</h2>
	{#if L1}
	<button class="exit" on:click={B1click}>Выключить</button>
	{:else}
	<button class="enter"on:click={B1click}>Включить</button>
	{/if}
	<h2>Линия 2</h2>
	{#if L2}
	<button class="exit" on:click={B2click}>Выключить</button>
	{:else}
	<button class="enter" on:click={B2click}>Включить</button>
	{/if}
	<h2>
	</h2>
	<button class="out" on:click={Out}>Выйти</button>
</main>

<style>
	h2{
margin-left: 40px;
	}
	button{
margin-left: 40px;
	}
	button.enter{
	background-color: rgb(10,250,20);
    border-color: #ff3e00;
	}
	button.exit{
	background-color: #ff3e00;
    border-color: #ff3e00;
	}
	button.out{
margin-left: 40px;
		margin-top: 20px;
		height: 40px;
		width: 100px;
		background-color: rgb(200,200,200);
    border-color: #ff3e00;
	}
</style>