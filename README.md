<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ChartJS</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>
    <div>
  <canvas id="myChart"></canvas>
</div>

<script>
  const ctx = document.getElementById('myChart');

  new Chart(ctx, {
    type: 'line',
    data: {
      labels: ['Janeiro', 'Fevereiro', 'Março', 'Abril', 'Maio', 'Junho'],
      datasets: [{
        label: 'temperatura',
        backgroundColor:`(0, 255, 255)`,
        borderColor: `#CCFF00`,
        data: [30, 29, 28, 25, 22, 21],
      },{
        label: 'umidade',
        backgroundColor:`rgb(0,0,255)`,
        borderColor: `rgb(255,0,0)`,
        data: [80, 82, 80, 85, 80, 83],
      }]
      
    },
    options: {
      scales: {
        y: {
          beginAtZero: true
        }
      }
    }
  });
</script>

