<script lang="ts">
  export let creator: {
    avatar: string;
    name: string;
    action: string;
    supporters: number;
    initials?: string;
  };
</script>

<div class="creator-card">
  <div class="avatar">
    {#if creator.avatar}
      <img src={creator.avatar} alt={creator.name} />
    {:else if creator.initials}
      <span>{creator.initials}</span>
    {/if}
  </div>
  <div class="info">
    <p>
      <strong>{creator.name}</strong>
      is
      {creator.action}
    </p>
    <p class="supporters">♡ {creator.supporters.toLocaleString()} supporters</p>
  </div>
</div>

<style>
  .creator-card {
    background-color: #fff;
    border-radius: 1rem;
    box-shadow: 0 4px 15px var(--shadow-color);
    padding: 1rem;
    display: flex;
    align-items: center;
    max-width: 300px;
    margin: 1rem;
    position: absolute;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    animation: float 6s ease-in-out infinite;
  }

  .creator-card:hover {
    transform: translateY(-5px) scale(1.05);
    box-shadow: 0 8px 25px var(--shadow-color);
  }

  @keyframes float {
    0% {
      transform: translateY(0px);
    }
    50% {
      transform: translateY(-10px);
    }
    100% {
      transform: translateY(0px);
    }
  }

  .avatar {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background-color: #eee;
    margin-right: 1rem;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    flex-shrink: 0;
  }

  .avatar img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .avatar span {
    font-weight: bold;
    font-size: 1.2rem;
  }

  .info p {
    margin: 0;
    line-height: 1.4;
    color: var(--text-color);
  }

  .info strong {
    color: #000;
  }

  .supporters {
    color: #555;
    font-size: 0.9rem;
    margin-top: 0.5rem;
  }
</style>
