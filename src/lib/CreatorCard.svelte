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
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1), 0 1px 3px rgba(0, 0, 0, 0.08);
    padding: 1rem;
    display: flex;
    align-items: center;
    max-width: 300px;
    margin: 1rem;
    position: absolute; /* This will be used for positioning */
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
    color: #333;
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
