<script>
  import Smiley from "./Smiley.svelte";

  let smileys = [
    {
      src: "./images/verygood.png",
      smileyText: 'Very good',
      clicked: false
    },
    {
      src: "./images/good.png",
      smileyText: 'Good',
      clicked: false
    },
    {
      src: "./images/okay.png",
      smileyText: 'Okay',
      clicked: false
    },
    {
      src: "./images/bad.png",
      smileyText: 'Bad',
      clicked: false
    },
    {
      src: "./images/verybad.png",
      smileyText: 'Very bad',
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
    <h3>Thank you so much for leaving your feedback!</h3>
    <button on:click={smileyClicked} class="resetbtn">Change your mind?</button>
  {:else}
  <h3>How was your experience?</h3>
    <div class="smiley-container">
      {#each smileys as smiley }
      <div>
        <button on:click={smileyClicked} class="smileybtn">
          <Smiley src={smiley.src} smileyText={smiley.smileyText} />
        </button>
        <p>{smiley.smileyText}</p>
      </div>
      {/each}
    </div>
  {/if}
</div>

<style>

  .review-container {
    width: 55%;
    border: 1px solid gray;
    border-radius: 8px;
    min-height: 200px;
    margin: 0 auto;
    text-align: center;
  }

  .smiley-container {
    display: flex;
    align-items: center;
    justify-content: space-evenly;
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
  }

  .resetbtn:hover {
    background-color: #065681;
  }

  p {
    margin: 0;
  }
</style>
