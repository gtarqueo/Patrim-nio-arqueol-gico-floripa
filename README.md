# Patrim-nio-arqueol-gico-floripa
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ecos de Meiembipe | Patrimônio Arqueológico de Florianópolis</title>
  <meta name="description" content="Guia arqueológico interativo dos sítios rupestres, oficinas líticas e patrimônio milenar da Ilha de Santa Catarina.">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@600;700;900&family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
  
  <style>
    :root {
      --bg-dark: #0b0f12;
      --bg-card: rgba(18, 25, 31, 0.75);
      --accent-gold: #e5b358;
      --accent-cyan: #38bdf8;
      --text-main: #f1f5f9;
      --text-muted: #94a3b8;
      --border-glass: rgba(255, 255, 255, 0.08);
      --font-display: 'Cinzel', serif;
      --font-sans: 'Inter', sans-serif;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      background-color: var(--bg-dark);
      color: var(--text-main);
      font-family: var(--font-sans);
      line-height: 1.6;
      overflow-x: hidden;
      background-image: 
        radial-gradient(circle at 10% 20%, rgba(56, 189, 248, 0.05) 0%, transparent 40%),
        radial-gradient(circle at 90% 80%, rgba(229, 179, 88, 0.05) 0%, transparent 40%);
    }

    /* Hero Section */
    .hero {
      position: relative;
      min-height: 90vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 3rem 1.5rem;
      background: linear-gradient(180deg, rgba(11, 15, 18, 0.4) 0%, var(--bg-dark) 100%),
                  radial-gradient(circle at center, #1e293b 0%, #0b0f12 100%);
      border-bottom: 1px solid var(--border-glass);
    }

    .badge {
      display: inline-block;
      padding: 0.35rem 1rem;
      background: rgba(229, 179, 88, 0.12);
      border: 1px solid var(--accent-gold);
      color: var(--accent-gold);
      border-radius: 999px;
      font-size: 0.75rem;
      font-weight: 700;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      margin-bottom: 1.5rem;
    }

    .hero h1 {
      font-family: var(--font-display);
      font-size: clamp(2.2rem, 6vw, 4.5rem);
      letter-spacing: 0.05em;
      line-height: 1.1;
      margin-bottom: 1rem;
      background: linear-gradient(135deg, #ffffff 40%, var(--accent-gold) 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .hero p {
      max-width: 680px;
      color: var(--text-muted);
      font-size: 1.1rem;
      font-weight: 300;
      margin-bottom: 2rem;
    }

    .cta-btn {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      background: linear-gradient(135deg, var(--accent-gold), #c99333);
      color: #0b0f12;
      font-weight: 700;
      padding: 0.9rem 2rem;
      border-radius: 8px;
      text-decoration: none;
      transition: transform 0.2s, box-shadow 0.2s;
    }

    .cta-btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 25px rgba(229, 179, 88, 0.3);
    }

    /* Container */
    .container {
      max-width: 1100px;
      margin: 0 auto;
      padding: 4rem 1.5rem;
    }

    .section-title {
      font-family: var(--font-display);
      font-size: clamp(1.8rem, 4vw, 2.5rem);
      color: var(--text-main);
      margin-bottom: 0.5rem;
      text-align: center;
    }

    .section-subtitle {
      text-align: center;
      color: var(--accent-gold);
      font-size: 0.9rem;
      text-transform: uppercase;
      letter-spacing: 0.1em;
      margin-bottom: 3rem;
    }

    /* Destaque Ilha do Campeche */
    .campeche-spotlight {
      background: var(--bg-card);
      border: 1px solid var(--accent-gold);
      border-radius: 16px;
      padding: 2.5rem;
      backdrop-filter: blur(12px);
      margin-bottom: 4rem;
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
      position: relative;
      overflow: hidden;
    }

    .campeche-spotlight::before {
      content: "TOMBO IPHAN 2000";
      position: absolute;
      top: 15px;
      right: -30px;
      background: var(--accent-gold);
      color: #0b0f12;
      font-size: 0.65rem;
      font-weight: 900;
      padding: 4px 35px;
      transform: rotate(45deg);
      letter-spacing: 0.1em;
    }

    .campeche-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 2rem;
    }

    @media (min-width: 768px) {
      .campeche-grid {
        grid-template-columns: 1.2fr 0.8fr;
      }
    }

    .campeche-text h3 {
      font-family: var(--font-display);
      font-size: 1.8rem;
      color: var(--accent-gold);
      margin-bottom: 1rem;
    }

    .campeche-text p {
      margin-bottom: 1rem;
      color: var(--text-muted);
    }

    .stats-box {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 1rem;
      background: rgba(0, 0, 0, 0.25);
      border-radius: 12px;
      padding: 1.2rem;
      border: 1px solid var(--border-glass);
    }

    .stat-number {
      font-size: 1.6rem;
      font-weight: 700;
      color: var(--accent-gold);
      font-family: var(--font-display);
    }

    .stat-label {
      font-size: 0.75rem;
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 0.05em;
    }

    /* Cards Grid */
    .sites-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 1.8rem;
      margin-bottom: 4rem;
    }

    .card {
      background: var(--bg-card);
      border: 1px solid var(--border-glass);
      border-radius: 14px;
      padding: 1.8rem;
      transition: transform 0.2s, border-color 0.2s;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    .card:hover {
      transform: translateY(-5px);
      border-color: rgba(229, 179, 88, 0.4);
    }

    .card-tag {
      font-size: 0.7rem;
      font-weight: 700;
      color: var(--accent-cyan);
      text-transform: uppercase;
      letter-spacing: 0.1em;
      margin-bottom: 0.8rem;
    }

    .card h4 {
      font-family: var(--font-display);
      font-size: 1.3rem;
      color: #fff;
      margin-bottom: 0.8rem;
    }

    .card p {
      font-size: 0.95rem;
      color: var(--text-muted);
      margin-bottom: 1.2rem;
    }

    /* Preservação / Manifesto */
    .preservation-banner {
      background: linear-gradient(135deg, rgba(229, 179, 88, 0.1), rgba(56, 189, 248, 0.05));
      border: 1px solid rgba(229, 179, 88, 0.3);
      border-radius: 16px;
      padding: 2.5rem;
      text-align: center;
      margin-bottom: 4rem;
    }

    .preservation-banner h3 {
      font-family: var(--font-display);
      font-size: 1.6rem;
      color: var(--accent-gold);
      margin-bottom: 1rem;
    }

    .rules-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 1.2rem;
      margin-top: 1.8rem;
      text-align: left;
    }

    .rule-item {
      background: rgba(0, 0, 0, 0.2);
      padding: 1rem;
      border-radius: 8px;
      font-size: 0.9rem;
      color: var(--text-muted);
      border-left: 3px solid var(--accent-gold);
    }

    /* Footer */
    footer {
      border-top: 1px solid var(--border-glass);
      padding: 2.5rem 1.5rem;
      text-align: center;
      font-size: 0.85rem;
      color: var(--text-muted);
    }
  </style>
</head>
<body>

  <!-- Hero Cinematográfico -->
  <header class="hero">
    <div class="badge">Patrimônio Arqueológico de Florianópolis</div>
    <h1>Ecos de Meiembipe</h1>
    <p>
      Antes do asfalto e das vilas coloniais, este litoral falava pela pedra. 
      Descubra as inscrições rupestres, oficinas líticas e monumentos ancestrais 
      esculpidos há mais de cinco mil anos na Ilha de Santa Catarina.
    </p>
    <a href="#campeche" class="cta-btn">Explorar Sítios Sagrados ↓</a>
  </header>

  <main class="container">
    
    <!-- Destaque Especial: Ilha do Campeche -->
    <section id="campeche" class="campeche-spotlight">
      <div class="campeche-grid">
        <div class="campeche-text">
          <h3>Ilha do Campeche: O Santuário do Atlântico</h3>
          <p>
            Localizada a 1,5 km da Praia do Campeche, esta ilha guarda a maior densidade de sítios de arte rupestre do litoral sul do Brasil. Tombada pelo IPHAN no ano 2000, suas escarpas de granito e diques de diabásio reúnem inscrições antropomorfas, máscaras estilizadas, setas e formas geométricas indecifráveis gravadas com percursores de quartzo há milênios.
          </p>
          <p>
            Além das inscrições, seus costões exibem oficinas líticas intactas, onde antigos navegadores e caçadores afiavam suas lâminas de machado diretamente na rocha banhada pelas marés.
          </p>
        </div>
        <div class="stats-box">
          <div>
            <div class="stat-number">> 10</div>
            <div class="stat-label">Sítios Arqueológicos</div>
          </div>
          <div>
            <div class="stat-number">> 100</div>
            <div class="stat-label">Petróglifos Catalogados</div>
          </div>
          <div>
            <div class="stat-number">5.000+</div>
            <div class="stat-label">Anos de Memória</div>
          </div>
          <div>
            <div class="stat-number">100%</div>
            <div class="stat-label">Monitoramento Guiado</div>
          </div>
        </div>
      </div>
    </section>

    <!-- Outros Sítios da Ilha de Santa Catarina -->
    <h2 class="section-title">O Território das Pedras</h2>
    <p class="section-subtitle">Mapeamento dos principais sítios do município</p>

    <div class="sites-grid">
      <!-- Santinho -->
      <article class="card">
        <div>
          <span class="card-tag">Extremo Norte</span>
          <h4>Costão do Santinho</h4>
          <p>
            Um dos painéis rupestres mais emblemáticos do Brasil. Sobre o granito voltado para o mar revolto, figuras pontilhadas e máscaras rituais marcam prováveis alinhamentos com o solstício e pontos de orientação astronômica.
          </p>
        </div>
        <div class="badge" style="margin: 0; align-self: flex-start;">Inscrição Rupestre</div>
      </article>

      <!-- Armação e Pântano do Sul -->
      <article class="card">
        <div>
          <span class="card-tag">Sul da Ilha</span>
          <h4>Oficinas da Armação & Pântano</h4>
          <p>
            Bacias polidoras e sulcos perfeitamente côncavos esculpidos no granito litorâneo. Os artesãos pré-coloniais utilizavam a areia da praia e a água do mar como pasta abrasiva para brunir e afiar machados de pedra.
          </p>
        </div>
        <div class="badge" style="margin: 0; align-self: flex-start;">Oficina Lítica</div>
      </article>

      <!-- Galheta e Barra da Lagoa -->
      <article class="card">
        <div>
          <span class="card-tag">Leste da Ilha</span>
          <h4>Galheta & Ponta do Gravatá</h4>
          <p>
            Trilhas escarpadas que conectam abrigos sob rocha com amoladores lineares. Testemunhos do deslocamento e acampamento de grupos pré-coloniais durante as estações de pesca da tainha.
          </p>
        </div>
        <div class="badge" style="margin: 0; align-self: flex-start;">Oficina & Abrigo</div>
      </article>

      <!-- Sambaquis -->
      <article class="card">
        <div>
          <span class="card-tag">Baías Norte & Sul</span>
          <h4>Sambaquis de Meiembipe</h4>
          <p>
            Montanhas artificiais de conchas erguidas por sociedades sambaquieiras ao longo de gerações. Serviam como locais de moradia, atalaia e sepultamentos cerimoniais repletos de oferendas de zoólitos esculpidos.
          </p>
        </div>
        <div class="badge" style="margin: 0; align-self: flex-start;">Sítio Funerário</div>
      </article>
    </div>

    <!-- Guia de Preservação e Ética -->
    <section class="preservation-banner">
      <h3>Preservação: O Compromisso com a Memória</h3>
      <p style="color: var(--text-muted); max-width: 720px; margin: 0 auto;">
        As rochas resistiram a milênios de ondas e tempestades, mas não resistem ao vandalismo moderno. Conforme a Lei Federal nº 3.924/1961, os sítios arqueológicos são patrimônio da União e sua destruição é crime inafiançável.
      </p>

      <div class="rules-grid">
        <div class="rule-item">
          <strong>Não toque nas gravuras:</strong> A oleosidade e o suor da pele alimentam fungos e aceleram a esfoliação da rocha.
        </div>
        <div class="rule-item">
          <strong>Jamais repinte ou contorne:</strong> Passar giz, carvão ou tinta destrói os pigmentos e microvestígios originais.
        </div>
        <div class="rule-item">
          <strong>Respeite as cordas de contenção:</strong> O pisoteio descalça a base das rochas e causa erosão irreversível.
        </div>
        <div class="rule-item">
          <strong>Traga de volta seu lixo:</strong> Fogueiras e detritos alteram a composição mineral do solo arqueológico.
        </div>
      </div>
    </section>

  </main>

  <footer>
    <p>Projeto de Valorização Arqueológica de Florianópolis | Desenvolvido para consulta via QR Code em campo.</p>
    <p style="margin-top: 0.5rem; opacity: 0.6;">Acesse com respeito. A terra que você pisa é sagrada e milenar.</p>
  </footer>

</body>
</html>
