<script>
	import Header from './Header.svelte';
	import './styles.css';
	import { setContext } from 'svelte';

	import  PocketBase  from 'pocketbase'

	const pb = new PocketBase('https://dev.coredump.online')

	setContext('pb',pb)


	
	
</script>

<div class="app">
	<Header />
	<div class="columns">
		<div class="column">
						
		</div>
		<div class="column is-three-quarters">
			<div class="box is-rounded has-text-centered">
				<main>
					<slot />
				</main>
			</div>

		</div>
		<div class="column">

		</div>
	</div>

	

	
</div>


