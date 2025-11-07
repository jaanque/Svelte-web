<script lang="ts">
  import Header from '$lib/Header.svelte';
  import Hero from '$lib/Hero.svelte';
  import CreatorCard from '$lib/CreatorCard.svelte';

  const creators = [
    {
      avatar: 'https://storage.googleapis.com/cursos-images/2/1/C.svg',
      name: 'Cara',
      action: 'building a new platform for artists',
      supporters: 8780,
    },
    {
      avatar: 'https://storage.googleapis.com/cursos-images/2/1/K.svg',
      name: 'Kaleigh Cohen',
      action: 'creating indoor cycling and strength workouts on YouTube!',
      supporters: 4488,
    },
    {
      avatar: 'https://storage.googleapis.com/cursos-images/2/1/T.svg',
      name: 'Teacher Stefano',
      action: 'creating YouTube videos and Podcast',
      supporters: 641,
    },
    {
      avatar: 'https://storage.googleapis.com/cursos-images/2/1/Th.svg',
      name: 'The Thrill Of The Thrift',
      action: 'is creating thrifting videos',
      supporters: 112,
    },
    {
      avatar: 'https://storage.googleapis.com/cursos-images/2/1/B.svg',
      name: 'Beach Talk Radio',
      action: 'is a Dinky Little Podcast',
      supporters: 1805,
    },
    {
      initials: 'SP',
      name: 'Simple Politics',
      action: 'is helping people have better conversations about politics',
      supporters: 0,
    },
  ];
</script>

<svelte:head>
  <title>Fund Your Creative Work</title>
  <meta name="description" content="Landing page clone" />
</svelte:head>

<Header />

<main>
  <div class="hero-container">
    <Hero />
    <div class="creator-cards-container">
      <div style="top: 10%; left: 5%; transform: rotate(-5deg);">
        <CreatorCard creator={creators[0]} />
      </div>
      <div style="top: 40%; left: 10%; transform: rotate(3deg);">
        <CreatorCard creator={creators[1]} />
      </div>
      <div style="top: 70%; left: 5%; transform: rotate(-3deg);">
        <CreatorCard creator={creators[2]} />
      </div>
      <div style="top: 15%; right: 5%; transform: rotate(5deg);">
        <CreatorCard creator={creators[3]} />
      </div>
      <div style="top: 45%; right: 10%; transform: rotate(-2deg);">
        <CreatorCard creator={creators[4]} />
      </div>
      <div style="top: 75%; right: 5%; transform: rotate(2deg);">
        <CreatorCard creator={creators[5]} />
      </div>
    </div>
  </div>
</main>

<style>
  main {
    position: relative;
  }
  .hero-container {
    position: relative;
    max-width: 1200px;
    margin: 0 auto;
    padding-bottom: 5rem; /* Add some space at the bottom */
  }
  .creator-cards-container {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none; /* Allows clicking through the container */
  }
  .creator-cards-container > div {
    position: absolute;
    pointer-events: all; /* Enable pointer events for the cards */
  }

  /* Responsive adjustments */
  @media (max-width: 1024px) {
    .creator-cards-container {
      display: none; /* Hide cards on smaller screens for simplicity */
    }
  }
</style>
