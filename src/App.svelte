<script lang="ts">
  import { PenNib, Paperclip, Envelope  } from "phosphor-svelte";

import { Django, Bootstrap, Svelte, Tailwindcss } from '@icons-pack/svelte-simple-icons'
  import { onMount } from "svelte";
import '@fontsource/dm-sans';
let bootstrap = "First of all, this is my opinion. Someone may think differently than me, and that is ok. Bootstrap is amazing for new web developers. It looks good out of the box. Check. It is Extremely good at making responsize websites. Check. It is accesable for everyone, with amazing documention and a massive userbase. Check. But here is where it goes wrong. Bootstrap is simply not customizable. Their color pallete is good, and with the semi recent release of Bootstrap 5, it has gotten better, but it does not have the flexibility like regular css. Don't get me wrong, I have some things to say about that too, but in regards to color, that is where regular css wins. In my opinion, what this website is built on uses what is the perfect balence between the two: Tailwind CSS. Tailwind still has a limited color pallete, but much less than Bootstrap. Tailwind's downside is no prebuilt items, like spinners, cards, buttons, etc. Instead of using the prebuilt items provided by Bootstrap, you get to make your own. This allows for flexibility and creativity at the expense of speed. I think that at the end of the day, Boostrap has its strengths, but Tailwind is my favorite. For now."
let bootstrap20 =  "First of all, this is my opinion. Someone may think differently than me, and that is ok. Bootstrap"



let stuff = ["Developer", "Coffee Lover", "History Enthusiast"];
  let currentIndex = 0;

  function cycleContent() {
    currentIndex = (currentIndex + 1) % stuff.length;
  }

  onMount(() => {
    const interval = setInterval(cycleContent, 2000); // Cycle every 2 seconds

    return () => {
      clearInterval(interval);
    };
  });




</script>

<main class="snap-y snap-mandatory h-screen  w-screen overflow-x-hidden">  
<div class="bg-zinc-200    pattern-red-200 pattern-bg-gray-800 
  pattern-size-3 pattern-opacity-100
   dark:bg-gray-800">
  <div class="snap-start">
  <div class="flex justify-between sticky top-0 items-center z-50">
    <div class="">
      <a href="#blog" class=" mx-2 text-zinc-400 transition ease-in-out hover:translate-3 hover:text-pink-500 hover:scale-150 duration-300">Blog </a>
      <a href="#portfolio" class=" mx-2 text-zinc-400 transition ease-in-out hover:translate-3 hover:text-pink-500 hover:scale-150 duration-300">Portfolio</a>
    </div>
    <div>
      <a href="#hello" class="text-gray-800 mx-2 bg-gradient-to-r from-purple-400 to-pink-600 flex items-center rounded-lg p-2">Contact</a>
    </div>
  </div>
</div>
<div class="h-screen   w-screen flex items-center justify-center">
  <div>
  <h1 class="font-extrabold text-transparent text-9xl bg-clip-text bg-gradient-to-r from-purple-400 to-pink-600 text-center ">Jado
   <br> nus</h1>
   <p class="text-center dark:text-zinc-400">Developer • Coffee lover • History Enthuesiast</p>
  
  </div>
  </div>
  <div class=" snap-start  bg-gradient-to-r from-purple-400 to-pink-600
   dark:bg-gray-800 grid">
   <div class="bg-zinc-200 dark:bg-gray-800 mx-12 mt-12 rounded-t-lg">


   <h1 class=" text-7xl text-zinc-400 m-10" id="portfolio">Portfolio:</h1>

   <p class="text-zinc-400 m-16 text-2xl"><span class="text-3xl">Roads</span> <br> A bible Memory verse web app. <br>
    
  <span class="flex items-center mr-2">
Made with: 
    <Django />
     <Bootstrap />
  </span> 
<a  class="text-purple-500 transition ease-in-out hover:-translate-y-1 hover:text-pink-500 hover:scale-150 duration-300 hover:shadow-lg"href="https://roadsbible.com">Link  </a>
|
<a class="text-purple-500 transition ease-in-out hover:-translate-y-1 hover:text-pink-500 hover:scale-150 duration-300"href="https://github.com/jadonus/roads_bible_vercel">Github</a>
</p>

   <p class="text-zinc-400 m-16 text-2xl"><span class="text-3xl">This website</span> <br> My personal website, That you are one right now!<br>
    
  <span class="flex items-center mr-2">
Made with: 
    <Tailwindcss />
     <Svelte />
  </span> 
<a  class="text-purple-500 transition ease-in-out hover:-translate-y-1 hover:text-pink-500 hover:scale-150 duration-300"href="https://jadonus.github.io/homepage">Link  </a>
|
<a class="text-purple-500 transition ease-in-out hover:-translate-y-1 hover:text-pink-500 hover:scale-150 duration-300"href="https://github.com/jadonus/homepage">Github</a>
</p> 

   </div>



   </div>

<div class=" snap-start h-screen bg-gradient-to-r from-purple-400 to-pink-600
   dark:bg-gray-800 grid">
   <div class="bg-zinc-200 dark:bg-gray-800 mx-12 mb-12 rounded-b-lg">
</div>
</div>
<div id="blog" class="snap-start h-screen bg-zinc-200 dark:bg-gray-800">
<h1 class="m-12 text-zinc-400 text-7xl">
Blog
</h1>
<p class=" m-10 text-zinc-400">{bootstrap}...</p>

</div>

<div id="blog" class="snap-start bg-gradient-to-r from-purple-400 to-pink-600 h-screen ">

  <div class="bg-zinc-200 h-1/2  dark:bg-gray-800 mx-12 mt-12  rounded-b-lg">
<p class="text-zinc-400 m-4 text-center ">This website is Open Source.<br><br>View the source code on <a class="text-purple-400"href="https://github.com/jadonus/homepage">Github</a><br><br>Copyright 2023 Jadon Gearhart </p>
</div>
</div>
</main>
<style>
  main {
    font-family:  system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }
</style>
