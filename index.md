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
    .animated-title span {
      display: block;
      transition: opacity 1s ease;
      animation-duration: 6s;
      animation-iteration-count: infinite;
    }
    .print {
      font-family: 'Arial', sans-serif;
      animation-name: fadeOutIn;
    }
    .cursive {
      font-family: 'Pacifico', cursive;
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      animation-name: fadeInOut;
    }
    @keyframes fadeOutIn {
      0%, 40%, 100% { opacity: 1; }
      50%, 90% { opacity: 0; }
    }
    @keyframes fadeInOut {
      0%, 40%, 100% { opacity: 0; }
      50%, 90% { opacity: 1; }
    }
  </style>
</head>
<body>
  <div class="header-container">
    <img src="images/left.JPG" alt="Left Photo" class="header-photo left-photo" />
    <h1 class="animated-title">
      <span class="print">The Henderson's</span>
      <span class="cursive">The Henderson's</span>
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
  <div class="table-grid" id="tableGrid">
    <!-- Table 1 -->
    <div class="table-card" data-names="abigail newman,alex cheatham,alex massman,brailyn henderson,hailey henderson,jada jones,lucas newman,traidyn henderson">
      <div class="table" data-table-number="1">
        <h2>Table 1</h2>
      </div>
      <ul class="guest-list">
        <li>Abigail Newman</li>
        <li>Alex Cheatham</li>
        <li>Alex Massman</li>
        <li>Brailyn Henderson</li>
        <li>Hailey Henderson</li>
        <li>Jada Jones</li>
        <li>Lucas Newman</li>
        <li>Traidyn Henderson</li>
      </ul>
    </div>
    <!-- Table 2 -->
    <div class="table-card" data-names="ascencion guerrero,efrain ledesma,efrain zubiate ledesma,etelvina guerrero,linda guerrero,sebastian guerrero,sergio guerrero,trista wilson">
      <div class="table" data-table-number="2">
        <h2>Table 2</h2>
      </div>
      <ul class="guest-list">
        <li>Ascencion Guerrero</li>
        <li>Efrain Ledesma</li>
        <li>Efrain Zubiate Ledesma</li>
        <li>Etelvina Guerrero</li>
        <li>Linda Guerrero</li>
        <li>Sebastian Guerrero</li>
        <li>Sergio Guerrero</li>
        <li>Trista Wilson</li>
      </ul>
    </div>
    <!-- Table 3 -->
    <div class="table-card" data-names="abby rosenbaum,cory chase,lance walley,jordan assel,kayla russell,kyle rosenbaum,michael russell,millie assel">
      <div class="table" data-table-number="3">
        <h2>Table 3</h2>
      </div>
      <ul class="guest-list">
        <li>Abby Rosenbaum</li>
        <li>Cory Chase</li>
        <li>Jordan Assel</li>
        <li>Kayla Russell</li>
        <li>Kyle Rosenbaum</li>
        <li>Lance Walley</li>
        <li>Michael Russell</li>
        <li>Millie Assel</li>
      </ul>
    </div>
    <!-- Table 4 -->
    <div class="table-card" data-names="dilyn fenton,lena yoder,cadence henderson,joseph henderson,chris fenton,michelle henderson,stephanie henderson,timmy henderson">
      <div class="table" data-table-number="4">
        <h2>Table 4</h2>
      </div>
      <ul class="guest-list">
        <li>Cadence Henderson</li>
        <li>Chris Fenton</li>
        <li>Dilyn Fenton</li>
        <li>Joseph Henderson</li>
        <li>Lena Yoder</li>
        <li>Michelle Henderson</li>
        <li>Stephanie Henderson</li>
        <li>Timmy Henderson</li>
      </ul>
    </div>
    <!-- Table 5 -->
    <div class="table-card" data-names="gemma gonzalez,jose santos gonzalez,ruben angel gamboa,santos gonzalez,tanya gonzalez,al parker,mari-cruz parker,allison gandara">
      <div class="table" data-table-number="5">
        <h2>Table 5</h2>
      </div>
      <ul class="guest-list">
        <li>Al Parker</li>
        <li>Allison Gandara</li>
        <li>Gemma Gonzalez</li>
        <li>Jose Santos Gonzalez</li>
        <li>Mari-Cruz Parker</li>
        <li>Ruben Angel Gamboa</li>
        <li>Santos Gonzalez</li>
        <li>Tanya Gonzalez</li>
      </ul>
    </div>
    <!-- Table 6 -->
    <div class="table-card" data-names="andre sidney,laura mcdonald,justin gorham,kurtis nanninga,laceta wright,telia hopkins,mitch wright,tiffany gorham">
      <div class="table" data-table-number="6">
        <h2>Table 6</h2>
      </div>
      <ul class="guest-list">
        <li>Andre Sidney</li>
        <li>Justin Gorham</li>
        <li>Kurtis Nanninga</li>
        <li>Laceta Wright</li>
        <li>Laura McDonald</li>
        <li>Mitch Wright</li>
        <li>Telia Hopkins</li>
        <li>Tiffany Gorham</li>
      </ul>
    </div>
    <!-- Table 7 -->
    <div class="table-card" data-names="jennifer kelly,sean kelly,jason prewitt,jennifer conrad,jon conrad,katie prewitt,matt link,tyler blake">
      <div class="table" data-table-number="7">
        <h2>Table 7</h2>
      </div>
      <ul class="guest-list">
        <li>Jason Prewitt</li>
        <li>Jennifer Conrad</li>
        <li>Jennifer Kelly</li>
        <li>Jon Conrad</li>
        <li>Katie Prewitt</li>
        <li>Matt Link</li>
        <li>Sean Kelly</li>
        <li>Tyler Blake</li>
      </ul>
    </div>
    <!-- Table 8 -->
    <div class="table-card" data-names="elizabeth gonzalez,ester castaneda,felicia scheuring,kitty rosas,laura gutierrez,salvador gonzalez,susie howell,virginia siordia">
      <div class="table" data-table-number="8">
        <h2>Table 8</h2>
      </div>
      <ul class="guest-list">
        <li>Elizabeth Gonzalez</li>
        <li>Ester Castaneda</li>
        <li>Felicia Scheuring</li>
        <li>Kitty Rosas</li>
        <li>Laura Gutierrez</li>
        <li>Salvador Gonzalez</li>
        <li>Susie Howell</li>
        <li>Virginia Siordia</li>
      </ul>
    </div>
    <!-- Table 9 -->
    <div class="table-card" data-names="angelica philpot,beatrice gonzalez,carly philpot,carlos philpot,daniella philpot,jacob philpot,lupita felix,henry felix">
      <div class="table" data-table-number="9">
        <h2>Table 9</h2>
      </div>
      <ul class="guest-list">
        <li>Angelica Philpot</li>
        <li>Beatrice Gonzalez</li>
        <li>Carly Philpot</li>
        <li>Carlos Philpot</li>
        <li>Daniella Philpot</li>
        <li>Henry Felix</li>
        <li>Jacob Philpot</li>
        <li>Lupita Felix</li>
      </ul>
    </div>
    <!-- Table 10 -->
    <div class="table-card" data-names="bernadette wildman,lana montgomery,gwen ring,martin montgomery,mechelle montgomery,mia montgomery,sasha ring,xander ring">
      <div class="table" data-table-number="10">
        <h2>Table 10</h2>
      </div>
      <ul class="guest-list">
        <li>Bernadette Wildman</li>
        <li>Gwen Ring</li>
        <li>Lana Montgomery</li>
        <li>Martin Montgomery</li>
        <li>Mechelle Montgomery</li>
        <li>Mia Montgomery</li>
        <li>Sasha Ring</li>
        <li>Xander Ring</li>
      </ul>
    </div>
    <!-- Table 11 -->
    <div class="table-card" data-names="bellamy armenta,crystal armenta,kendrick micheal,martha armenta,olivia hutchinson,thomas armenta">
      <div class="table" data-table-number="11">
        <h2>Table 11</h2>
      </div>
      <ul class="guest-list">
        <li>Bellamy Armenta</li>
        <li>Crystal Armenta</li>
        <li>Kendrick Micheal</li>
        <li>Martha Armenta</li>
        <li>Olivia Hutchinson</li>
        <li>Thomas Armenta</li>
      </ul>
    </div>
    <!-- Table 12 -->
    <div class="table-card" data-names="brandy sunderland,claire henderson,connor henderson,darlene henderson,elizabeth johnson,rob henderson,tamitha henderson,terri simons">
      <div class="table" data-table-number="12">
        <h2>Table 12</h2>
      </div>
      <ul class="guest-list">
        <li>Brandy Sunderland</li>
        <li>Claire Henderson</li>
        <li>Connor Henderson</li>
        <li>Darlene Henderson</li>
        <li>Elizabeth Johnson</li>
        <li>Rob Henderson</li>
        <li>Tamitha Henderson</li>
        <li>Terri Simons</li>
      </ul>
    </div>
  </div>
  <button id="backToTop" title="Back to Top">↑ Top</button>
  <script>
    document.addEventListener('DOMContentLoaded', () => {
      const searchInput = document.getElementById('searchInput');
      const matchedTableDiv = document.getElementById('matchedTable');
      const tableGrid = document.getElementById('tableGrid');
      const tableCards = Array.from(document.querySelectorAll('.table-card'));
      const backToTopButton = document.getElementById('backToTop');
      let matchedCard = null;
      // Sort guest lists within each table alphabetically
      tableCards.forEach(card => {
        const ul = card.querySelector('.guest-list');
        const listItems = Array.from(ul.querySelectorAll('li'));
        listItems.sort((a, b) => a.textContent.toLowerCase().localeCompare(b.textContent.toLowerCase()));
        ul.innerHTML = '';
        listItems.forEach(li => ul.appendChild(li));
      });
      // Sort tables by table number
      const sortedCards = tableCards.sort((a, b) => {
        const aNum = parseInt(a.querySelector('.table').getAttribute('data-table-number'), 10);
        const bNum = parseInt(b.querySelector('.table').getAttribute('data-table-number'), 10);
        return aNum - bNum;
      });
      tableGrid.innerHTML = '';
      sortedCards.forEach(card => tableGrid.appendChild(card));
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
