<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Le Ptit Bain — En construction</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Oswald:wght@700&family=IBM+Plex+Mono:wght@400&display=swap" rel="stylesheet">
<style>
* { margin: 0; padding: 0; box-sizing: border-box; }

:root {
  --noir:  #0D0D0D;
  --blanc: #F0EBE0;
  --rouge: #CC1100;
}

html, body {
  height: 100%;
}

body {
  background: var(--noir);
  color: var(--blanc);
  font-family: 'IBM Plex Mono', monospace;
  display: grid;
  grid-template-rows: 1fr auto;
  min-height: 100vh;
  overflow: hidden;
}

/* Grand cercle rouge en arrière-plan */
.bg-circle {
  position: fixed;
  width: 600px;
  height: 600px;
  border-radius: 50%;
  background: var(--rouge);
  top: -200px;
  right: -120px;
  pointer-events: none;
  z-index: 0;
}

/* Coin noir qui recouvre le cercle */
.bg-wedge {
  position: fixed;
  top: 0; right: 0;
  width: 0; height: 0;
  border-top: 480px solid var(--noir);
  border-left: 640px solid transparent;
  pointer-events: none;
  z-index: 1;
}

/* Contenu principal */
main {
  position: relative;
  z-index: 2;
  display: grid;
  grid-template-columns: 64px 1fr;
  align-items: end;
  padding: 72px 80px;
  gap: 40px;
}

.side-label {
  font-size: 10px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: rgba(240,235,224,0.28);
  writing-mode: vertical-rl;
  white-space: nowrap;
}

.content {}

.eyebrow {
  font-size: 11px;
  letter-spacing: 0.22em;
  text-transform: uppercase;
  color: rgba(240,235,224,0.4);
  margin-bottom: 40px;
  display: flex;
  align-items: center;
  gap: 12px;
}

.eyebrow::before {
  content: '';
  width: 8px;
  height: 8px;
  background: var(--rouge);
  display: inline-block;
  flex-shrink: 0;
}

h1 {
  font-family: 'Oswald', sans-serif;
  font-weight: 700;
  font-size: clamp(72px, 12vw, 160px);
  line-height: 0.88;
  text-transform: uppercase;
  letter-spacing: -0.02em;
}

h1 .red { color: var(--rouge); }

.tagline {
  margin-top: 48px;
  font-size: 13px;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: rgba(240,235,224,0.5);
  max-width: 480px;
  line-height: 1.8;
}

.contact {
  margin-top: 40px;
  display: flex;
  align-items: center;
  gap: 24px;
}

.contact a {
  font-size: 12px;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: var(--blanc);
  text-decoration: none;
  border-bottom: 1px solid rgba(240,235,224,0.25);
  padding-bottom: 2px;
  transition: border-color 0.2s;
}

.contact a:hover { border-color: var(--rouge); color: var(--rouge); }

.contact-sep {
  width: 1px;
  height: 16px;
  background: rgba(240,235,224,0.15);
}

/* Footer */
footer {
  position: relative;
  z-index: 2;
  border-top: 3px solid var(--rouge);
  padding: 20px 80px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.footer-brand {
  font-family: 'Oswald', sans-serif;
  font-weight: 700;
  font-size: 15px;
  text-transform: uppercase;
  letter-spacing: 0.06em;
  display: flex;
  align-items: center;
  gap: 10px;
}

.footer-dot {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: var(--rouge);
}

.footer-meta {
  font-size: 10px;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: rgba(240,235,224,0.25);
}
</style>
</head>
<body>

<div class="bg-circle"></div>
<div class="bg-wedge"></div>

<main>
  <div class="side-label">LE PTIT BAIN · LABO ARGENTIQUE · ÎLE SAINT-LOUIS</div>

  <div class="content">
    <div class="eyebrow">En construction</div>
    <h1>
      BIENTÔT<br>
      <span class="red">OUVERT.</span>
    </h1>
    <p class="tagline">
      Laboratoire argentique partagé · Île Saint-Louis · Paris<br>
      Adhésion sur candidature · Ouverture 2026
    </p>
    <div class="contact">
      <a href="mailto:contact@leptitbain.fr">contact@leptitbain.fr</a>
      <div class="contact-sep"></div>
      <a href="https://instagram.com/leptitbain" target="_blank">Instagram</a>
    </div>
  </div>
</main>

<footer>
  <div class="footer-brand">
    <div class="footer-dot"></div>
    Le Ptit Bain
  </div>
  <div class="footer-meta">Association Loi 1901 · Paris 4e</div>
</footer>

</body>
</html>
