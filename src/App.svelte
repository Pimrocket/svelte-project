<script>
  import Navbar from './Navbar.svelte';
  import SmileyContainer from './SmileyContainer.svelte';
	// export let name;
</script>

<Navbar />
<main>
  <div class="main-container">
    <!-- First container -->
    <div class="container right-position">
      <div class="image-container">
        <div class="content-right">
          <p>"Move people through the wonders of sport."</p>
        </div>
      </div>
    </div>
    <!-- Second container -->
    <div class="container left-position">
      <div class="content-container">
        <div class="content-left">
          <h1>Thanks for shopping at Decathlon!</h1>
        </div>
      </div>
    </div>
  </div>
</main>
<SmileyContainer />

<style>
  :global(body) {
    margin: 0;
    padding: 0;
  }

	main {
    min-height: 400px;
		text-align: center;
		padding: 1em;
		/* max-width: 240px; */
		margin: 0 auto;

    background: linear-gradient(166deg, rgba(221,231,241,1) 45%, rgba(255,255,255,0.9910015031403187) 46%);
    border: 1px solid gray;
    width: 80%;
    border-radius: 8px;
    position: relative;
	}

	h1 {
		font-size: 4em;
		font-weight: 200;
	}

  .container {
    overflow: hidden;
    border-radius: 8px 8px 0px 0px;
    max-width: 50%;
  }

  .image-container {
    background-image: url("https://images.unsplash.com/photo-1586627161720-ee2849303aee?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80");
    background-size: cover;
    color: whitesmoke;
    overflow: hidden;
    border-radius: 8px 8px 0px 0px;

    min-height: 340px;
    width: 750px;
    max-width: 100%;

    display: flex;
    justify-content: center;
    align-items: center;

    transform: skewY(5deg);
    transform-origin: top right;
    border-radius: 8px 8px 0px 100px;
  }
  .content-container {
    background: linear-gradient(45deg, rgba(12,131,195,1) 40%, rgba(255,255,255,1) 100%);
    color: whitesmoke;
    overflow: hidden;

    min-height: 300px;
    /* min-width: 450px; */

    display: flex;
    justify-content: center;
    align-items: center;

    transform: skewY(-5deg);
    transform-origin: top left;
    border-radius: 8px 8px 100px 0px;
  }

  .left-position {
    position: absolute;
    top: 5%;
    left: 3%;
  }
  .right-position {
    position: absolute;
    bottom: 12%;
    right: 3%;
  }

  .content-left {
    transform: skewY(5deg);
  }
  .content-right {
    transform: skewY(-5deg);
  }

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}

  @media (max-width: 800px) {
    h1 {
      font-size: 2em ;
    }
  }

  @media (max-width: 600px) {
    .image-container {
      display: none;
    }
    .container {
      max-width: 95%;
    }
  }
</style>
