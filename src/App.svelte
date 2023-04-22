<script>
  import Navbar from './Navbar.svelte';
  import SmileyContainer from './SmileyContainer.svelte';
	// export let name;
</script>

<Navbar />
<div class="main">
  <div  class="main-container">
    <div>
      <!-- First container -->
      <div class="container right-position">
        <div class="image-container">
          <div class="content-right">
            <p>"Notre mission : rendre durablement le plaisir et les bienfaits de la pratique du sport accessibles au plus grand nombre."</p>
          </div>
        </div>
      </div>
      <!-- Second container -->
      <div class="container left-position">
        <div class="content-container">
          <div class="content-left">
            <h1 class="percentage"><em>87%</em></h1>
            <h1 class="main-text"><em>DES GRIMPEURS EN SUISSE ACHÈTENT LEUR MATÉRIEL CHEZ DECATHLON.</em></h1>
            <h1 class="last-text"><em>ET VOUS ?</em></h1>
          </div>
        </div>
      </div>
    </div>
  </div>
  <SmileyContainer />
</div>

<style>
  :global(body) {
    margin: 0;
    padding: 0;
    font-family: 'Roboto Condensed', sans-serif;
  }


  .main {
    background: linear-gradient(174deg, rgba(221,231,241,1) 57%, rgba(255,255,255,0.9910015031403187) 57%);
    border-radius: 8px;
    box-shadow: 0px 0px 10px -2px rgba(0, 0, 0, 0.7);
    width: 95%;
    margin: 0 auto;
  }

	.main-container {
    min-height: 400px;
		text-align: left;
		padding: 1em;
    /* background: linear-gradient(166deg, rgba(221,231,241,1) 45%, rgba(255,255,255,0.9910015031403187) 46%); */
    background: transparent;
    /* border: 1px solid gray; */
    border-radius: 8px;
    position: relative;
	}

  /* TEXT */
  .percentage {
    font-size: 4em;
    font-weight: bold;
    margin: 0;
    color: #128134;
    font-family: 'Roboto Condensed', sans-serif;
    padding-left: 16px;
  }

  .main-text {
    color: #737a7e;
  }

  .last-text {
    color: #0C83C3;
  }
	h1 {
    font-family: 'Roboto Condensed', sans-serif;
    font-weight: 900;
		font-size: 2em;
    margin: 5px;
    padding-left: 16px;
	}

  p {
    font-weight: bold;
    margin-left: 24px;
    text-align: right;
    width: 80%;
  }

  .container {
    overflow: hidden;
    border-radius: 8px 8px 0px 0px;
    max-width: 50%;
    width: 100%;
    background: transparent;
  }

  .image-container {
    background-image: url("https://images.unsplash.com/photo-1586627161720-ee2849303aee?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80");
    background-size: cover;
    color: whitesmoke;
    box-shadow: -1px 1px 5px #00000066;

    min-height: 340px;

    display: flex;
    justify-content: end;
    align-items: end;

    transform: skewY(5deg);
    transform-origin: top right;
    border-radius: 8px 8px 0px 100px;
  }
  .content-container {
    /* background: linear-gradient(45deg, rgba(12,131,195,1) 40%, rgba(255,255,255,1) 100%); */
    background-color: #FFFFFF;
    box-shadow: 1px 1px 5px #00000066;

    min-height: 340px;

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
    padding: 16px;
    display: flex;
    justify-content: flex-end;
  }


  /* MEDIA QUERY */
	@media (min-width: 640px) {
		.main-container {
			max-width: none;
		}
	}

  @media (max-width: 600px) {
    .image-container {
      display: none;
    }
    .container {
      max-width: 95%;
    }
    .main {
      width: 100%;
    }
  }
</style>
