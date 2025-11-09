mkdir -p ~/Desktop/my-website
cd ~/Desktop/my-website

cat > index.html <<'EOF'
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Home</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="menu">
    <a href="compositions.html">Compositions</a>
    <a href="media.html">Media</a>
    <a href="contact.html">Contact</a>
  </div>
</body>
</html>
EOF

cat > compositions.html <<'EOF'
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Compositions</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="page">
    <h1>Compositions</h1>
  </div>
</body>
</html>
EOF

cat > media.html <<'EOF'
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Media</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="page">
    <h1>Media</h1>
  </div>
</body>
</html>
EOF

cat > contact.html <<'EOF'
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Contact</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="page">
    <h1>Contact</h1>
  </div>
</body>
</html>
EOF

cat > style.css <<'EOF'
html, body {
  margin: 0;
  padding: 0;
  background: white;
  color: black;
  font-family: Helvetica, Arial, sans-serif;
}

.menu {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 2rem;
  gap: 0.75rem;
}

.menu a {
  text-decoration: none;
  color: black;
  font-size: 1.5rem;
  transition: opacity 0.2s ease;
}

.menu a:hover {
  opacity: 0.6;
}

.page {
  padding: 2rem;
}

.page h1 {
  font-weight: normal;
  font-size: 2rem;
  margin: 0;
}
EOF
