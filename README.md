<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Status</title>
  <link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg:      #fff5f7;
      --surface: #ffffff;
      --pink-3:  #f472b6;
      --text:    #3d1a26;
      --muted:   #b07090;
      --border:  #fce7ef;
      --radius:  14px;
      --mono:    'Share Tech Mono', 'Courier New', monospace;
    }

    .msg-bar {
      position: fixed;
      top: 0; left: 0; right: 0;
      background: #fce7ef;
      color: #c2185b;
      font-family: var(--mono);
      font-size: 0.72rem;
      letter-spacing: 0.16em;
      text-transform: uppercase;
      text-align: center;
      padding: 10px;
      border-bottom: 1px solid #f9c8db;
      z-index: 50;
    }

    body {
      font-family: var(--mono);
      background: var(--bg);
      min-height: 100vh;
      display: flex;
      align-items: flex-start;
      justify-content: center;
      padding: 100px 20px 60px;
      color: var(--text);
    }

    .wrapper { width: 100%; max-width: 560px; }

    header { margin-bottom: 28px; }

    header h1 {
      font-family: var(--mono);
      font-weight: 400;
      font-size: 1.5rem;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      color: var(--pink-3);
    }

    header p {
      margin-top: 5px;
      font-size: 0.7rem;
      color: var(--muted);
      letter-spacing: 0.14em;
      text-transform: uppercase;
    }

    .count {
      font-size: 0.68rem;
      color: var(--muted);
      letter-spacing: 0.1em;
      margin-bottom: 14px;
    }

    .card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      overflow: hidden;
      box-shadow: 0 2px 24px rgba(244,114,182,0.07);
    }

    table { width: 100%; border-collapse: collapse; }

    thead th {
      padding: 13px 22px;
      text-align: left;
      font-family: var(--mono);
      font-size: 0.65rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--muted);
      font-weight: 400;
      background: var(--bg);
      border-bottom: 1px solid var(--border);
    }

    tbody tr {
      border-bottom: 1px solid var(--border);
      transition: background 0.12s;
    }
    tbody tr:last-child { border-bottom: none; }
    tbody tr:hover { background: #fff0f5; }

    td {
      padding: 13px 22px;
      font-family: var(--mono);
      font-size: 0.82rem;
    }

    td.code { color: var(--text); letter-spacing: 0.05em; }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 7px;
      padding: 3px 10px;
      border-radius: 4px;
      font-family: var(--mono);
      font-size: 0.72rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      background: #fce7ef;
      color: #c2185b;
    }

    .dot {
      width: 6px; height: 6px;
      border-radius: 50%;
      background: #f472b6;
      display: inline-block;
      animation: pulse 2s infinite;
    }

    @keyframes pulse {
      0%, 100% { opacity: 1; }
      50%       { opacity: 0.3; }
    }

    .table-label {
      font-family: var(--mono);
      font-size: 0.68rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--muted);
      margin-bottom: 10px;
    }

    .badge-soon {
      background: #fdf0f7;
      color: #a0457a;
    }

    .soon-dot {
      background: #e0a0c8 !important;
      animation: none !important;
      opacity: 0.7;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(5px); }
      to   { opacity: 1; transform: none; }
    }
  </style>
</head>
<body>
<div class="msg-bar">stay safe Dr 🫂🫂🫂🫂 (</div>
<div class="wrapper">
  <header>
    <h1>// codes</h1>
  </header>

  <div class="table-label">Deliver</div>
  <div class="card">
    <table>
      <thead>
        <tr>
          <th>Code</th>
          <th>Status</th>
        </tr>
      </thead>
      <tbody id="tbody-deliver"></tbody>
    </table>
  </div>

  <div class="table-label" style="margin-top:40px">SHIN</div>
  <div class="card">
    <table>
      <thead>
        <tr>
          <th>Code</th>
          <th>Pin</th>
          <th>Status</th>
        </tr>
      </thead>
      <tbody id="tbody-shin"></tbody>
    </table>
  </div>
</div>

<script>
  const deliverRows = ['java.net.SocketTimeout','java.net.SocketTimeout','java.net.SocketTimeout','java.net.SocketTimeout','java.net.SocketTimeout','java.net.SocketTimeout','java.net.SocketTimeout','NABX69URQT32QXJP','NABX38JYZJ9NZK7F','NABX3N35MWJA5FCJ','NABX36WREWRD76FM','NABX3K7T92PLQ4ZM','NABX3RT27QEGJA4A','java.net.SocketTimeout','java.net.SocketTimeout','NABX3MQDXJAZTDZ3'];

  const shinRows = [
    { code: 'Exception E', pin: 'null' },
    { code: 'Exception E', pin: 'null' },
    { code: 'Exception E', pin: 'null' },
  ];

  function validBadge() {
    return `<span class="badge badge-valid"><span class="dot"></span>VALID</span>`;
  }

  document.getElementById('tbody-deliver').innerHTML = deliverRows.map((code, i) => `
    <tr style="animation:fadeIn 0.22s ease both;animation-delay:${i*0.05}s">
      <td class="code">${code}</td>
      <td>${validBadge()}</td>
    </tr>
  `).join('');

  document.getElementById('tbody-shin').innerHTML = shinRows.map((r, i) => `
    <tr style="animation:fadeIn 0.22s ease both;animation-delay:${i*0.05}s">
      <td class="code">${r.code}</td>
      <td class="code">${r.pin}</td>
      <td>${validBadge()}</td>
    </tr>
  `).join('');
</script>
</body>
</html>
