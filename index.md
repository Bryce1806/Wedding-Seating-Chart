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
  </style>
</head>
<body>
  <h1>Welcome to the Wedding Seating Chart</h1>

  <div class="search-container">
    <div id="matchedTable" class="matched-table"></div>
    <input type="text" id="searchInput" placeholder="Search for a guest name..." />
  </div>

  <div class="table-grid" id="tableGrid">
    <!-- Table 1 -->
    <div class="table-card" data-names="abby rosenbaum,cory chase,glance walley,jordan assel,kayla russell,kyle rosenbaum,michael russell,millie assel">
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
    <div class="table-card" data-names="al parker,allison gandara,cadence henderson,joseph henderson,mari-cruz parker,michelle henderson,stephanie henderson,timmy henderson">
      <h2>Table 2</h2>
      <ul>
        <li>Al Parker</li>
        <li>Allison Gandara</li>
        <li>Cadence Henderson</li>
        <li>Joseph Henderson</li>
        <li>Mari-Cruz Parker</li>
        <li>Michelle Henderson</li>
        <li>Stephanie Henderson</li>
        <li>Timmy Henderson</li>
      </ul>
    </div>
    <!-- Table 3 -->
    <div class="table-card" data-names="ashley,jason prewitt,jennifer conrad,jon conrad,katie prewitt,matt link,tyler blake">
      <h2>Table 3</h2>
      <ul>
        <li>Ashley</li>
        <li>Jason Prewitt</li>
        <li>Jennifer Conrad</li>
        <li>Jon Conrad</li>
        <li>Katie Prewitt</li>
        <li>Matt Link</li>
        <li>Tyler Blake</li>
      </ul>
    </div>
    <!-- Table 4 -->
    <div class="table-card" data-names="abigail newman,alex cheatham,alex massman,brailyn henderson,hailey henderson,lana montgomery,lucas newman,traidyn henderson">
      <h2>Table 4</h2>
      <ul>
        <li>Abigail Newman</li>
        <li>Alex Cheatham</li>
        <li>Alex Massman</li>
        <li>Brailyn Henderson</li>
        <li>Hailey Henderson</li>
        <li>Lana Montgomery</li>
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
    <div class="table-card" data-names="andre sidney,henry felix,justin gorham,kurtis nanninga,laceta wright,lupita felix,mitch wright,tiffany gorham">
      <h2>Table 6</h2>
      <ul>
        <li>Andre Sidney</li>
        <li>Henry Felix</li>
        <li>Justin Gorham</li>
        <li>Kurtis Nanninga</li>
        <li>Laceta Wright</li>
        <li>Lupita Felix</li>
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
    <div class="table-card" data-names="bellamy armenta,chris fenton,crystal armenta,kendrick micheal,lena yoder,martha armenta,olivia hutchinson,thomas armenta">
      <h2>Table 8</h2>
      <ul>
        <li>Bellamy Armenta</li>
        <li>Chris Fenton</li>
        <li>Crystal Armenta</li>
        <li>Kendrick Micheal</li>
        <li>Lena Yoder</li>
        <li>Martha Armenta</li>
        <li>Olivia Hutchinson</li>
        <li>Thomas Armenta</li>
      </ul>
    </div>
    <!-- Table 9 -->
    <div class="table-card" data-names="bernadette wildman,dilyn fenton,gwen ring,martin montgomery,mechelle montgomery,mia montgomery,sasha ring,xander ring">
      <h2>Table 9</h2>
      <ul>
        <li>Bernadette Wildman</li>
        <li>Dilyn Fenton</li>
        <li>Gwen Ring</li>
        <li>Martin Montgomery</li>
        <li>Michelle Montgomery</li>
        <li>Mia Montgomery</li>
        <li>Sasha Ring</li>
        <li>Xander Ring</li>
      </ul>
    </div>
    <!-- Table 10 -->
    <div class="table-card" data-names="gemma gonzalez,jose santos gonzalez,ruben angel gamboa,santos gonzalez,tanya gonzalez">
      <h2>Table 10</h2>
      <ul>
        <li>Gemma Gonzalez</li>
        <li>Jose Santos Gonzalez</li>
        <li>Ruben Angel Gamboa</li>
        <li>Santos Gonzalez</li>
        <li>Tanya Gonzalez</li>
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

  <script>
    const searchInput = document.getElementById('searchInput');
    const matchedTableDiv = document.getElementById('matchedTable');
    const tableCards = document.querySelectorAll('.table-card');

searchInput.addEventListener('input', function () {
  const query = this.value.toLowerCase();
  let found = false;

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
        setTimeout(() => {
          card.scrollIntoView({ behavior: 'smooth', block: 'start' });
        }, 100); // <== added delay for better UX
        found = true;
      }
    } else {
      card.classList.remove('highlight');
    }
  });

  if (!found) {
    matchedTableDiv.textContent = query ? "No match found" : "";
  }
});
  </script>
</body>
</html>
