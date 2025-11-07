<script lang="ts">
  const events = [
    {
      image: 'https://images.unsplash.com/photo-1511795409834-ef04bbd51622?q=80&w=2940&auto=format&fit=crop',
      title: 'Festa Major de Maig',
      date: '10-14 de Mayo',
      description: 'La celebración más grande de la ciudad con música, desfiles y fuegos artificiales.',
    },
    {
      image: 'https://images.unsplash.com/photo-1514525253161-7a46d19cd819?q=80&w=2874&auto=format&fit=crop',
      title: 'Festival de Jazz de Lleida',
      date: '2-5 de Junio',
      description: 'Disfruta de los mejores artistas de jazz nacionales e internacionales en vivo.',
    },
    {
      image: 'https://images.unsplash.com/photo-1519750015927-5aae33497d43?q=80&w=2940&auto=format&fit=crop',
      title: 'Noche de San Juan',
      date: '23 de Junio',
      description: 'Hogueras, música y tradición en la noche más mágica del año.',
    },
  ];
</script>

<section id="events" class="featured-events">
  <h2>Eventos Destacados</h2>
  <div class="events-grid">
    {#each events as event}
      <div class="event-card">
        <img src={event.image} alt={event.title} />
        <div class="card-content">
          <h3>{event.title}</h3>
          <p class="date">{event.date}</p>
          <p>{event.description}</p>
        </div>
      </div>
    {/each}
  </div>
</section>

<style>
  .featured-events {
    padding: 4rem 2rem;
    text-align: center;
  }

  h2 {
    font-size: 2.5rem;
    margin-bottom: 3rem;
    color: var(--primary-color);
  }

  .events-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    max-width: 1200px;
    margin: 0 auto;
  }

  .event-card {
    background-color: #fff;
    border-radius: 1rem;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
    overflow: hidden;
    text-align: left;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .event-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
  }

  .event-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }

  .card-content {
    padding: 1.5rem;
  }

  h3 {
    font-size: 1.5rem;
    margin: 0 0 0.5rem;
  }

  .date {
    font-weight: bold;
    color: var(--accent-color);
    margin-bottom: 1rem;
  }

  p {
    color: #555;
    line-height: 1.6;
  }
</style>
