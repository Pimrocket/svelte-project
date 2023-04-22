<script>
  export let smileyType;
  export let smileyText;
  export let src;
  // export let clicked;
</script>

<style>
  div {
    text-align: center;
  }

  img {
    width: 65px;
    opacity: 50%;
  }
  img:hover {
    opacity: 100%;
  }

  p {
    margin: 0;
  }
</style>


<div>
  <img {src} alt={smileyType} />
  <p><strong>{smileyText}</strong></p>
</div>
