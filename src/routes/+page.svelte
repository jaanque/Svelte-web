<script lang="ts">
  import Header from '$lib/Header.svelte';
  import Hero from '$lib/Hero.svelte';
  import HowItWorks from '$lib/HowItWorks.svelte';
  import FeaturedEvents from '$lib/FeaturedEvents.svelte';
  import Benefits from '$lib/Benefits.svelte';
  import Footer from '$lib/Footer.svelte';
</script>

<svelte:head>
  <title>Lleida.me - Conectando la comunidad</title>
  <meta name="description" content="Gana recompensas y asiste a los mejores eventos de Lleida." />
</svelte:head>

<Header />

<main>
  <Hero />
  <HowItWorks />
  <FeaturedEvents />
  <Benefits />
</main>

<Footer />

<style>
  main {
    display: flex;
    flex-direction: column;
  }
</style>
