<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Travel Booking</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header>
    <h1>Travel Explorer</h1>
    <nav>
      <a href="#">Home</a>
      <a href="#">Destinations</a>
      <a href="#">Flights</a>
      <a href="#">Hotels</a>
      <a href="#">Contact</a>
    </nav>
  </header>

  <main>
    <section class="search">
      <h2>Find Your Next Adventure</h2>
      <input type="text" placeholder="Search destinations..." id="searchBox" />
      <button onclick="searchDestinations()">Search</button>
    </section>

    <section class="cards" id="destinationCards">
      <!-- Destination cards will be populated here -->
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Travel Explorer</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Travel Booking</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header>
    <h1>Travel Explorer</h1>
    <nav>
      <a href="#">Home</a>
      <a href="#">Destinations</a>
      <a href="#">Flights</a>
      <a href="#">Hotels</a>
      <a href="#">Contact</a>
    </nav>
  </header>

  <main>
    <section class="search">
      <h2>Find Your Next Adventure</h2>
      <input type="text" placeholder="Search destinations..." id="searchBox" />
      <button onclick="searchDestinations()">Search</button>
    </section>

    <section class="cards" id="destinationCards">
      <!-- Destination cards will be populated here -->
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Travel Explorer</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
const destinations = [
  { name: "Paris", image: "https://source.unsplash.com/300x200/?paris" },
  { name: "Bali", image: "https://source.unsplash.com/300x200/?bali" },
  { name: "New York", image: "https://source.unsplash.com/300x200/?newyork" },
];

function searchDestinations() {
  const query = document.getElementById("searchBox").value.toLowerCase();
  const filtered = destinations.filter(dest =>
    dest.name.toLowerCase().includes(query)
  );

  const container = document.getElementById("destinationCards");
  container.innerHTML = "";

  filtered.forEach(dest => {
    container.innerHTML += `
      <div class="card">
        <img src="${dest.image}" alt="${dest.name}">
        <h3>${dest.name}</h3>
      </div>
    `;
  });
}

// Initial load
searchDestinations();
