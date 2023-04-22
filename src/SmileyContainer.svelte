<script>
  import Smiley from "./Smiley.svelte";

  let smileys = [
    {
      src: "./images/verygood.png",
      smileyType: 'Very good smiley',
      smileyText: 'Very good',
      clicked: false
    },
    {
      src: "./images/good.png",
      smileyType: 'Good smiley',
      smileyText: 'Good',
      clicked: false
    },
    {
      src: "./images/okay.png",
      smileyType: 'Okay smiley',
      smileyText: 'Okay',
      clicked: false
    },
    {
      src: "./images/bad.png",
      smileyType: 'Bad smiley',
      smileyText: 'Bad',
      clicked: false
    },
    {
      src: "./images/verybad.png",
      smileyType: 'Very bad smiley',
      smileyText: 'Very bad',
      clicked: false
    }
  ];

</script>


<div class="review-container">
  <h3>How was your experience?</h3>
    <div class="smiley-container">
    {#each smileys as smiley }
      <Smiley src={smiley.src} alt={smiley.smileyType} smileyText={smiley.smileyText}/>
    {/each}
  </div>
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
</style>
