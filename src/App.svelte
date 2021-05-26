<script>
	export let name;
	let login='';
	let password='';
	let logingenter='0';
	let passwordenter='0';
	let count = 0; 
	function handleClick() {
    logingenter=login;
	passwordenter=password;
	//count += 1 ;
	}
</script>

<main>
	<h1>Приветствую тебя, {name}!</h1>
	<p>Введи данные учетной записи для входа.</p>
	<input bind:value={login} placeholder="Логин">
	<input bind:value={password} placeholder="Пароль">
	{#if logingenter==="gpo" && passwordenter==="gpo"}
		<button on:click={handleClick}>
			Выйти
		</button>
	{:else if logingenter==='0' && passwordenter==='0'}
		<button on:click={handleClick}>
			Войти
		</button>
	{:else}
		<button on:click={handleClick}>
				Войти
		</button>
		<h4>Данные введены неверно. Проверьте логин и пароль и ещё раз попытайтесь совершить вход.</h4>
	{/if}
	
	<!--{#if count === 0 }
	<p></p> 
	{:else if logingenter==="gpo" && passwordenter==="gpo"}
		<p>переход на страницу с кнопками вкл/выкл</p>
		<button on:click={handleClick}>Выход </button>	
	{:else}
		<h4>Данные введены неверно. Проверьте логин и пароль и ещё раз попытайтесь совершить вход.</h4>
	{/if}-->
</main>



<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 3em;
		font-weight: 100;
	}
	button {
    height: 3rem;
    width: 8rem;
    background-color: rgb(104, 104, 104);
    border-color: #ff3e00;
    color: #ff3e00;
    font-size: 1.25rem;
    background-image: linear-gradient(45deg, #ff3e00 50%, transparent 50%);
    background-position: 100%;
    background-size: 400%;
    transition: background 300ms ease-in-out;
  }
  button:hover {
    background-position: 0;
    color: rgb(104, 104, 104);
  }

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>