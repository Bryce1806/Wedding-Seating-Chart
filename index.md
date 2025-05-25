<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Wedding Seating Chart</title>
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
  <div class="table-grid">
    <!-- Repeat this block for tables 1 to 12 -->
    <div class="table-card">
      <h2>Table 1</h2>
      <ul>
        <li>Guest Name 1</li>
        <li>Guest Name 2</li>
        <li>Guest Name 3</li>
      </ul>
    </div>
    <!-- Add more table-card divs below for Tables 2 to 12 -->
    <!-- Example for Table 2 -->
    <div class="table-card">
      <h2>Table 2</h2>
      <ul>
        <li>Guest Name A</li>
        <li>Guest Name B</li>
        <li>Guest Name C</li>
      </ul>
    </div>
    <!-- Continue through Table 12 -->
  </div>
</body>
</html>

