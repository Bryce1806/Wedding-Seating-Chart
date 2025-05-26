<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Bryce and Cristina's Wedding Table Chart</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 1rem;
      background-color: #fdf6f0;
      color: #333;
    }
    h1 {
      text-align: center;
      font-size: 2rem;
      margin-bottom: 1rem;
    }
.header-container {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
  text-align: center;
  flex-wrap: nowrap;
}
@media (max-width: 600px) {
  .header-container {
    flex-direction: column;
    flex-wrap: wrap;
  }
}
@keyframes heartbeat {
  0% {
    transform: scale(1);
  }
  14% {
    transform: scale(1.3);
  }
  28% {
    transform: scale(1);
  }
  42% {
    transform: scale(1.15);
  }
  70% {
    transform: scale(1);
  }
  100% {
    transform: scale(1);
  }
}
.header-photo {
  width: 90px;
  height: 90px;
  object-fit: cover;
  object-position: center center; /* or center center depending on the photo */
  clip-path: path('M50 20 C45 0, 0 0, 0 35 C0 65, 50 100, 50 100 C50 100, 100 65, 100 35 C100 0, 55 0, 50 20 Z');
  animation: heartbeat 1.5s infinite ease-in-out;
}
.header-container h1 {
  margin: 0;
  font-size: 2rem;
}
/* Responsive adjustments for small screens */
@media (max-width: 600px) {
  .header-container {
    flex-direction: column;
  }
  .header-container {
  max-width: 800px;
  margin: 0 auto;
}
  .header-container h1 {
    font-size: 1.5rem;
  }
}
  .header-container {
  align-items: center; /* already included, good */
}
  .header-container h1 {
  line-height: 1.2; /* ensures title isn’t stretching the layout */
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
    @media (max-width: 600px) {
      h1 {
        font-size: 1.5rem;
      }
    }
    #backToTop {
  display: none; /* Hidden by default */
  position: fixed;
  bottom: 20px;
  right: 20px;
  z-index: 100;
  background-color: #9c5c5c;
  color: white;
  border: none;
  border-radius: 50%;
  width: 48px;
  height: 48px;
  font-size: 1.2rem;
  cursor: pointer;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.3);
}
#backToTop:hover {
  background-color: #7c4545;
}
    .subheading {
  text-align: center;
  font-size: 1.2rem;
  color: #666;
  margin-top: 0.5rem;
  margin-bottom: 1.5rem;
}
  </style>
</head>
<body>
<div class="header-container">
  <img src="images/left.JPG" alt="Left Photo" class="header-photo left-photo" />
  <h1>Welcome to the Wedding Seating Chart</h1>
  <img src="images/right.JPG" alt="Right Photo" class="header-photo right-photo" />
</div>
<h2 class="subheading">Find your seat and enjoy the celebration!</h2>
  
<div class="search-container">
  <div id="matchedTable" class="matched-table"></div>
  <input type="text" id="searchInput" placeholder="Search for a guest name..." />
  <button id="searchButton">Go</button>
</div>
  <div class="table-grid" id="tableGrid">
    <!-- Table 1 -->
    <div class="table-card" data-names="abby rosenbaum,cory chase,lance walley,jordan assel,kayla russell,kyle rosenbaum,michael russell,millie assel">
      <h2>Table 1</h2>
      <ul>
        <li>Abby Rosenbaum</li>
        <li>Cory Chase</li>
        <li>Lance Walley</li>
        <li>Jordan Assel</li>
        <li>Kayla Russell</li>
        <li>Kyle Rosenbaum</li>
        <li>Michael Russell</li>
        <li>Millie Assel</li>
      </ul>
    </div>
    <!-- Table 2 -->
    <div class="table-card" data-names="dilyn fenton,lena yoder,cadence henderson,joseph henderson,chris fenton,michelle henderson,stephanie henderson,timmy henderson">
      <h2>Table 2</h2>
      <ul>
        <li>Dilyn Fenton</li>
        <li>Lena Yoder</li>
        <li>Cadence Henderson</li>
        <li>Joseph Henderson</li>
        <li>Chris Fenton</li>
        <li>Michelle Henderson</li>
        <li>Stephanie Henderson</li>
        <li>Timmy Henderson</li>
      </ul>
    </div>
    <!-- Table 3 -->
    <div class="table-card" data-names="jennifer kelly,sean kelly,jason prewitt,jennifer conrad,jon conrad,katie prewitt,matt link,tyler blake">
      <h2>Table 3</h2>
      <ul>
        <li>Jennifer Kelly</li>
        <li>Sean Kelly</li>
        <li>Jason Prewitt</li>
        <li>Jennifer Conrad</li>
        <li>Jon Conrad</li>
        <li>Katie Prewitt</li>
        <li>Matt Link</li>
        <li>Tyler Blake</li>
      </ul>
    </div>
    <!-- Table 4 -->
    <div class="table-card" data-names="abigail newman,alex cheatham,alex massman,brailyn henderson,hailey henderson,jada,lucas newman,traidyn henderson">
      <h2>Table 4</h2>
      <ul>
        <li>Abigail Newman</li>
        <li>Alex Cheatham</li>
        <li>Alex Massman</li>
        <li>Brailyn Henderson</li>
        <li>Hailey Henderson</li>
        <li>Jada</li>
        <li>Lucas Newman</li>
        <li>Traidyn Henderson</li>
      </ul>
    </div>
    <!-- Table 5 -->
    <div class="table-card" data-names="ascencion guerrero,efrain ledesma,efrain zubiate ledesma,etelvina guerrero,linda guerrero,sebastian guerrero,sergio guerrero,trista wilson">
      <h2>Table 5</h2>
      <ul>
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
    <!-- Table 6 -->
    <div class="table-card" data-names="andre sidney,laura mcdonald,justin gorham,kurtis nanninga,laceta wright,telia hopkins,mitch wright,tiffany gorham">
      <h2>Table 6</h2>
      <ul>
        <li>Andre Sidney</li>
        <li>Laura McDonald</li>
        <li>Justin Gorham</li>
        <li>Kurtis Nanninga</li>
        <li>Laceta Wright</li>
        <li>Telia Hopkins</li>
        <li>Mitch Wright</li>
        <li>Tiffany Gorham</li>
      </ul>
    </div>
    <!-- Table 7 -->
    <div class="table-card" data-names="brandy sunderland,claire henderson,connor henderson,darlene henderson,elizabeth johnson,rob henderson,tamitha henderson,terri simons">
      <h2>Table 7</h2>
      <ul>
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
    <!-- Table 8 -->
    <div class="table-card" data-names="bellamy armenta,crystal armenta,kendrick micheal,martha armenta,olivia hutchinson,thomas armenta">
      <h2>Table 8</h2>
      <ul>
        <li>Bellamy Armenta</li>
        <li>Crystal Armenta</li>
        <li>Kendrick Micheal</li>
        <li>Martha Armenta</li>
        <li>Olivia Hutchinson</li>
        <li>Thomas Armenta</li>
      </ul>
    </div>
    <!-- Table 9 -->
    <div class="table-card" data-names="bernadette wildman,lana montgomery,gwen ring,martin montgomery,mechelle montgomery,mia montgomery,sasha ring,xander ring">
      <h2>Table 9</h2>
      <ul>
        <li>Bernadette Wildman</li>
        <li>Lana Montgomery</li>
        <li>Gwen Ring</li>
        <li>Martin Montgomery</li>
        <li>Michelle Montgomery</li>
        <li>Mia Montgomery</li>
        <li>Sasha Ring</li>
        <li>Xander Ring</li>
      </ul>
    </div>
    <!-- Table 10 -->
    <div class="table-card" data-names="gemma gonzalez,jose santos gonzalez,ruben angel gamboa,santos gonzalez,tanya gonzalez,al parker,mari-cruz parker,allison gandara">
      <h2>Table 10</h2>
      <ul>
        <li>Gemma Gonzalez</li>
        <li>Jose Santos Gonzalez</li>
        <li>Ruben Angel Gamboa</li>
        <li>Santos Gonzalez</li>
        <li>Tanya Gonzalez</li>
        <li>Al Parker</li>
        <li>Mari-Cruz Parker</li>
        <li>Allison Gandara</li>
      </ul>
    </div>
    <!-- Table 11 -->
    <div class="table-card" data-names="angelica philpot,beatrice gonzalez,carly philpot,carlos philpot,daniella philpot,jacob philpot,laura mcdonald,telia hopkins">
      <h2>Table 11</h2>
      <ul>
        <li>Angelica Philpot</li>
        <li>Beatrice Gonzalez</li>
        <li>Carly Philpot</li>
        <li>Carlos Philpot</li>
        <li>Daniella Philpot</li>
        <li>Jacob Philpot</li>
        <li>Laura McDonald</li>
        <li>Telia Hopkins</li>
      </ul>
    </div>
    <!-- Table 12 -->
    <div class="table-card" data-names="elizabeth gonzalez,ester castaneda,felicia scheuring,kitty rosas,laura gutierrez,salvador gonzalez,susie howell,virginia siordia">
      <h2>Table 12</h2>
      <ul>
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
 </div>
 <button id="backToTop" title="Back to Top">↑ Top</button>
 
<script>
  const searchInput = document.getElementById('searchInput');
  const matchedTableDiv = document.getElementById('matchedTable');
  const tableCards = document.querySelectorAll('.table-card');
  let matchedCard = null; // Track matched card to scroll later

  // Function to check for matches and update display
  function checkMatch(query) {
    let found = false;
    matchedCard = null;

    tableCards.forEach((card) => {
      const names = card.querySelectorAll('li');
      let matchInCard = false;

      names.forEach((name) => {
        if (name.textContent.toLowerCase().includes(query)) {
          matchInCard = true;
        }
      });

      if (matchInCard) {
        card.classList.add('highlight');
        if (!found) {
          const tableNumber = card.querySelector('h2').textContent;
          matchedTableDiv.textContent = `Match found at ${tableNumber}`;
          matchedCard = card;
          found = true;
        }
      } else {
        card.classList.remove('highlight');
      }
    });

    if (!found) {
      matchedTableDiv.textContent = query ? "No match found" : "";
    }
  }

  // Live feedback while typing
  searchInput.addEventListener('input', function () {
    const query = this.value.toLowerCase();
    checkMatch(query);
  });

  // Scroll on Enter
  searchInput.addEventListener('keydown', function (event) {
    if (event.key === 'Enter' && matchedCard) {
      matchedCard.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }
  });

  // Scroll on Go button click
  document.getElementById('searchButton').addEventListener('click', function () {
    if (matchedCard) {
      matchedCard.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }
  });
  // Sort each table's list items alphabetically by first name
document.querySelectorAll('.table-card ul').forEach((ul) => {
  const listItems = Array.from(ul.querySelectorAll('li'));

  listItems.sort((a, b) => {
    const nameA = a.textContent.toLowerCase();
    const nameB = b.textContent.toLowerCase();
    return nameA.localeCompare(nameB);
  });

  // Clear and re-append in sorted order
  ul.innerHTML = '';
  listItems.forEach((li) => ul.appendChild(li));
});
const backToTopButton = document.getElementById('backToTop');

// Show/hide button on scroll
window.addEventListener('scroll', () => {
  if (window.scrollY > 300) {
    backToTopButton.style.display = 'block';
  } else {
    backToTopButton.style.display = 'none';
  }
});
// Scroll to top when clicked
backToTopButton.addEventListener('click', () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
});
</script>
</body>
</html>
