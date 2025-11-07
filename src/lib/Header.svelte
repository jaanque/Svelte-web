<header>
  <div class="logo">
    <a href="/">
      <span>Lleida.me</span>
    </a>
  </div>
  <nav>
    <ul>
      <li><a href="#events">Eventos</a></li>
      <li><a href="#how-it-works">Cómo funciona</a></li>
    </ul>
  </nav>
  <div class="actions">
    <a href="/login" class="login">Iniciar Sesión</a>
    <a href="/signup" class="signup">Registrarse</a>
  </div>
</header>

<style>
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
    background-color: #fff;
    border-bottom: 1px solid var(--border-color, #eaeaea);
  }

  .logo a {
    display: flex;
    align-items: center;
    text-decoration: none;
    color: #000;
    font-weight: bold;
    font-size: 1.5rem;
  }

  nav ul {
    display: flex;
    list-style: none;
    margin: 0;
    padding: 0;
  }

  nav li {
    margin: 0 1rem;
  }

  nav a {
    text-decoration: none;
    color: #555;
    transition: color 0.2s ease;
    font-weight: 500;
  }

  nav a:hover {
    color: var(--primary-color);
  }

  .actions {
    display: flex;
    align-items: center;
  }

  .login {
    margin-right: 1rem;
    text-decoration: none;
    color: #555;
    transition: color 0.2s ease;
    font-weight: 500;
  }

  .login:hover {
    color: var(--primary-color);
  }

  .signup {
    padding: 0.5rem 1.5rem;
    background-color: var(--accent-color);
    color: #fff;
    border-radius: 999px;
    text-decoration: none;
    transition: background-color 0.2s ease;
    font-weight: 500;
  }

  .signup:hover {
    background-color: var(--secondary-color);
  }
</style>
