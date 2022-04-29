<template>
 <main class="grid">
  <div>
  <h1>Make remote work</h1>

  <p>Get your team in sync, no matter your location. Streamline processes, 
  create team rituals, and watch productivity soar.</p>

  <button>Learn more</button>
  
  <img src="src/assets/client-databiz.svg" alt="data biz">
  <img src="src/assets/client-audiophile.svg" alt="audio phile">
  <img src="src/assets/client-meet.svg" alt="meet">
  <img src="src/assets/client-maker.svg" alt="maker">
  </div>
  <picture >
    <source class="home-img" media="(min-width: 45em)" srcset="src/assets/image-hero-desktop.png">
  <img class="home-img" src="src/assets/image-hero-mobile.png" alt="Remote work">
</picture>
</main>
</template>

<style scoped>
 .grid {
   display: grid;
   gap: var(--gap, 2em);
 }

 main {
   margin-inline: clamp(1em, 4vw, 4em);
 }

 .home-img {
   min-width: 300px;
   width: 30vw;
   max-width: 700px;
 }

@media (min-width: 45em) {
  .grid {
   grid-template-columns: 1fr 1fr;
  }
}
</style>