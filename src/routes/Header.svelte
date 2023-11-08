<script>
import PocketBase  from 'pocketbase'
	import { writable } from 'svelte/store';
            

    const pb = new PocketBase('https://dev.coredump.online')

	const currentUser = writable(pb.authStore.model)
	pb.authStore.onChange((auth)=> {
		console.log('authStore changed',auth)
		currentUser.set(pb.authStore.model)
	})

    let username=""

    let password=""

</script>

<header>
	<title>Logo MDE App</title>
</header>

<style>
	
</style>
