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
