<header>
  <div class="logo">
    <a href="/">
      <img src="https://storage.googleapis.com/cursos-images/2/1/Nav-logo.svg" alt="Logo" />
      <span>Buy me a coffee</span>
    </a>
  </div>
  <nav>
    <ul>
      <li><a href="/faq">FAQ</a></li>
      <li><a href="/wall-of-love">Wall of ♡</a></li>
      <li><a href="/resources">Resources</a></li>
    </ul>
  </nav>
  <div class="actions">
    <div class="search">
      <input type="text" placeholder="Search creators" />
    </div>
    <a href="/login" class="login">Log in</a>
    <a href="/signup" class="signup">Sign up</a>
  </div>
</header>

<style>
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 2rem;
    background-color: #fff;
    border-bottom: 1px solid #eaeaea;
  }

  .logo a {
    display: flex;
    align-items: center;
    text-decoration: none;
    color: #000;
    font-weight: bold;
  }

  .logo img {
    height: 2rem;
    margin-right: 0.5rem;
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
  }

  .actions {
    display: flex;
    align-items: center;
  }

  .search {
    margin-right: 1rem;
  }

  .search input {
    border: 1px solid #ccc;
    border-radius: 999px;
    padding: 0.5rem 1rem;
  }

  .login {
    margin-right: 1rem;
    text-decoration: none;
    color: #555;
  }

  .signup {
    padding: 0.5rem 1rem;
    background-color: var(--accent-color);
    color: #fff;
    border-radius: 999px;
    text-decoration: none;
  }
</style>
