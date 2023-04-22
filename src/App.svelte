<script>
  import { each } from 'svelte/internal';
  import Navbar from './Navbar.svelte';
  import Smiley from './Smiley.svelte';
	// export let name;

    let smileys = [
    {
      src: "./images/verygood.png",
      smileyType: 'Happy',
      smileyText: 'Happy',
      clicked: false
    }
  ];
</script>

<Navbar />
<main>
	<h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
  {#each smileys as smiley}
    <Smiley src={smiley.src} alt={smiley.smileyType} smileyText={smiley.smileyText}/>
  {/each}
</main>
<style>

  :global(body) {
    margin: 0;
    padding: 0;
  }

	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;

    border: 1px solid gray;
    width: 80%;
    border-radius: 8px;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
