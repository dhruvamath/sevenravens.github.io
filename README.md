# sevenravens.github.io
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Helvetia Blog</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <header class="site-header">
      <h1 class="site-title">Helvetia</h1>
      <nav class="site-nav">
        <a href="#compositions">Compositions</a>
        <a href="#ideas">Ideas</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>
    <main class="sections">
      <section id="compositions" class="section-card">
        <h2>Compositions</h2>
      </section>
      <section id="ideas" class="section-card">
        <h2>Ideas</h2>
      </section>
      <section id="contact" class="section-card">
        <h2>Contact</h2>
      </section>
    </main>
    <footer class="site-footer">
      <p>&copy; <span id="year"></span> Helvetia Blog</p>
    </footer>
    <script>
      document.getElementById("year").textContent = new Date().getFullYear();
    </script>
  </body>
</html>
:root {
  color-scheme: light;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  background-color: #f5f6f7;
  color: #1f1f1f;
}

*,
*::before,
*::after {
  box-sizing: border-box;
}

html,
body {
  margin: 0;
  min-height: 100%;
}

body {
  display: flex;
  flex-direction: column;
  align-items: stretch;
}

.site-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 2rem clamp(1.5rem, 2.5vw, 3rem);
  border-bottom: 1px solid rgba(0, 0, 0, 0.08);
  background-color: #ffffff;
}

.site-title {
  margin: 0;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  font-size: clamp(1.4rem, 2vw, 2.4rem);
}

.site-nav {
  display: flex;
  gap: clamp(1.5rem, 2.5vw, 3rem);
}

.site-nav a {
  font-size: 0.9rem;
  text-transform: uppercase;
  letter-spacing: 0.28em;
  text-decoration: none;
  color: inherit;
  position: relative;
  padding-bottom: 0.4rem;
}

.site-nav a::after {
  content: "";
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: 2px;
  transform: scaleX(0);
  transform-origin: center;
  transition: transform 0.2s ease-in-out;
  background-color: currentColor;
}

.site-nav a:focus-visible::after,
.site-nav a:hover::after {
  transform: scaleX(1);
}

.sections {
  flex: 1;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: clamp(1rem, 4vw, 4rem);
  padding: clamp(4rem, 8vw, 8rem) clamp(1.5rem, 6vw, 6rem);
}

.section-card {
  border: 1px solid rgba(0, 0, 0, 0.1);
  border-radius: 12px;
  background-color: #ffffff;
  padding: clamp(2.5rem, 4vw, 5rem);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.section-card h2 {
  margin: 0;
  font-weight: 400;
  letter-spacing: 0.2em;
  text-transform: uppercase;
}

.section-card:hover,
.section-card:focus-within {
  transform: translateY(-4px);
  box-shadow: 0 18px 30px -18px rgba(0, 0, 0, 0.35);
}

.site-footer {
  padding: 1.5rem clamp(1.5rem, 2.5vw, 3rem);
  text-align: center;
  font-size: 0.85rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: rgba(0, 0, 0, 0.55);
}

@media (max-width: 640px) {
  .site-header {
    flex-direction: column;
    gap: 1rem;
  }

  .site-nav {
    width: 100%;
    justify-content: space-around;
  }
}
