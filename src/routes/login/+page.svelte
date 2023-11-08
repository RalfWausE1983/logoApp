<script>
       let username=""

let password=""
    
    const login = async ()=> {
        await pb.collection('users').authWithPassword(
        username,
        password, 
    ).then((e)=>{

        console.log(e)

        }
     )
}

    const getArtList = async () => {
        await pb.collection('artikel').getFullList({
        sort: '-created',
        }).then((e)=>{
            console.log(e)
        })
    }


</script>



<div class="columns">
    <div class="column">

    </div>
    <div class="column">
        <div class="title is-2">Login</div>




<input class="input" type="text" id="username" style="witdth 30%" placeholder="Benutzername" bind:value={username}/>


<input class="input mt-4" type="password" id="password" placeholder="Passwort" bind:value={password} />

<button class="button is-rounded is-dark is-large is-danger mt-3" on:click={login}>Login</button>


    </div>
    <div class="column">

    </div>



</div>
