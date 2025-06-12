<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Bryce and Cristina's Wedding Table Chart</title>
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 1rem;
      background-color: #fdf6f0;
      color: #333;
    }
    body > header {
      display: none;
    }
    h1, h2, h3 {
      text-align: center;
    }
    h1 {
      font-size: 2rem;
      margin-bottom: 1rem;
    }
    .header-container {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 1rem;
      flex-wrap: nowrap;
      margin-bottom: 1rem;
    }
    @media (max-width: 600px) {
      .header-container {
        flex-direction: column;
        flex-wrap: wrap;
        max-width: 800px;
        margin: 0 auto;
      }
      .header-container h1 {
        font-size: 1.5rem;
      }
    }
    @keyframes heartbeat {
      0% { transform: scale(1); }
      14% { transform: scale(1.3); }
      28% { transform: scale(1); }
      42% { transform: scale(1.15); }
      70% { transform: scale(1); }
      100% { transform: scale(1); }
    }
    .header-photo {
      width: 95px;
      height: 95px;
      object-fit: cover;
      object-position: center top;
      clip-path: path('M50 20 C45 0, 0 0, 0 35 C0 65, 50 100, 50 100 C50 100, 100 65, 100 35 C100 0, 55 0, 50 20 Z');
      animation: heartbeat 1.5s infinite ease-in-out;
    }
    .search-container {
      text-align: center;
      margin-bottom: 1rem;
    }
    input[type="text"] {
      padding: 0.5rem;
      font-size: 1rem;
      border-radius: 5px;
      border: 1px solid #ccc;
      width: 80%;
      max-width: 400px;
    }
    button#searchButton {
      padding: 0.5rem 1rem;
      font-size: 1rem;
      margin-left: 0.5rem;
      background-color: #9c5c5c;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button#searchButton:hover {
      background-color: #7c4545;
    }
    .matched-table {
      text-align: center;
      font-size: 1.1rem;
      font-weight: bold;
      color: #ffffff;
      background-color: #9c5c5c;
      padding: 0.5rem;
      border-radius: 5px;
      margin: 1rem auto;
      width: fit-content;
    }
    .table-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1rem;
    }
    .table-card {
      background-color: #fff;
      padding: 1rem;
      border-radius: 10px;
      box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
      scroll-margin-top: 100px;
    }
    .table-card.highlight {
      border: 2px solid #9c5c5c;
      background-color: #fff3f3;
    }
    .table-card h2 {
      margin-top: 0;
      font-size: 1.25rem;
      color: #9c5c5c;
    }
    ul {
      padding-left: 1.2rem;
    }
    li {
      line-height: 1.5;
    }
    #backToTop {
      position: fixed;
      bottom: 20px;
      right: 20px;
      z-index: 999;
      background-color: #9c5c5c;
      color: white;
      border: none;
      border-radius: 25px;
      padding: 0.75rem 1.5rem;
      font-size: 1rem;
      cursor: pointer;
      box-shadow: 0 2px 6px rgba(0, 0, 0, 0.3);
      display: none;
    }
    #backToTop:hover {
      background-color: #7c4545;
    }
.animated-title {
  position: relative;
  display: block;
  font-size: 2.5rem;
  line-height: 1.2;
  text-align: center;
  min-width: 200px;
}
.cursive {
  font-family: 'Pacifico', cursive;
  display: inline-flex;
  align-items: center;
}
.letter {
  display: inline-block;
  animation: ekgBounce 3s infinite ease-in-out; /* Increased from 1.5s to 3s */
}
/* Stagger the animation for each letter to create a slower wave effect */
.letter:nth-child(1) { animation-delay: 0s; }
.letter:nth-child(2) { animation-delay: 0.15s; }  /* Increased from 0.075s to 0.15s */
.letter:nth-child(3) { animation-delay: 0.3s; }
.letter:nth-child(4) { animation-delay: 0.45s; }
.letter:nth-child(5) { animation-delay: 0.6s; }
.letter:nth-child(6) { animation-delay: 0.75s; }
.letter:nth-child(7) { animation-delay: 0.9s; }
.letter:nth-child(8) { animation-delay: 1.05s; }
.letter:nth-child(9) { animation-delay: 1.2s; }
.letter:nth-child(10) { animation-delay: 1.35s; }
.letter:nth-child(11) { animation-delay: 1.5s; }
.letter:nth-child(12) { animation-delay: 1.65s; }
.letter:nth-child(13) { animation-delay: 1.8s; }
.letter:nth-child(14) { animation-delay: 1.95s; }
.letter:nth-child(15) { animation-delay: 2.1s; }
/* EKG waveform animation remains the same */
@keyframes ekgBounce {
  0%, 10%, 50%, 100% { transform: translateY(0); } /* Baseline */
  15% { transform: translateY(-5px); } /* P wave (small upward bump) */
  20% { transform: translateY(0); } /* Return to baseline */
  25% { transform: translateY(3px); } /* Q dip (small downward) */
  30% { transform: translateY(-20px); } /* R spike (sharp upward) */
  35% { transform: translateY(5px); } /* S dip (small downward) */
  40% { transform: translateY(0); } /* Return to baseline */
  45% { transform: translateY(-8px); } /* T wave (medium upward bump) */
}
@media (max-width: 600px) {
  .animated-title {
    font-size: 1.8rem;
  }
}
    /* Wedding-themed border for sections */
.header-container, .search-container, .table-grid {
  position: relative;
  border: 2px solid #d4af37; /* Soft gold double-line border */
  border-right: 2px solid #d4af37; /* Double line effect */
  border-left: 2px solid #d4af37; /* Double line effect */
  padding: 1rem;
  background-color: #fffaf5; /* Slightly lighter background to contrast with page */
  border-radius: 10px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  margin-bottom: 1.5rem;
}
/* Add heart accents in the corners using pseudo-elements */
.header-container::before, .search-container::before, .table-grid::before,
.header-container::after, .search-container::after, .table-grid::after {
  content: "♥";
  position: absolute;
  color: #d4af37;
  font-size: 1rem;
  line-height: 1;
}
.header-container::before, .search-container::before, .table-grid::before {
  top: -0.5rem;
  left: -0.5rem;
}
.header-container::after, .search-container::after, .table-grid::after {
  bottom: -0.5rem;
  right: -0.5rem;
}
/* Ensure the search container's content is centered and not affected by padding */
.search-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.5rem;
}
/* Adjust table-grid padding to prevent overlap with border hearts */
.table-grid {
  padding: 1.5rem;
}
/* Optional: Add a subtle hover effect to table cards to enhance the wedding feel */
.table-card:hover {
  transform: scale(1.02);
  transition: transform 0.3s ease;
}
  </style>
</head>
<body>
<div class="header-container">
  <img src="images/left.JPG" alt="Left Photo" class="header-photo left-photo" />
  <h1 class="animated-title">
    <span class="cursive">
      <span class="letter">T</span><span class="letter">h</span><span class="letter">e</span><span class="letter"> </span>
      <span class="letter">H</span><span class="letter">e</span><span class="letter">n</span><span class="letter">d</span>
      <span class="letter">e</span><span class="letter">r</span><span class="letter">s</span><span class="letter">o</span>
      <span class="letter">n</span><span class="letter">'</span><span class="letter">s</span>
    </span>
  </h1>
  <img src="images/right.JPG" alt="Right Photo" class="header-photo right-photo" />
</div>
  <h2 class="subheading">Welcome Please Find Your Seat</h2>
  <h3 class="subheading">05.31.2025</h3>
  <div class="search-container">
    <div id="matchedTable" class="matched-table"></div>
    <input type="text" id="searchInput" placeholder="Search for a guest name..." />
    <button id="searchButton">Go</button>
  </div>
  <div class="table-grid" id="tableGrid"></div>
  <button id="backToTop" title="Back to Top">↑ Top</button>
<script>
  document.addEventListener('DOMContentLoaded', () => {
    const searchInput = document.getElementById('searchInput');
    const matchedTableDiv = document.getElementById('matchedTable');
    const tableGrid = document.getElementById('tableGrid');
    const backToTopButton = document.getElementById('backToTop');
    fetch('https://sheets.googleapis.com/v4/spreadsheets/1F7znetXsbcScTniePe10MCWFPFbhI1q-E1Xrr80smG0/values/Sheet1?key=AIzaSyBhn-3TkoesLgMTNWJHbOUSJ6w78EEf_eY')
      .then(response => response.json())
      .then(data => {
        const values = data.values;
        if (!values || values.length < 1) {
          console.error('No data found');
          return;
        }
        const headers = values[0];
        const tables = [];
        for (let i = 0; i < headers.length; i++) {
          const header = headers[i].trim();
          if (header.startsWith('Table')) {
            const tableNumber = header.match(/\d+/)[0];
            const guests = [];
            for (let j = 1; j < values.length; j++) {
              const name = values[j][i] ? values[j][i].trim() : '';
              if (name) {
                guests.push(name);
              }
            }
            tables.push({ table: tableNumber, guests: guests });
          }
        }
        // Sort tables by table number
        tables.sort((a, b) => parseInt(a.table) - parseInt(b.table));
        // Generate table cards
        tableGrid.innerHTML = '';
        tables.forEach(table => {
          const tableCard = document.createElement('div');
          tableCard.className = 'table-card';
          tableCard.setAttribute('data-names', table.guests.join(',').toLowerCase());
          const tableDiv = document.createElement('div');
          tableDiv.className = 'table';
          tableDiv.setAttribute('data-table-number', table.table);
          const h2 = document.createElement('h2');
          h2.textContent = `Table ${table.table}`;
          tableDiv.appendChild(h2);
          const ul = document.createElement('ul');
          ul.className = 'guest-list';
          table.guests.sort((a, b) => a.toLowerCase().localeCompare(b.toLowerCase()));
          table.guests.forEach(guest => {
            const li = document.createElement('li');
            li.textContent = guest;
            ul.appendChild(li);
          });
          tableCard.appendChild(tableDiv);
          tableCard.appendChild(ul);
          tableGrid.appendChild(tableCard);
        });
        // Define tableCards for search
        const tableCards = Array.from(document.querySelectorAll('.table-card'));
        let matchedCard = null;
        // Search functionality
        function checkMatch(query) {
          query = query.toLowerCase().trim();
          let found = false;
          matchedCard = null;
          matchedTableDiv.textContent = '';
          tableCards.forEach(card => {
            const names = card.getAttribute('data-names').toLowerCase();
            card.classList.remove('highlight');
            if (query && names.includes(query)) {
              card.classList.add('highlight');
              if (!found) {
                const tableNumber = card.querySelector('h2').textContent;
                matchedTableDiv.textContent = `Match found at ${tableNumber}`;
                matchedCard = card;
                found = true;
              }
            }
          });
          if (query && !found) {
            matchedTableDiv.textContent = 'No match found';
          }
        }
        // Live search
        searchInput.addEventListener('input', () => {
          checkMatch(searchInput.value);
        });
        // Scroll on Enter key
        searchInput.addEventListener('keydown', (event) => {
          if (event.key === 'Enter' && matchedCard) {
            matchedCard.scrollIntoView({ behavior: 'smooth', block: 'start' });
          }
        });
        // Scroll on Go button click
        document.getElementById('searchButton').addEventListener('click', () => {
          if (matchedCard) {
            matchedCard.scrollIntoView({ behavior: 'smooth', block: 'start' });
          }
        });
      })
      .catch(error => console.error('Error fetching data:', error));
    // Back-to-top button visibility
    window.addEventListener('scroll', () => {
      backToTopButton.style.display = window.scrollY > 200 ? 'block' : 'none';
    });
    // Scroll to top on button click
    backToTopButton.addEventListener('click', () => {
      window.scrollTo({ top: 0, behavior: 'smooth' });
    });
    // Initially hide back-to-top button
    backToTopButton.style.display = 'none';
  });
</script>
</body>
</html>
