<script>
  import Navbar from './Navbar.svelte';
  import SmileyContainer from './SmileyContainer.svelte';
	// export let name;
</script>

<Navbar />
<main>
  <!-- <div> -->
    <!-- First container -->
    <div class="picture-container">
      <div class="image-container">
        <div class="image-content">
          <h1 class="image-text">Thanks for shopping at Decathlon!</h1>
        </div>
      </div>
    </div>
    <!-- Second container -->
    <div class="picture-container">
      <div class="image-container">
        <div class="image-content">
          <h1 class="image-text">Thanks for shopping at Decathlon!</h1>
        </div>
      </div>
    </div>
  <!-- </div> -->
</main>
<!-- <SmileyContainer /> -->

<style>
  :global(body) {
    margin: 0;
    padding: 0;
  }

	main {
    min-height: 600px;
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;

    border: 1px solid gray;
    width: 80%;
    border-radius: 8px;

    display: flex;
    justify-content: center;
    align-items: center;
	}

	h1 {
		font-size: 4em;
		font-weight: 100;
	}

  .picture-container {
    border: 1px solid red;
    overflow: hidden;
    /* min-height: 350px; */
    border-radius: 8px 8px 0px 0px;
    max-width: 50%;
  }

  .image-container {
    background-image: url("https://images.unsplash.com/photo-1586627161720-ee2849303aee?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80");
    background-position: center;
    object-fit: cover;
    color: whitesmoke;
    overflow: hidden;

    min-height: 350px;
    transform: skewY(-5deg);
    transform-origin: top left;
    border-radius: 8px 8px 100px 0px;

    display: flex;
    justify-content: center;
    align-items: center;
  }

  .image-content {
    transform: skewY(5deg);
  }

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
