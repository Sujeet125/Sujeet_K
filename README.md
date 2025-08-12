<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Roorkee Water — Home</title>
  <style>
    :root{--accent:#0b6e4f;--muted:#6b7280;--bg:#f7fafc}
    body{font-family:Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial; margin:0;background:var(--bg);color:#0f172a}
    .container{max-width:1100px;margin:32px auto;padding:0 20px}
    header{display:flex;align-items:center;justify-content:space-between;padding:14px 0}
    .brand{display:flex;align-items:center;gap:12px}
    .logo{width:50px;height:50px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#0b946e);display:flex;align-items:center;justify-content:center;color:white;font-weight:700}
    nav a{margin-left:18px;color:var(--muted);text-decoration:none}
    .hero{background:white;border-radius:14px;padding:28px;box-shadow:0 6px 20px rgba(9,30,66,0.06);display:grid;grid-template-columns:1fr 420px;gap:24px}
    .hero h1{margin:0;font-size:28px}
    .hero p{color:var(--muted);margin:10px 0 18px}
    .cta-row{display:flex;gap:12px}
    .btn{background:var(--accent);color:white;padding:10px 14px;border-radius:10px;text-decoration:none;display:inline-block}
    .ghost{background:transparent;border:1px solid #e6eef0;color:var(--accent);padding:10px 14px;border-radius:10px}
    .card{background:#fff;padding:16px;border-radius:12px;box-shadow:0 4px 14px rgba(11,14,21,0.04)}
    .stats{display:flex;gap:12px;margin-top:12px}
    .stat{flex:1;text-align:center}
    .grid{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-top:18px}
    .map{height:300px;border-radius:10px;overflow:hidden}
    footer{margin-top:24px;text-align:center;color:var(--muted)}
    @media(max-width:900px){.hero{grid-template-columns:1fr;}.grid{grid-template-columns:1fr;}.map{height:220px}}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">RW</div>
        <div>
          <div style="font-weight:700">Roorkee Water</div>
          <div style="font-size:12px;color:var(--muted)">Safe • Smart • Flood-Aware</div>
        </div>
      </div>
      <nav>
        <a href="#features">Features</a>
        <a href="#map">Map</a>
        <a href="#report">Report</a>
        <a href="#about">About</a>
      </nav>
    </header>

    <section class="hero">
      <div>
        <h1>Report and track Roorkee's water, flood, and canal problems</h1>
        <p>This app helps you report leaks, waterlogging, floods, canal blockages, and water quality issues. It connects citizens, engineers, IIT Roorkee experts, and the municipal team for faster solutions — especially during the monsoon and flood season.</p>
        <div class="cta-row">
          <a class="btn" href="#report">Report an issue</a>
          <a class="ghost" href="#map">View live map</a>
        </div>

        <div style="margin-top:18px" class="card">
          <div style="font-weight:600">Quick stats</div>
          <div class="stats">
            <div class="stat"><div style="font-size:18px">1,240</div><div style="font-size:12px;color:var(--muted)">Reports (last 6 mo)</div></div>
            <div class="stat"><div style="font-size:18px">78%</div><div style="font-size:12px;color:var(--muted)">Avg resolution rate</div></div>
            <div class="stat"><div style="font-size:18px">16 hrs</div><div style="font-size:12px;color:var(--muted)">Median time to first action</div></div>
          </div>
        </div>

        <div style="margin-top:18px" class="grid">
          <div class="card"><strong>Leak & pipe bursts</strong><div style="font-size:13px;color:var(--muted);margin-top:6px">Report pipe leaks and bursts with photo & location.</div></div>
          <div class="card"><strong>Flood & waterlogging</strong><div style="font-size:13px;color:var(--muted);margin-top:6px">Mark flooded areas or blocked drains before and during rains.</div></div>
          <div class="card"><strong>Canal & intake blockages</strong><div style="font-size:13px;color:var(--muted);margin-top:6px">Report silt, debris, or flood damage in the Upper Ganga Canal or feeders.</div></div>
          <div class="card"><strong>Water quality</strong><div style="font-size:13px;color:var(--muted);margin-top:6px">Request testing and see lab results.</div></div>
        </div>
      </div>

      <aside class="card">
        <div style="font-weight:600;margin-bottom:8px">Live map</div>
        <div id="map" class="map">
          <iframe title="Roorkee map placeholder" src="https://www.openstreetmap.org/export/embed.html?bbox=77.8534%2C29.8498%2C77.8950%2C29.8740&amp;layer=mapnik" style="border:0;width:100%;height:100%"></iframe>
        </div>
        <div style="margin-top:12px">
          <button class="btn" onclick="openReport()">Report now</button>
        </div>
      </aside>
    </section>

    <section style="margin-top:18px;display:grid;grid-template-columns:1fr 320px;gap:18px">
      <div class="card" id="features">
        <h3 style="margin-top:0">How it helps</h3>
        <ol>
          <li>Collects geo-tagged reports on leaks, floods, canal issues, and water quality.</li>
          <li>Shows live flood and blockage alerts to help residents avoid danger zones.</li>
          <li>Connects reports to municipal teams and IIT Roorkee experts for quick action.</li>
          <li>Tracks fixes and keeps citizens updated on progress.</li>
        </ol>
      </div>

      <div class="card" id="report">
        <h4 style="margin-top:0">Fast report</h4>
        <p style="font-size:13px;color:var(--muted)">Add a photo, choose issue type (leak, flood, canal blockage, dirty water) and send. You can stay anonymous.</p>
        <form onsubmit="event.preventDefault();fakeSubmit()">
          <label style="font-size:13px">Issue type</label>
          <select required style="width:100%;padding:8px;margin-top:6px;border-radius:8px">
            <option>Leak / Burst pipe</option>
            <option>Flooded street / Waterlogging</option>
            <option>Canal blockage / Silt</option>
            <option>Contaminated water</option>
            <option>Other</option>
          </select>
          <label style="font-size:13px;margin-top:8px;display:block">Photo (optional)</label>
          <input type="file" accept="image/*" style="margin-top:6px" />
          <button class="btn" style="width:100%;margin-top:10px" type="submit">Submit report</button>
        </form>
      </div>
    </section>

    <footer>
      <div style="font-size:13px;color:var(--muted)">Built for Roorkee — works with IIT Roorkee, Roorkee Municipal Council, and canal engineers to keep water safe and flood risks low.</div>
      <div style="margin-top:8px;font-size:12px;color:var(--muted)">© Roorkee Water • Designed for community action</div>
    </footer>
  </div>

  <script>
    function openReport(){location.hash = '#report';document.getElementById('report').scrollIntoView({behavior:'smooth'});}
    function fakeSubmit(){alert('Thanks — report submitted (demo). In the real app this sends details to the right team.');}
  </script>
</body>
</html>
