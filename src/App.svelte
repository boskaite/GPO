<script>
	export let name;
	let login='';
	let password='';
	const logingenter;
	const passwordenter;

</script>

<main>
	<h1>Приветствую тебя, {name}!</h1>
	<p>Введи данные учетной записи для входа.</p>
</main>

<input bind:value={login} placeholder="Логин">
<input bind:value={password} placeholder="Пароль">

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

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>