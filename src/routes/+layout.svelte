<script>
	import Header from './Header.svelte';
	import './styles.css';


	
	
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


