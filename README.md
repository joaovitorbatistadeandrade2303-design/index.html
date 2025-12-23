# index.html
Goldpage 
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <title>GOLD Produção — Código & Sangue</title>
  <meta name="description" content="GOLD Produção — música, audiovisual e estratégia. Ouça Código & Sangue, acompanhe o canal e baixe os materiais oficiais." />
  <meta name="theme-color" content="#FFD700" />

  <!-- Favicon (usa seu logo) -->
  <link rel="icon" type="image/png" href="logo-gold.png" />

  <!-- Open Graph (preview ao compartilhar) -->
  <meta property="og:title" content="GOLD Produção — Código & Sangue" />
  <meta property="og:description" content="Onde a mente cria, o código executa. Links oficiais, músicas e materiais." />
  <meta property="og:type" content="website" />
  <!-- Se quiser preview com imagem: crie um arquivo og.png e descomente -->
  <!-- <meta property="og:image" content="og.png" /> -->

  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet" />

  <style>
    :root{
      --bg: #000;
      --panel: #0b0b0b;
      --panel2:#101010;
      --gold:#FFD700;
      --text:#f3f3f3;
      --muted:#b9b9b9;
      --line: rgba(255,215,0,.35);
      --shadow: 0 18px 60px rgba(0,0,0,.55);
      --radius: 18px;
    }
    *{ box-sizing: border-box; }
    html,body{ height:100%; }
    html{ scroll-behavior:smooth; }
    body{
      margin:0;
      background:
        radial-gradient(900px 500px at 20% 0%, rgba(255,215,0,.10), transparent 60%),
        radial-gradient(900px 600px at 80% 10%, rgba(255,215,0,.07), transparent 55%),
        linear-gradient(180deg, #000 0%, #000 35%, #050505 100%);
      color:var(--text);
      font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
    }
    .container{
      width:min(1100px, 92vw);
      margin:0 auto;
      padding:28px 0 40px;
    }

    .topbar{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:16px;
      padding:14px 18px;
      border:1px solid rgba(255,255,255,.06);
      background: rgba(10,10,10,.65);
      backdrop-filter: blur(10px);
      border-radius: 999px;
      box-shadow: var(--shadow);
      position: sticky;
      top: 14px;
      z-index: 50;
    }
    .brand{
      display:flex;
      align-items:center;
      gap:12px;
      min-width: 240px;
    }

    /* LOGO real */
    .logoImgWrap{
      width:44px; height:44px;
      border-radius: 14px;
      overflow:hidden;
      border:1px solid var(--line);
      background: rgba(255,215,0,.06);
      box-shadow: 0 0 0 1px rgba(255,215,0,.12);
      flex: 0 0 auto;
    }
    .logoImg{
      width:100%;
      height:100%;
      object-fit: cover;
      display:block;
      transform: scale(1.02);
    }

    .brand h1{
      font-family: Orbitron, sans-serif;
      font-size: 14px;
      margin:0;
      letter-spacing: .9px;
      color: var(--gold);
      line-height: 1.1;
    }
    .brand p{
      margin:0;
      font-size:12px;
      color: var(--muted);
      line-height: 1.1;
    }
    .nav{
      display:flex;
      gap:10px;
      flex-wrap:wrap;
      justify-content:flex-end;
    }
    .nav a{
      text-decoration:none;
      color: var(--muted);
      font-size: 12px;
      padding:8px 10px;
      border-radius: 999px;
      border:1px solid rgba(255,255,255,.06);
      background: rgba(0,0,0,.35);
      transition: .2s ease;
      white-space: nowrap;
    }
    .nav a:hover{
      color:#000;
      background: var(--gold);
      border-color: rgba(255,215,0,.75);
      transform: translateY(-1px);
    }

    .hero{
      margin-top: 22px;
      display:grid;
      grid-template-columns: 1.2fr .8fr;
      gap:18px;
      align-items: stretch;
    }
    @media (max-width: 920px){
      .hero{ grid-template-columns: 1fr; }
      .brand{ min-width:auto; }
      .topbar{ border-radius: 18px; }
    }

    .heroCard{
      background: linear-gradient(180deg, rgba(255,215,0,.10), rgba(255,255,255,.02));
      border: 1px solid rgba(255,215,0,.28);
      border-radius: var(--radius);
      padding:22px;
      box-shadow: var(--shadow);
      position: relative;
      overflow:hidden;
    }
    .heroCard:before{
      content:"";
      position:absolute;
      inset:-2px;
      background:
        radial-gradient(500px 220px at 0% 0%, rgba(255,215,0,.18), transparent 60%),
        radial-gradient(420px 220px at 100% 20%, rgba(255,215,0,.12), transparent 60%);
      pointer-events:none;
      opacity:.9;
    }
    .heroInner{ position: relative; z-index:1; }

    .kicker{
      font-family: Orbitron, sans-serif;
      color: rgba(255,215,0,.90);
      letter-spacing: 1.2px;
      font-size: 12px;
      text-transform: uppercase;
      display:flex;
      align-items:center;
      gap:10px;
      flex-wrap:wrap;
    }
    /* Logo mini no Hero */
    .miniLogo{
      width:26px; height:26px;
      border-radius: 9px;
      border:1px solid rgba(255,215,0,.25);
      overflow:hidden;
      display:inline-block;
    }
    .miniLogo img{ width:100%; height:100%; object-fit:cover; display:block; }

    .headline{
      margin: 10px 0 10px;
      font-size: clamp(26px, 3.6vw, 44px);
      line-height:1.05;
      font-weight: 800;
    }
    .tagline{
      margin: 0 0 18px;
      color: var(--muted);
      max-width: 64ch;
      font-size: 14px;
      line-height: 1.55;
    }

    .ctaRow{
      display:flex;
      gap:10px;
      flex-wrap:wrap;
      margin-top: 12px;
    }

    .btn{
      display:inline-flex;
      align-items:center;
      justify-content:center;
      gap:10px;
      padding: 12px 14px;
      border-radius: 12px;
      border: 1px solid rgba(255,255,255,.08);
      background: rgba(0,0,0,.45);
      color: var(--text);
      text-decoration:none;
      font-weight: 700;
      transition: .22s ease;
      font-size: 13px;
    }
    .btn:hover{
      transform: translateY(-2px);
      border-color: rgba(255,215,0,.35);
      box-shadow: 0 18px 60px rgba(0,0,0,.65);
    }
    .btn.primary{
      background: var(--gold);
      color: #000;
      border-color: rgba(255,215,0,.9);
    }

    .sideCard{
      background: linear-gradient(180deg, rgba(255,255,255,.03), rgba(255,255,255,.015));
      border: 1px solid rgba(255,255,255,.08);
      border-radius: var(--radius);
      padding: 18px;
      box-shadow: var(--shadow);
    }
    .sideTitle{
      font-family: Orbitron, sans-serif;
      color: var(--gold);
      margin:0 0 10px;
      font-size: 14px;
      letter-spacing: .8px;
    }
    .sideText{
      margin:0 0 14px;
      color: var(--muted);
      font-size: 13px;
      line-height: 1.55;
    }
    .pill{
      display:inline-flex;
      align-items:center;
      gap:8px;
      padding: 9px 12px;
      border-radius: 999px;
      border: 1px solid rgba(255,215,0,.25);
      background: rgba(255,215,0,.06);
      color: rgba(255,215,0,.95);
      font-size: 12px;
      font-family: Orbitron, sans-serif;
      letter-spacing: .6px;
    }

    section{ margin-top: 18px; padding-top: 10px; }
    .sectionTitle{
      display:flex;
      align-items:end;
      justify-content:space-between;
      gap:14px;
      margin: 18px 2px 10px;
    }
    .sectionTitle h2{
      margin:0;
      font-family: Orbitron, sans-serif;
      color: var(--gold);
      font-size: 16px;
      letter-spacing: .8px;
    }
    .sectionTitle span{ color: var(--muted); font-size: 12px; }

    .grid{
      display:grid;
      grid-template-columns: repeat(3, 1fr);
      gap:12px;
    }
    @media (max-width: 920px){ .grid{ grid-template-columns: 1fr; } }

    .card{
      background: linear-gradient(180deg, rgba(255,255,255,.025), rgba(255,255,255,.01));
      border:1px solid rgba(255,255,255,.08);
      border-radius: var(--radius);
      padding: 14px;
      box-shadow: var(--shadow);
    }
    .card h3{ margin:0 0 6px; font-size: 13px; color: #fff; }
    .card p{ margin:0 0 12px; color: var(--muted); font-size: 12.5px; line-height: 1.55; }
    .card a{
      display:block;
      text-decoration:none;
      text-align:center;
      padding: 12px 12px;
      border-radius: 12px;
      border: 1px solid rgba(255,215,0,.35);
      color: var(--gold);
      background: rgba(0,0,0,.35);
      font-weight: 800;
      transition: .2s ease;
    }
    .card a:hover{
      background: var(--gold);
      color: #000;
      transform: translateY(-2px);
    }

    .divider{
      height:1px;
      background: linear-gradient(90deg, transparent, rgba(255,215,0,.32), transparent);
      margin: 18px 0 6px;
    }

    footer{
      margin-top: 26px;
      padding: 20px 6px 14px;
      color: #8a8a8a;
      font-size: 12px;
      text-align:center;
    }
    footer .gold{ color: var(--gold); font-family: Orbitron, sans-serif; }
    .small{ opacity:.9; margin-top: 6px; line-height: 1.5; }
  </style>
</head>

<body>
  <div class="container">

    <!-- Topbar -->
    <div class="topbar">
      <div class="brand">
        <div class="logoImgWrap">
          <img class="logoImg" src="logo-gold.png" alt="Logo GOLD Produção" />
        </div>
        <div>
          <h1>GOLD Produção</h1>
          <p>“Onde a mente cria, o código executa.”</p>
        </div>
      </div>

      <nav class="nav" aria-label="Navegação">
        <a href="#links">Links</a>
        <a href="#musica">Música</a>
        <a href="#conteudos">Conteúdos</a>
        <a href="#comunidade">Comunidade</a>
      </nav>
    </div>

    <!-- Hero -->
    <div class="hero">
      <div class="heroCard">
        <div class="heroInner">
          <div class="kicker">
            <span class="miniLogo"><img src="logo-gold.png" alt="" /></span>
            <span>CÓDIGO & SANGUE • OFICIAL</span>
          </div>

          <div class="headline">GOLD Produção<br/>no comando da quebrada digital.</div>

          <p class="tagline">
            Música, audiovisual e estratégia. Aqui você encontra os links oficiais do projeto, o álbum
            <b>“Código Vivo”</b>, e os materiais de criação pra evoluir sua produção com IA.
          </p>

          <div class="ctaRow">
            <a class="btn primary" href="https://kntn.ly/64da9e63" target="_blank" rel="noopener">🎥 Abrir YouTube</a>
            <a class="btn" href="https://open.spotify.com/artist/5RQkqgF7p05Qkjg7FlhptB?si=dVv-ATjVT6eUZkrvCSAsCA" target="_blank" rel="noopener">🎧 Ouvir no Spotify</a>
            <a class="btn" href="https://whatsapp.com/channel/0029VbBWitXF1YlM5T5Uno2R" target="_blank" rel="noopener">💬 Entrar no Canal WhatsApp</a>
          </div>
        </div>
      </div>

      <aside class="sideCard">
        <div class="sideTitle">🔥 Destaque</div>
        <p class="sideText">
          Quer aprender a criar com qualidade e consistência? Começa pelo PDF gratuito e depois sobe pro e-book premium.
        </p>
        <div class="divider"></div>
        <p style="margin: 12px 0 10px;">
          <span class="pill">ARIS • Inteligência Estratégica GOLD</span>
        </p>
        <a class="btn" style="width:100%;" href="https://drive.google.com/file/d/1uZGGcRxJ3zTKooW3lbgEApiKfvWgLRRi/view?usp=drivesdk" target="_blank" rel="noopener">📗 Baixar PDF Gratuito</a>
        <a class="btn primary" style="width:100%; margin-top:10px;" href="https://pay.hotmart.com/Y99184081N" target="_blank" rel="noopener">📘 Comprar E-book Premium</a>
      </aside>
    </div>

    <!-- Links -->
    <section id="links">
      <div class="sectionTitle">
        <h2>Links Principais</h2>
        <span>atalhos oficiais do projeto</span>
      </div>

      <div class="grid">
        <div class="card">
          <h3>🎥 YouTube GOLD YT</h3>
          <p>Clipes, shorts, lives e evolução do projeto.</p>
          <a href="https://kntn.ly/64da9e63" target="_blank" rel="noopener">Abrir</a>
        </div>

        <div class="card">
          <h3>🎬 TikTok GOLD Produção</h3>
          <p>Conteúdo curto, impacto visual e trends.</p>
          <a href="https://kntn.ly/14dbcc06" target="_blank" rel="noopener">Abrir</a>
        </div>

        <div class="card">
          <h3>💬 Canal WhatsApp GOLD</h3>
          <p>Comunicados, lançamentos e bastidores.</p>
          <a href="https://whatsapp.com/channel/0029VbBWitXF1YlM5T5Uno2R" target="_blank" rel="noopener">Entrar</a>
        </div>

        <div class="card">
          <h3>🎧 Spotify — Código & Sangue</h3>
          <p>Perfil do artista e catálogo oficial.</p>
          <a href="https://open.spotify.com/artist/5RQkqgF7p05QkjgF7p05Qkjg7FlhptB?si=dVv-ATjVT6eUZkrvCSAsCA" target="_blank" rel="noopener">Ouvir</a>
        </div>

        <div class="card">
          <h3>🎵 YouTube Music — Código & Sangue</h3>
          <p>Playlist oficial no YouTube Music.</p>
          <a href="https://music.youtube.com/playlist?list=OLAK5uy_n5LiR16gW7F-VMOOKLZmFrr5rkWPIoLZQ&si=JlN5H3IWpfYV7YKJ" target="_blank" rel="noopener">Ouvir</a>
        </div>

        <div class="card">
          <h3>🍎 Apple Music — Código Vivo</h3>
          <p>Álbum disponível na Apple Music Brasil.</p>
          <a href="https://music.apple.com/br/album/c%C3%B3digo-vivo/1862655463" target="_blank" rel="noopener">Ouvir</a>
        </div>

        <div class="card">
          <h3>💿 Álbum “Código Vivo”</h3>
          <p>Central de streaming e compartilhamento.</p>
          <a href="https://distrokid.com/hyperfollow/cdigosangue/cdigo-vivo" target="_blank" rel="noopener">Abrir</a>
        </div>

        <div class="card">
          <h3>📘 E-book Criador Profissional</h3>
          <p>Versão premium: módulos, tarefas e bônus.</p>
          <a href="https://pay.hotmart.com/Y99184081N" target="_blank" rel="noopener">Comprar</a>
        </div>

        <div class="card">
          <h3>📗 PDF Gratuito — Criador Imbatível</h3>
          <p>Manual rápido pra criar vídeos cinematográficos com IA.</p>
          <a href="https://drive.google.com/file/d/1uZGGcRxJ3zTKooW3lbgEApiKfvWgLRRi/view?usp=drivesdk" target="_blank" rel="noopener">Acessar</a>
        </div>

        <div class="card">
          <h3>📸 Instagram GOLD SEO Edition</h3>
          <p>Posts, provas sociais e novidades.</p>
          <a href="https://www.instagram.com/goldseoedition?igsh=enhyZmRoMGRsZGJ1" target="_blank" rel="noopener">Abrir</a>
        </div>

        <div class="card">
          <h3>📘 Facebook GOLD</h3>
          <p>Comunidade e publicações extras.</p>
          <a href="https://www.facebook.com/profile.php?id=61582781752953" target="_blank" rel="noopener">Abrir</a>
        </div>

        <div class="card">
          <h3>🚀 Comunidade & Avisos</h3>
          <p>Pra receber drops e novidades do universo GOLD.</p>
          <a href="https://whatsapp.com/channel/0029VbBWitXF1YlM5T5Uno2R" target="_blank" rel="noopener">Receber avisos</a>
        </div>
      </div>
    </section>

    <!-- Música -->
    <section id="musica">
      <div class="sectionTitle">
        <h2>Música</h2>
        <span>streaming oficial</span>
      </div>

      <div class="grid">
        <div class="card">
          <h3>🎧 Spotify — Código & Sangue</h3>
          <p>Perfil do artista e catálogo oficial.</p>
          <a href="https://open.spotify.com/artist/5RQkqgF7p05Qkjg7FlhptB?si=dVv-ATjVT6eUZkrvCSAsCA" target="_blank" rel="noopener">Ouvir</a>
        </div>

        <div class="card">
          <h3>🎵 YouTube Music — Código & Sangue</h3>
          <p>Playlist oficial no YouTube Music.</p>
          <a href="https://music.youtube.com/playlist?list=OLAK5uy_n5LiR16gW7F-VMOOKLZmFrr5rkWPIoLZQ&si=JlN5H3IWpfYV7YKJ" target="_blank" rel="noopener">Ouvir</a>
        </div>

        <div class="card">
          <h3>🍎 Apple Music — Código Vivo</h3>
          <p>Álbum disponível na Apple Music Brasil.</p>
          <a href="https://music.apple.com/br/album/c%C3%B3digo-vivo/1862655463" target="_blank" rel="noopener">Ouvir</a>
        </div>
      </div>
    </section>

    <!-- Conteúdos -->
    <section id="conteudos">
      <div class="sectionTitle">
        <h2>Conteúdos & Materiais</h2>
        <span>aprendizado e evolução</span>
      </div>

      <div class="grid">
        <div class="card">
          <h3>📗 PDF Gratuito — Criador Imbatível</h3>
          <p>Manual rápido pra criar vídeos cinematográficos com IA.</p>
          <a href="https://drive.google.com/file/d/1uZGGcRxJ3zTKooW3lbgEApiKfvWgLRRi/view?usp=drivesdk" target="_blank" rel="noopener">Acessar</a>
        </div>

        <div class="card">
          <h3>📘 E-book — Criador Profissional</h3>
          <p>Versão premium: módulos, tarefas e bônus.</p>
          <a href="https://pay.hotmart.com/Y99184081N" target="_blank" rel="noopener">Comprar</a>
        </div>

        <div class="card">
          <h3>💬 Canal WhatsApp</h3>
          <p>Atualizações, lançamentos e bastidores.</p>
          <a href="https://whatsapp.com/channel/0029VbBWitXF1YlM5T5Uno2R" target="_blank" rel="noopener">Entrar</a>
        </div>
      </div>
    </section>

    <!-- Comunidade -->
    <section id="comunidade">
      <div class="sectionTitle">
        <h2>Comunidade</h2>
        <span>chega junto</span>
      </div>

      <div class="heroCard" style="padding:18px;">
        <div class="heroInner">
          <div class="kicker">FÃS • APOIADORES • PARCERIAS</div>
          <div style="display:flex; flex-wrap:wrap; gap:10px; margin-top:10px;">
            <a class="btn primary" href="https://kntn.ly/64da9e63" target="_blank" rel="noopener">✅ Inscrever no YouTube</a>
            <a class="btn" href="https://kntn.ly/14dbcc06" target="_blank" rel="noopener">🔥 Seguir no TikTok</a>
            <a class="btn" href="https://www.instagram.com/goldseoedition?igsh=enhyZmRoMGRsZGJ1" target="_blank" rel="noopener">📸 Seguir no Instagram</a>
            <a class="btn" href="https://www.facebook.com/profile.php?id=61582781752953" target="_blank" rel="noopener">📘 Seguir no Facebook</a>
          </div>
        </div>
      </div>
    </section>

    <footer>
      <div>GOLD Produção © 2026 — <span class="gold">CÓDIGO & SANGUE</span></div>
      <div class="small">Desenvolvido por <span class="gold">ARIS</span> — Inteligência Estratégica GOLD</div>
    </footer>

  </div>
</body>
</html>
