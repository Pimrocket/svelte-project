<script>
  import Smiley from "./Smiley.svelte";

  let smileys = [
    {
      src: "./images/verygood.png",
      smileyText: 'Très Bon',
      clicked: false
    },
    {
      src: "./images/good.png",
      smileyText: 'Bon',
      clicked: false
    },
    {
      src: "./images/okay.png",
      smileyText: 'Neutre',
      clicked: false
    },
    {
      src: "./images/bad.png",
      smileyText: 'Mauvais',
      clicked: false
    },
    {
      src: "./images/verybad.png",
      smileyText: 'Très Mauvais',
      clicked: false
    }

  ];

  let clicked = false;

  let smileyClicked = () => {
    clicked = !clicked
  }

</script>


<div class="review-container">
  {#if clicked}
  <h3>Merci d'avoir partagé votre opinion!</h3>
    <button on:click={smileyClicked} class="resetbtn">Avez-vous changé d'avis?</button>
  {:else}
  <h3>Quel est votre niveau de satisfaction concernant decathlon.ch?</h3>
    <div class="smiley-container">
      {#each smileys as smiley }
      <div>
        <button on:click={smileyClicked} class="smileybtn">
          <Smiley src={smiley.src} smileyText={smiley.smileyText} />
        </button>
        <p class="smiley-text">{smiley.smileyText}</p>
      </div>
      {/each}
    </div>
  {/if}
</div>

<style>

  .review-container {
    width: 80%;
    margin: 0 auto;
    text-align: center;
    padding-bottom: 16px;
  }

  .smiley-container {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .smileybtn {
    background: transparent;
    border: none;
    border-radius: 50%;
    margin: 0;
  }

  .resetbtn {
    border-radius: 8px;
    background-color: #0C83C3;
    color: whitesmoke;
    border: none;
    margin-top: 24px;
  }

  .resetbtn:hover {
    background-color: #065681;
  }

  h3{
    margin: 0%;
  }
  p {
    margin: 0;
  }

  @media (max-width: 600px) {
    .review-container {
      width: 100%;
    }
    .smiley-text {
      display: none;
    }
  }
</style>
