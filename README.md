<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Meet & Greet Event</title>

<style>
body {
  margin: 0;
  font-family: 'Segoe UI', sans-serif;
  scroll-behavior: smooth;
}

/* NAVBAR */
nav {
  position: fixed;
  width: 100%;
  background: white;
  padding: 15px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

nav a {
  margin: 0 15px;
  text-decoration: none;
  color: black;
  font-weight: bold;
}

/* HERO */
header {
  height: 100vh;
  background: url('https://images.unsplash.com/photo-1492684223066-81342ee5ff30') center/cover;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: white;
  text-align: center;
}

header h1 {
  font-size: 50px;
}

.btn {
  padding: 15px 25px;
  background: #d1410c;
  color: white;
  border: none;
  cursor: pointer;
}

/* SECTIONS */
section {
  padding: 80px 20px;
  text-align: center;
  opacity: 0;
  transform: translateY(40px);
  transition: 0.6s;
}

section.show {
  opacity: 1;
  transform: translateY(0);
}

.about { background: #f8f8f8; }

.gallery img {
  width: 250px;
  margin: 10px;
  border-radius: 10px;
}

.ticket {
  background: #1e0a3c;
  color: white;
}

footer {
  background: black;
  color: white;
  padding: 20px;
}
</style>
</head>

<body>

<!-- NAV -->
<nav>
  <a href="#home">Home</a>
  <a href="#about">About</a>
  <a href="#details">Details</a>
  <a href="#gallery">Gallery</a>
  <a href="#tickets">Tickets</a>
</nav>

<!-- HERO -->
<header id="home">
  <h1>Meet & Greet Experience</h1>
  <p>Join us for an unforgettable fan moment</p>
  <button class="btn">Get Tickets</button>
</header>

<!-- ABOUT -->
<section id="about" class="about">
  <h2>About The Event</h2>
  <p>This exclusive meet and greet gives fans a chance to connect, take photos, and enjoy a special experience.</p>
</section>

<!-- DETAILS -->
<section id="details">
  <h2>Event Details</h2>
  <p><strong>Date:</strong> August 20, 2026</p>
  <p><strong>Location:</strong> Pierre Part, Louisiana</p>
</section>

<!-- GALLERY -->
<section id="gallery" class="gallery">
  <h2>Gallery</h2>
  <img src="https://images.unsplash.com/photo-1515169067865-5387ec356754">
  <img src="https://images.unsplash.com/photo-1506157786151-b8491531f063">
  <img src="https://images.unsplash.com/photo-1497032205916-ac775f0649ae">
</section>

<!-- TICKETS -->
<section id="tickets" class="ticket">
  <h2>Reserve Your Spot</h2>
  <p>This is a demo — no real payment required</p>
  <button class="btn" onclick="alert('Demo ticket only!')">Buy Ticket</button>
</section>

<footer>
  <p>© 2026 Meet & Greet Project</p>
</footer>

<script>
// SCROLL ANIMATION
const sections = document.querySelectorAll("section");

window.addEventListener("scroll", () => {
  sections.forEach(sec => {
    const top = sec.getBoundingClientRect().top;
    if(top < window.innerHeight - 100){
      sec.classList.add("show");
    }
  });
});
</script>

</body>
</html>
