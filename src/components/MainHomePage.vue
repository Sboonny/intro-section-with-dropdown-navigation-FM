<template>
 <main class="grid">
  <div class="main--content">
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
   grid-template-rows: min-content 1fr;
   grid-template-areas: 
           'HomeImage'
           'HomeMain';
 }

 main {
   margin-inline: clamp(1em, 4vw, 4em);
   font-family: 'Epilogue', sans-serif;
   font-size: 18px;
 }

 h1 {
   font-size: 4em;
   font-weight: 700;
 }

 p {
   color: hsl(var(--gray));
   font-weight: 500;
 }

  button {
  background-color: hsl(var(--black));
  color: hsl(var(--white));
  border: 0;
  border-radius: 5px;
  font-weight: 700;
  padding: .5em .9em;
}

 .main--content {
   grid-area: HomeMain;
   color: hsl(var(--black));
   font-style: inherit;
 }
 
 .home-img {
   min-width: 300px;
   width: 30vw;
   max-width: 700px;
   grid-area: HomeImage;
 }

@media (min-width: 45em) {
  .grid {
   grid-template-columns: 1fr 1fr;
   grid-template-areas: 'HomeMain'
                        'HomeImag';
   }
  }

</style>