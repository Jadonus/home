<script>
  let stuff = ["Developer", "Coffee Lover", "History Enthusiast"];
  let currentIndex = 0;
</script>

<div class="flex justify-center items-center h-screen">
  {#each stuff as entry, index}
    <div
      class="absolute text-4xl opacity-0 transition-opacity transform"
      class:opacity-100={currentIndex === index}
      class:translate-x-0={currentIndex === index}
      class:translate-x-full={currentIndex !== index}
      class:-translate-x-full={currentIndex !== index}
      in:slide-in={currentIndex === index}
      out:slide-out={currentIndex !== index}
    >
      {entry}
    </div>
  {/each}
</div>

<style>
  .slide-in {
    transition: transform 0.5s ease, opacity 0.5s ease;
  }

  .slide-out {
    transition: transform 0.5s ease, opacity 0.5s ease;
  }
</style>