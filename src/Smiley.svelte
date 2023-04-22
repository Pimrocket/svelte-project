<script>
  export let src;
  export let smileyText;
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
</style>


<div>
  <img src={src} alt={smileyText}/>
</div>
