<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dashboard PRAD | UFV Rio do Peixe I e II — Julho/2026</title>
<script src="https://cdn.jsdelivr.net/npm/chart.js@4.5.1"></script>
<style>
:root{
  --bg:#0d1117; --card:#161b22; --card2:#1d2633;
  --blue1:#0b3d91; --blue2:#1565C0; --blue3:#2196F3; --cyan:#00BCD4;
  --gray1:#8b949e; --gray2:#c9d1d9; --white:#ffffff;
  --success:#00C853; --warning:#FFC107; --danger:#FF5252;
  /* legacy tokens remapped to tech palette (kept for structural compatibility) */
  --green-900:var(--blue1); --green-800:#0e4aa8; --green-700:var(--blue2); --green-600:var(--blue3);
  --green-500:var(--cyan); --green-100:#132030; --amber:var(--warning); --red:var(--danger); --blue:var(--blue3);
  --text:var(--gray2); --text-sec:var(--gray1); --radius:12px;
  --gap:18px; --shadow:0 4px 18px rgba(0,0,0,.45);
}
*{box-sizing:border-box;}
body{margin:0;font-family:'Segoe UI',system-ui,Arial,sans-serif;background:
  radial-gradient(circle at 15% 0%, #101c30 0%, var(--bg) 45%),var(--bg);color:var(--text);}
.container{max-width:1500px;margin:0 auto;padding:20px;}

/* ===== HEADER ===== */
.header{
  background:linear-gradient(120deg,var(--blue1),var(--blue2) 55%,var(--cyan));
  color:#fff;border-radius:var(--radius);padding:22px 28px;margin-bottom:14px;
  display:flex;justify-content:space-between;align-items:flex-start;flex-wrap:wrap;gap:14px;
  box-shadow:var(--shadow);position:relative;overflow:hidden;border:1px solid #2b3f5c;
}
.header::after{content:'';position:absolute;inset:0;background:repeating-linear-gradient(115deg,rgba(255,255,255,.035) 0 2px,transparent 2px 26px);pointer-events:none;}
.header h1{margin:0;font-size:21px;font-weight:700;letter-spacing:.2px;}
.header p{margin:4px 0 0;font-size:12.5px;color:#cfe1ff;}
.header .badge{background:rgba(255,255,255,.14);backdrop-filter:blur(4px);padding:6px 14px;border-radius:20px;font-size:11.5px;font-weight:600;border:1px solid rgba(255,255,255,.18);}
.tag-row{display:flex;gap:8px;flex-wrap:wrap;}
.header-status{display:flex;flex-direction:column;gap:8px;align-items:flex-end;font-size:12px;min-width:230px;position:relative;z-index:1;}
.hs-row{display:flex;align-items:center;gap:8px;justify-content:flex-end;flex-wrap:wrap;}
.hs-clock{font-size:22px;font-weight:800;font-variant-numeric:tabular-nums;letter-spacing:.5px;}
.hs-date{font-size:11.5px;color:#cfe1ff;}
.dot{width:8px;height:8px;border-radius:50%;display:inline-block;box-shadow:0 0 8px currentColor;}
.dot.online{background:var(--success);color:var(--success);animation:pulse 1.6s infinite;}
.dot.sync{background:var(--cyan);color:var(--cyan);animation:pulse 1.2s infinite;}
@keyframes pulse{0%,100%{opacity:1;transform:scale(1);}50%{opacity:.45;transform:scale(1.3);}}
.hs-pill{background:rgba(255,255,255,.14);border:1px solid rgba(255,255,255,.2);padding:3px 10px;border-radius:20px;font-weight:700;font-size:11px;}
.hs-bar-wrap{width:230px;}
.hs-bar-label{display:flex;justify-content:space-between;font-size:10.5px;color:#cfe1ff;margin-bottom:3px;}
.hs-bar{height:7px;border-radius:6px;background:rgba(255,255,255,.18);overflow:hidden;}
.hs-bar-fill{height:100%;border-radius:6px;background:linear-gradient(90deg,var(--cyan),var(--success));animation:growBar 1.4s ease;}
@keyframes growBar{from{width:0;}}

/* ===== DYNAMIC STATUS BAR ===== */
.dynbar{display:flex;align-items:center;gap:18px;background:var(--card);border:1px solid #232c3d;border-radius:var(--radius);
  padding:12px 22px;margin-bottom:var(--gap);box-shadow:var(--shadow);flex-wrap:wrap;}
.dynbar .db-item{display:flex;align-items:center;gap:8px;font-size:12.5px;color:var(--gray1);}
.dynbar .db-item b{color:var(--white);font-size:13px;}
.dynbar .db-sep{width:1px;height:20px;background:#2a3550;}
.db-progress{flex:1;min-width:160px;display:flex;align-items:center;gap:10px;}
.db-progress .track{flex:1;height:9px;border-radius:6px;background:#0f1622;overflow:hidden;border:1px solid #232c3d;}
.db-progress .fill{height:100%;border-radius:6px;background:linear-gradient(90deg,var(--blue3),var(--success));animation:growBar 1.6s ease;}
.status-chip{padding:4px 12px;border-radius:20px;font-size:11.5px;font-weight:800;letter-spacing:.4px;}
.status-chip.ok{background:rgba(0,200,83,.15);color:var(--success);border:1px solid rgba(0,200,83,.4);}

/* ===== TABS ===== */
.tabs{display:flex;gap:8px;margin-bottom:var(--gap);flex-wrap:wrap;}
.tab-btn{background:var(--card);border:1px solid #232c3d;color:var(--text-sec);padding:9px 16px;border-radius:8px;font-size:13px;font-weight:600;cursor:pointer;transition:.18s;}
.tab-btn.active{background:linear-gradient(120deg,var(--blue2),var(--blue3));color:#fff;border-color:var(--blue3);box-shadow:0 0 14px rgba(33,150,243,.4);}
.tab-btn:hover{border-color:var(--blue3);color:#fff;transform:translateY(-1px);}
.tab-content{display:none;}
.tab-content.active{display:block;animation:fade .3s ease;}
@keyframes fade{from{opacity:0;transform:translateY(4px);}to{opacity:1;transform:translateY(0);}}

.kpi-row{display:grid;grid-template-columns:repeat(auto-fit,minmax(190px,1fr));gap:var(--gap);margin-bottom:var(--gap);}
.kpi-card{background:var(--card);border-radius:var(--radius);padding:18px 20px;box-shadow:var(--shadow);border-left:4px solid var(--blue3);border-top:1px solid #232c3d;border-right:1px solid #232c3d;border-bottom:1px solid #232c3d;transition:.2s;}
.kpi-card:hover{transform:translateY(-3px);box-shadow:0 8px 24px rgba(33,150,243,.18);border-left-color:var(--cyan);}
.kpi-card.amber{border-left-color:var(--warning);}
.kpi-card.red{border-left-color:var(--danger);}
.kpi-card.blue{border-left-color:var(--blue3);}
.kpi-card.cyan{border-left-color:var(--cyan);}
.kpi-label{font-size:11px;color:var(--text-sec);text-transform:uppercase;letter-spacing:.6px;margin-bottom:6px;font-weight:700;}
.kpi-value{font-size:25px;font-weight:800;color:var(--white);margin-bottom:4px;font-variant-numeric:tabular-nums;}
.kpi-sub{font-size:11.5px;color:var(--text-sec);}
.trend{font-size:12px;font-weight:700;}
.trend.up{color:var(--success);} .trend.flat{color:var(--text-sec);} .trend.down{color:var(--danger);}
.grid-2{display:grid;grid-template-columns:1.3fr 1fr;gap:var(--gap);margin-bottom:var(--gap);}
.grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:var(--gap);margin-bottom:var(--gap);}
.grid-6{display:grid;grid-template-columns:repeat(6,1fr);gap:14px;margin-bottom:var(--gap);}
@media(max-width:1100px){.grid-6{grid-template-columns:repeat(3,1fr);}}
@media(max-width:900px){.grid-2,.grid-3{grid-template-columns:1fr;}}
@media(max-width:560px){.grid-6{grid-template-columns:repeat(2,1fr);}.header{flex-direction:column;}.header-status{align-items:flex-start;}}
@media(min-width:2200px){.container{max-width:1900px;}body{font-size:17px;}}

.card{background:var(--card);border-radius:var(--radius);padding:20px 22px;box-shadow:var(--shadow);border:1px solid #232c3d;transition:.2s;}
.card:hover{border-color:#334a6d;}
.card h3{margin:0 0 4px;font-size:14px;font-weight:700;color:var(--white);}
.card .subtitle{font-size:11.5px;color:var(--text-sec);margin-bottom:14px;}
canvas{max-height:300px;}
table{width:100%;border-collapse:collapse;font-size:12.5px;}
thead th{text-align:left;padding:9px 10px;background:#101a2c;color:var(--cyan);font-weight:700;font-size:11px;text-transform:uppercase;letter-spacing:.4px;}
tbody td{padding:8px 10px;border-bottom:1px solid #1d2633;color:var(--gray2);}
tbody tr{transition:.15s;}
tbody tr:hover{background:#101a2c;}
.pill{padding:3px 10px;border-radius:20px;font-size:11px;font-weight:700;display:inline-block;}
.pill.green{background:rgba(0,200,83,.14);color:var(--success);border:1px solid rgba(0,200,83,.35);}
.pill.amber{background:rgba(255,193,7,.14);color:var(--warning);border:1px solid rgba(255,193,7,.35);}
.pill.red{background:rgba(255,82,82,.14);color:var(--danger);border:1px solid rgba(255,82,82,.35);}
.pill.blue{background:rgba(33,150,243,.14);color:var(--blue3);border:1px solid rgba(33,150,243,.35);}
.arrow{font-weight:800;}
.footer{text-align:center;font-size:11.5px;color:var(--text-sec);padding:20px 0;}
.note{background:rgba(255,193,7,.08);border-left:4px solid var(--warning);padding:12px 16px;border-radius:8px;font-size:12.5px;color:#e8d590;margin-bottom:var(--gap);}
.legend-swatch{display:inline-block;width:10px;height:10px;border-radius:2px;margin-right:6px;}
.two-col-list{display:grid;grid-template-columns:1fr 1fr;gap:8px 20px;font-size:12.5px;list-style:none;padding:0;color:var(--gray2);}
.two-col-list li{margin-bottom:4px;}
.section-title{font-size:15px;font-weight:800;color:var(--white);margin:4px 0 12px;padding-bottom:8px;border-bottom:2px solid #232c3d;display:flex;align-items:center;gap:8px;}
.section-title::before{content:'';width:4px;height:16px;background:linear-gradient(180deg,var(--cyan),var(--blue3));border-radius:2px;}

/* ===== EXEC CARDS ===== */
.exec-card{background:linear-gradient(160deg,var(--card),var(--card2));border-radius:var(--radius);padding:16px;text-align:center;border:1px solid #232c3d;box-shadow:var(--shadow);transition:.2s;position:relative;overflow:hidden;}
.exec-card:hover{transform:translateY(-4px) scale(1.02);border-color:var(--cyan);}
.exec-card .ring{width:74px;height:74px;margin:0 auto 8px;position:relative;}
.exec-card .ring svg{transform:rotate(-90deg);}
.exec-card .ring-bg{fill:none;stroke:#20293a;stroke-width:8;}
.exec-card .ring-fg{fill:none;stroke-width:8;stroke-linecap:round;transition:stroke-dashoffset 1.4s cubic-bezier(.4,0,.2,1);}
.exec-card .ring-val{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;font-size:15px;font-weight:800;color:#fff;}
.exec-card .ring-label{font-size:11.5px;color:var(--text-sec);font-weight:700;text-transform:uppercase;letter-spacing:.4px;}

/* ===== GAUGE ===== */
.gauge-wrap{display:flex;flex-direction:column;align-items:center;justify-content:center;}
.gauge-val{font-size:30px;font-weight:800;color:#fff;margin-top:-46px;}
.gauge-label{font-size:12px;color:var(--text-sec);font-weight:700;margin-top:2px;text-transform:uppercase;letter-spacing:.5px;}

/* ===== ALERTA FITOSSANITARIO ===== */
.fito-row{display:flex;justify-content:space-between;gap:8px;flex-wrap:wrap;}
.fito-item{flex:1;min-width:80px;text-align:center;background:#101a2c;border-radius:10px;padding:12px 6px;border:1px solid #232c3d;transition:.2s;}
.fito-item:hover{transform:translateY(-3px);}
.fito-dot{width:22px;height:22px;border-radius:50%;margin:0 auto 8px;box-shadow:0 0 12px currentColor;}
.fito-month{font-size:11px;color:var(--text-sec);font-weight:700;}

/* ===== SEMAFORO ===== */
.semaforo{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:10px;}
.sem-item{display:flex;align-items:center;gap:8px;background:#101a2c;border:1px solid #232c3d;border-radius:8px;padding:9px 12px;font-size:12.5px;font-weight:600;color:var(--gray2);}
.sem-dot{width:11px;height:11px;border-radius:50%;box-shadow:0 0 8px currentColor;flex-shrink:0;}

/* ===== IA PANEL ===== */
.ia-panel{background:linear-gradient(120deg,#0d1b30,#101a2c);border:1px solid #23405e;border-radius:var(--radius);padding:22px 26px;margin-bottom:var(--gap);box-shadow:0 0 24px rgba(0,188,212,.08);}
.ia-panel h3{color:var(--cyan);display:flex;align-items:center;gap:8px;margin:0 0 14px;font-size:15px;}
.ia-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(230px,1fr));gap:10px;}
.ia-item{display:flex;align-items:center;gap:8px;font-size:13px;color:var(--gray2);background:rgba(0,188,212,.06);border:1px solid rgba(0,188,212,.18);border-radius:8px;padding:10px 12px;}
.ia-item span.check{color:var(--success);font-weight:900;}

/* ===== DEV STAGE ===== */
.dev-stage-track{display:flex;align-items:center;justify-content:space-between;background:#101a2c;border:1px solid #232c3d;border-radius:10px;padding:16px 10px;gap:4px;}
.dev-step{flex:1;text-align:center;position:relative;}
.dev-step .dev-icon{font-size:26px;opacity:.35;filter:grayscale(1);transition:.3s;}
.dev-step.active .dev-icon{opacity:1;filter:none;transform:scale(1.15);text-shadow:0 0 14px var(--cyan);}
.dev-step .dev-name{font-size:10.5px;color:var(--text-sec);margin-top:6px;font-weight:700;text-transform:uppercase;letter-spacing:.3px;}
.dev-step.active .dev-name{color:var(--cyan);}
.dev-step::after{content:'';position:absolute;top:16px;left:50%;width:100%;height:2px;background:#232c3d;z-index:0;}
.dev-step:last-child::after{display:none;}
.dev-step.done::after{background:var(--success);}
.dev-compare{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:16px;}
.dev-col{background:#101a2c;border:1px solid #232c3d;border-radius:10px;padding:12px 14px;}
.dev-col-title{font-size:12.5px;font-weight:800;margin-bottom:4px;}
.dev-col-stage{font-size:15px;font-weight:800;color:#fff;margin-bottom:6px;}
.dev-col-note{font-size:11.5px;color:var(--text-sec);line-height:1.4;}

/* ===== WEATHER ===== */
.weather-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(110px,1fr));gap:10px;}
.weather-loading{grid-column:1/-1;text-align:center;color:var(--text-sec);font-size:12.5px;padding:20px 0;}
.w-item{background:#101a2c;border:1px solid #232c3d;border-radius:10px;padding:12px 10px;text-align:center;}
.w-item .w-val{font-size:19px;font-weight:800;color:#fff;font-variant-numeric:tabular-nums;}
.w-item .w-lbl{font-size:10.5px;color:var(--text-sec);text-transform:uppercase;letter-spacing:.4px;margin-top:2px;}
.w-updated{grid-column:1/-1;text-align:right;font-size:10.5px;color:var(--text-sec);margin-top:4px;}
.weather-links{margin-top:14px;border-top:1px solid #232c3d;padding-top:10px;}
.wl-row{display:flex;gap:8px;flex-wrap:wrap;margin-top:6px;}
.wl-row a{background:rgba(0,188,212,.1);border:1px solid rgba(0,188,212,.3);color:var(--cyan);text-decoration:none;font-size:11px;font-weight:700;padding:5px 11px;border-radius:16px;transition:.2s;}
.wl-row a:hover{background:rgba(0,188,212,.22);}
</style>
</head>
<body>
<div class="container">

  <div class="header">
    <div>
      <h1>🌱 PRAD — UFV Rio do Peixe I e II | Caraúbas-PB</h1>
      <p>Relatório de Monitoramento da Reposição Florestal · Campanha de Referência: <b>Julho/2026</b> · Bragagnoli Ambiental / EKORA Consultoria Ambiental</p>
      <div class="tag-row" style="margin-top:10px">
        <span class="badge">Diretor Técnico: Railson N. de Arruda — CREA-PB 1619008858</span>
        <span class="badge">Área Total: 4,74 ha</span>
      </div>
    </div>
    <div class="header-status">
      <div class="hs-clock" id="liveClock">--:--:--</div>
      <div class="hs-date" id="liveDate">carregando data...</div>
      <div class="hs-row">
        <span class="dot online"></span><span>Online</span>
        <span class="dot sync"></span><span>Sinc. automática 60s</span>
      </div>
      <div class="hs-row">
        <span class="hs-pill">Status: Operacional</span>
        <span class="hs-pill">Estabilidade Ecológica: Alta</span>
      </div>
      <div class="hs-bar-wrap">
        <div class="hs-bar-label"><span>Progresso Geral do PRAD</span><span>92%</span></div>
        <div class="hs-bar"><div class="hs-bar-fill" style="width:92%"></div></div>
      </div>
    </div>
  </div>

  <div class="dynbar">
    <div class="db-item">🌿 <span>PRAD</span></div>
    <div class="db-sep"></div>
    <div class="db-item">Status <b>ESTÁVEL</b></div>
    <div class="db-sep"></div>
    <div class="db-progress">
      <span style="font-size:12px;color:var(--text-sec)">Desempenho consolidado</span>
      <div class="track"><div class="fill" style="width:92%"></div></div>
      <b style="color:#fff">92%</b>
    </div>
    <div class="db-sep"></div>
    <span class="status-chip ok">● REPLANTIO NÃO RECOMENDADO NESTA FASE</span>
  </div>

  <div class="tabs">
    <button class="tab-btn active" onclick="showTab('overview')">📊 Visão Geral</button>
    <button class="tab-btn" onclick="showTab('species')">🌳 Espécies & Sobrevivência</button>
    <button class="tab-btn" onclick="showTab('factors')">⚠️ Fatores Supervenientes</button>
    <button class="tab-btn" onclick="showTab('manejo')">🔧 Manejo & Ações</button>
    <button class="tab-btn" onclick="showTab('areas')">🗺️ Áreas & Cronograma</button>
  </div>

  <!-- ===================== TAB 1: OVERVIEW ===================== -->
  <div id="overview" class="tab-content active">

    <div class="kpi-row">
      <div class="kpi-card">
        <div class="kpi-label">Sobrevivência — Nativas</div>
        <div class="kpi-value">~70%</div>
        <div class="trend flat">→ estável vs. Maio/26</div>
      </div>
      <div class="kpi-card amber">
        <div class="kpi-label">Sobrevivência — Não Nativas</div>
        <div class="kpi-value">~30%</div>
        <div class="trend flat">→ estável vs. Maio/26</div>
      </div>
      <div class="kpi-card">
        <div class="kpi-label">Regeneração Natural</div>
        <div class="kpi-value">Elevada</div>
        <div class="trend up">▲ mantida desde Fev/26</div>
      </div>
      <div class="kpi-card">
        <div class="kpi-label">Área Total Monitorada</div>
        <div class="kpi-value">4,74 ha</div>
        <div class="kpi-sub">12 sub-áreas (A1–A20)</div>
      </div>
      <div class="kpi-card blue">
        <div class="kpi-label">Matriz de Risco Ambiental</div>
        <div class="kpi-value">3 Monitorados</div>
        <div class="kpi-sub">Nova estiagem, herbivoria, competição por gramíneas</div>
      </div>
      <div class="kpi-card red">
        <div class="kpi-label">Pragas / Herbivoria</div>
        <div class="kpi-value">Moderada</div>
        <div class="trend up" style="color:var(--success)">▼ de Moderada/Alta (Maio)</div>
      </div>
      <div class="kpi-card cyan">
        <div class="kpi-label">Tempo desde Fim da Execução</div>
        <div class="kpi-value" id="kpiImplantTime">—</div>
        <div class="kpi-sub">desde 15/12/2025</div>
      </div>
      <div class="kpi-card blue">
        <div class="kpi-label">Próximo Monitoramento</div>
        <div class="kpi-value" id="kpiCountdown">—</div>
        <div class="kpi-sub">Campanha 8 · 15/08/2026</div>
      </div>
      <div class="kpi-card cyan">
        <div class="kpi-label">Idade Fisiológica das Mudas desde Implantação</div>
        <div class="kpi-value" id="kpiPhysioAge">—</div>
        <div class="kpi-sub">75 dias de implantação + tempo desde 15/12/2025</div>
      </div>
      <div class="kpi-card">
        <div class="kpi-label">Crescimento Médio</div>
        <div class="kpi-value" id="kpiGrowthRate">—</div>
        <div class="kpi-sub">100 cm ÷ idade das mudas</div>
      </div>
      <div class="kpi-card">
        <div class="kpi-label">Altura Média Atual</div>
        <div class="kpi-value">1,00 m</div>
        <div class="kpi-sub">média das mudas monitoradas</div>
      </div>
    </div>

    <div class="note">📌 <b>Conclusão técnica:</b> Não foram verificadas alterações significativas frente a Maio/2026. Dados comparados desde maio-julho. Área em fase de estabilidade ecológica. Fatores supervenientes (estiagem, herbivoria) não caracterizam falha de implantação. Reposição de mudas <b>não recomendada</b> neste momento.</div>

    <div class="section-title">Painel Executivo — Indicadores Consolidados</div>
    <div class="grid-6">
      <div class="exec-card" data-ring="92" data-color="var(--success)">
        <div class="ring"><svg viewBox="0 0 90 90" width="74" height="74">
          <circle class="ring-bg" cx="45" cy="45" r="38"></circle>
          <circle class="ring-fg" cx="45" cy="45" r="38" stroke="var(--success)"></circle>
        </svg><div class="ring-val">92%</div></div>
        <div class="ring-label">Recuperação</div>
      </div>
      <div class="exec-card" data-ring="89" data-color="var(--cyan)">
        <div class="ring"><svg viewBox="0 0 90 90" width="74" height="74">
          <circle class="ring-bg" cx="45" cy="45" r="38"></circle>
          <circle class="ring-fg" cx="45" cy="45" r="38" stroke="var(--cyan)"></circle>
        </svg><div class="ring-val">89%</div></div>
        <div class="ring-label">Regeneração</div>
      </div>
      <div class="exec-card" data-ring="95" data-color="var(--success)">
        <div class="ring"><svg viewBox="0 0 90 90" width="74" height="74">
          <circle class="ring-bg" cx="45" cy="45" r="38"></circle>
          <circle class="ring-fg" cx="45" cy="45" r="38" stroke="var(--success)"></circle>
        </svg><div class="ring-val">95%</div></div>
        <div class="ring-label">Rebrota</div>
      </div>
      <div class="exec-card" data-ring="91" data-color="var(--blue3)">
        <div class="ring"><svg viewBox="0 0 90 90" width="74" height="74">
          <circle class="ring-bg" cx="45" cy="45" r="38"></circle>
          <circle class="ring-fg" cx="45" cy="45" r="38" stroke="var(--blue3)"></circle>
        </svg><div class="ring-val">91%</div></div>
        <div class="ring-label">Resiliência</div>
      </div>
      <div class="exec-card" data-ring="70" data-color="var(--warning)">
        <div class="ring"><svg viewBox="0 0 90 90" width="74" height="74">
          <circle class="ring-bg" cx="45" cy="45" r="38"></circle>
          <circle class="ring-fg" cx="45" cy="45" r="38" stroke="var(--warning)"></circle>
        </svg><div class="ring-val">70%</div></div>
        <div class="ring-label">Sobrevivência</div>
      </div>
      <div class="exec-card" data-ring="18" data-color="var(--danger)">
        <div class="ring"><svg viewBox="0 0 90 90" width="74" height="74">
          <circle class="ring-bg" cx="45" cy="45" r="38"></circle>
          <circle class="ring-fg" cx="45" cy="45" r="38" stroke="var(--danger)"></circle>
        </svg><div class="ring-val">18%</div></div>
        <div class="ring-label">Risco</div>
      </div>
    </div>

    <div class="section-title">Monitoramento em Tempo Real & Status de Desenvolvimento</div>
    <div class="grid-2">
      <div class="card">
        <h3>🌱 Status de Desenvolvimento das Mudas</h3>
        <div class="subtitle">Estágio fisiológico atual · calculado a partir da data de implantação</div>
        <div class="dev-stage-track" id="devStageTrack"></div>
        <div class="ia-grid" style="margin-top:14px">
          <div class="ia-item"><span class="check">✓</span>Herbivoria reduzida consideravelmente</div>
          <div class="ia-item"><span class="check">✓</span>Rebrotagem detectada em diversos indivíduos</div>
        </div>
        <div class="dev-compare">
          <div class="dev-col">
            <div class="dev-col-title" style="color:var(--success)">🌳 Nativas</div>
            <div class="dev-col-stage" id="devNativeStage">—</div>
            <div class="dev-col-note">Recuperação de copa em curso · maior plasticidade ecológica ao déficit hídrico do Semiárido.</div>
          </div>
          <div class="dev-col">
            <div class="dev-col-title" style="color:var(--warning)">🌿 Não Nativas</div>
            <div class="dev-col-stage" id="devExoticStage">—</div>
            <div class="dev-col-note">Estabelecimento mais lento · maior sensibilidade ao estresse hídrico e evaporativo.</div>
          </div>
        </div>
      </div>

      <div class="card">
        <h3>🌡️ Monitor Meteorológico — Caraúbas-PB</h3>
        <div class="subtitle">Dados em tempo real · Open-Meteo (fonte com API pública aberta)</div>
        <div id="weatherLive" class="weather-grid">
          <div class="weather-loading">Carregando dados meteorológicos em tempo real...</div>
        </div>
        <div class="weather-links">
          <span style="color:var(--text-sec);font-size:11px">Fontes complementares oficiais (sem API pública embutível — consulta manual):</span>
          <div class="wl-row">
            <a href="https://previsao.inmet.gov.br/" target="_blank" rel="noopener">INMET</a>
            <a href="https://www.cptec.inpe.br/" target="_blank" rel="noopener">CPTEC/INPE</a>
            <a href="https://queimadas.dgi.inpe.br/queimadas/portal" target="_blank" rel="noopener">INPE Queimadas</a>
            <a href="https://www.embrapa.br/agencia-de-informacao-tecnologica" target="_blank" rel="noopener">EMBRAPA AGEITEC</a>
            <a href="https://www.aesa.pb.gov.br/" target="_blank" rel="noopener">AESA-PB (Pluviometria)</a>
          </div>
        </div>
      </div>
    </div>

    <div class="grid-2">
      <div class="card">
        <h3>Sobrevivência das Mudas — Maio × Julho/2026</h3>
        <div class="subtitle">Comparação percentual por grupo de espécies</div>
        <canvas id="chartSurvival"></canvas>
      </div>
      <div class="card gauge-wrap">
        <h3 style="align-self:flex-start">Índice de Desenvolvimento</h3>
        <div class="subtitle" style="align-self:flex-start">Gauge consolidado — Julho/2026</div>
        <svg id="gaugeDev" viewBox="0 0 200 120" width="260" height="160">
          <path d="M20,110 A80,80 0 0 1 180,110" fill="none" stroke="#20293a" stroke-width="16" stroke-linecap="round"></path>
          <path id="gaugeArc" d="M20,110 A80,80 0 0 1 180,110" fill="none" stroke="url(#gaugeGrad)" stroke-width="16" stroke-linecap="round"
            stroke-dasharray="251.3" stroke-dashoffset="251.3"></path>
          <defs><linearGradient id="gaugeGrad" x1="0%" y1="0%" x2="100%" y2="0%">
            <stop offset="0%" stop-color="#FF5252"/><stop offset="50%" stop-color="#FFC107"/><stop offset="100%" stop-color="#00C853"/>
          </linearGradient></defs>
        </svg>
        <div class="gauge-val">83%</div>
        <div class="gauge-label">Desenvolvimento</div>
      </div>
    </div>

    <div class="grid-2">
      <div class="card">
        <h3>Distribuição dos Fatores no Monitoramento</h3>
        <div class="subtitle">Composição relativa (Figura 5)</div>
        <canvas id="chartDonut"></canvas>
      </div>
      <div class="card">
        <h3>Indicadores Integrados de Desempenho Ambiental</h3>
        <div class="subtitle">Avaliação qualitativa — Julho/2026 (escala 0–120)</div>
        <canvas id="chartIndicators"></canvas>
      </div>
    </div>

    <div class="grid-3">
      <div class="card">
        <h3>Crescimento das Mudas</h3>
        <div class="subtitle">Altura média acumulada (cm) — Dez/25 a Jul/26</div>
        <canvas id="chartGrowth"></canvas>
      </div>
      <div class="card">
        <h3>Herbivoria — Série Temporal</h3>
        <div class="subtitle">Índice de incidência mensal (Jan–Jul/26)</div>
        <canvas id="chartHerbivoria"></canvas>
      </div>
      <div class="card">
        <h3>Radar Ambiental</h3>
        <div class="subtitle">Indicadores multidimensionais — Julho/26</div>
        <canvas id="chartRadar"></canvas>
      </div>
    </div>

    <div class="grid-2">
      <div class="card">
        <h3>Alerta Fitossanitário</h3>
        <div class="subtitle">Status mensal por nível de risco</div>
        <div class="fito-row" id="fitoRow"></div>
      </div>
      <div class="card">
        <h3>Semáforo Ambiental</h3>
        <div class="subtitle">Indicadores operacionais — leitura rápida</div>
        <div class="semaforo" id="semaforoRow"></div>
      </div>
    </div>

    <div class="grid-2">
      <div class="card">
        <h3>Evolução Histórica do Monitoramento</h3>
        <div class="subtitle">Linha do tempo das campanhas — Quadro 1</div>
        <table>
          <thead><tr><th>Campanha</th><th>Situação Geral</th><th>Observações</th></tr></thead>
          <tbody id="tblHistorico"></tbody>
        </table>
      </div>
      <div class="ia-panel">
        <h3>🤖 IA Ambiental — Análise Automática</h3>
        <div class="ia-grid" id="iaGrid"></div>
      </div>
    </div>

  </div>

  <!-- ===================== TAB 2: SPECIES ===================== -->
  <div id="species" class="tab-content">

    <div class="section-title">Desempenho por Grupo de Espécies</div>
    <div class="grid-3">
      <div class="card">
        <h3>Espécies Nativas</h3>
        <div class="subtitle">Melhor desempenho do PRAD</div>
        <div class="kpi-value" style="font-size:34px">70%</div>
        <ul style="font-size:13px;color:var(--text-sec)">
          <li>Manutenção da maioria dos indivíduos</li>
          <li>Emissão de novas brotações</li>
          <li>Recuperação parcial da copa</li>
          <li>Maior plasticidade ecológica</li>
        </ul>
      </div>
      <div class="card">
        <h3>Espécies Não Nativas</h3>
        <div class="subtitle">Menor adaptação ao Semiárido</div>
        <div class="kpi-value" style="font-size:34px;color:var(--warning)">30%</div>
        <ul style="font-size:13px;color:var(--text-sec)">
          <li>Maior suscetibilidade ao estresse hídrico</li>
          <li>Maior demanda evaporativa</li>
          <li>Menor plasticidade ecológica</li>
        </ul>
      </div>
      <div class="card">
        <h3>Rebrota & Regeneração</h3>
        <div class="subtitle">Indicadores fisiológicos positivos</div>
        <p style="font-size:13px;"><span class="pill green">Rebrota: Presente</span></p>
        <p style="font-size:13px;"><span class="pill green">Regeneração Natural: Mantida</span></p>
        <p style="font-size:12.5px;color:var(--text-sec);margin-top:10px">Segundo Larcher (2006), rebrota evidencia sistema radicular funcional mesmo após perda foliar significativa — não configura perda definitiva.</p>
      </div>
    </div>

    <div class="grid-2">
      <div class="card">
        <h3>Tabela 1 — Comparação de Indicadores Maio × Julho/2026</h3>
        <table>
          <thead><tr><th>Indicador</th><th>Maio</th><th>Junho</th><th>Julho</th><th>Tendência</th></tr></thead>
          <tbody id="tblComparacao"></tbody>
        </table>
      </div>
      <div class="card">
        <h3>Tabela 4 — Indicadores Ecológicos</h3>
        <table>
          <thead><tr><th>Indicador</th><th>Maio</th><th>Junho</th><th>Julho</th></tr></thead>
          <tbody id="tblEcologicos"></tbody>
        </table>
      </div>
    </div>

    <div class="card">
      <h3>Situação das Ações de Manejo — Tabela 3</h3>
      <div class="subtitle">Status de execução por atividade</div>
      <table>
        <thead><tr><th>Ação</th><th>Situação</th></tr></thead>
        <tbody id="tblAcoes"></tbody>
      </table>
    </div>

  </div>

  <!-- ===================== TAB 3: FATORES SUPERVENIENTES ===================== -->
  <div id="factors" class="tab-content">

    <div class="note">⚠️ Fatores supervenientes: eventos posteriores à implantação, imprevisíveis, sem nexo causal com falha técnica de execução (ABNT NBR ISO 31000; IBAMA, 2011). O contrato do PRAD prevê apenas controle de formigas cortadeiras — não contempla controle de herbívoros desfolhadores.</div>

    <div class="grid-2">
      <div class="card">
        <h3>Intensidade dos Fatores Supervenientes</h3>
        <div class="subtitle">Escala: 1=Baixo · 2=Moderado · 3=Médio · 4=Alto · 5=Muito Alto</div>
        <canvas id="chartFactorsBar"></canvas>
      </div>
      <div class="card">
        <h3>Matriz de Risco Ambiental — Quadro 3</h3>
        <table>
          <thead><tr><th>Evento</th><th>Probabilidade</th><th>Impacto</th><th>Situação</th></tr></thead>
          <tbody id="tblRisco"></tbody>
        </table>
      </div>
    </div>

    <div class="card">
      <h3>Quadro 2 — Painel de Indicadores Ambientais Consolidado (Maio–Julho/2026)</h3>
      <table>
        <thead><tr><th>Fator</th><th>Influência Observada</th><th>Avaliação Técnica</th></tr></thead>
        <tbody id="tblPainel"></tbody>
      </table>
    </div>

    <div class="card">
      <h3>Fatores Supervenientes Consolidados — Influência</h3>
      <table>
        <thead><tr><th>Fator</th><th>Influência</th></tr></thead>
        <tbody id="tblFatoresConsolidados"></tbody>
      </table>
    </div>

  </div>

  <!-- ===================== TAB 4: MANEJO ===================== -->
  <div id="manejo" class="tab-content">

    <div class="section-title">Evolução das Atividades de Manejo (Figura 3)</div>
    <div class="card">
      <h3>Intensidade Relativa das Ações — Maio × Julho</h3>
      <div class="subtitle">Irrigação, manutenção hidráulica, monitoramento, capina/roçagem, inspeções técnicas</div>
      <canvas id="chartManejo"></canvas>
    </div>

    <div class="grid-2">
      <div class="card">
        <h3>Escopo do Monitoramento — Julho/2026</h3>
        <ul class="two-col-list">
          <li>✅ Inspeção técnica das áreas recuperadas</li>
          <li>✅ Avaliação da sobrevivência das mudas</li>
          <li>✅ Identificação de rebrotas</li>
          <li>✅ Verificação da regeneração natural</li>
          <li>✅ Avaliação da cobertura vegetal espontânea</li>
          <li>✅ Registro de evidências fotográficas</li>
          <li>✅ Acompanhamento de indivíduos atacados</li>
          <li>✅ Capina seletiva / coroamento / roçagem</li>
        </ul>
      </div>
      <div class="card">
        <h3>Fora do Escopo Contratual</h3>
        <p style="font-size:13px;color:var(--text-sec)">O plano executivo do PRAD <b>não contempla</b>:</p>
        <ul style="font-size:13px;color:var(--text-sec)">
          <li>Controle fitossanitário de insetos herbívoros desfolhadores</li>
          <li>Reposição automática de mudas por fatores supervenientes</li>
          <li>Controle previsto apenas para formigas cortadeiras</li>
        </ul>
        <p style="font-size:12.5px;margin-top:12px;">Eventuais intervenções extraordinárias dependem de avaliação técnica específica + manifestação formal da contratante e do órgão ambiental.</p>
      </div>
    </div>

  </div>

  <!-- ===================== TAB 5: AREAS & CRONOGRAMA ===================== -->
  <div id="areas" class="tab-content">

    <div class="grid-2">
      <div class="card">
        <h3>Áreas Monitoradas — Coordenadas e Extensão</h3>
        <table>
          <thead><tr><th>Área</th><th>Latitude (S)</th><th>Longitude (W)</th><th>Área (ha)</th></tr></thead>
          <tbody id="tblAreas"></tbody>
        </table>
      </div>
      <div class="card">
        <h3>Distribuição de Área por Talhão (ha)</h3>
        <canvas id="chartAreas"></canvas>
      </div>
    </div>

    <div class="card">
      <h3>Cronograma de Monitoramento (12 campanhas)</h3>
      <div class="subtitle">✓ = concluído</div>
      <table>
        <thead><tr><th>Monitoramento</th><th>Data Prevista</th><th>Status</th></tr></thead>
        <tbody id="tblCronograma"></tbody>
      </table>
    </div>

  </div>

  <div class="footer">
    Dashboard gerado a partir do Relatório Técnico de Monitoramento — UFV Rio do Peixe I e II — Julho/2026 · Bragagnoli Ambiental (CTF/AIDA 8805586) · Diretor Técnico: Railson Nogueira de Arruda, Eng. Ambiental, CREA-PB RNP 1619008858, ART PB20250690039
  </div>

</div>

<script>
function showTab(id){
  document.querySelectorAll('.tab-content').forEach(t=>t.classList.remove('active'));
  document.querySelectorAll('.tab-btn').forEach(b=>b.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  event.target.classList.add('active');
}

Chart.defaults.font.family = "'Segoe UI',Arial,sans-serif";
Chart.defaults.color = '#8b949e';
Chart.defaults.borderColor = '#232c3d';
const GREEN='#00C853', GREEN_D='#0b3d91', AMBER='#FFC107', RED='#FF5252', BLUE='#2196F3', CYAN='#00BCD4';

// --- Chart 1: Survival comparison ---
new Chart(document.getElementById('chartSurvival'), {
  type:'bar',
  data:{
    labels:['Espécies Nativas','Espécies Não Nativas'],
    datasets:[
      {label:'Maio', data:[70,30], backgroundColor:BLUE, borderRadius:6},
      {label:'Junho', data:[70,30], backgroundColor:CYAN, borderRadius:6},
      {label:'Julho', data:[70,30], backgroundColor:GREEN, borderRadius:6}
    ]
  },
  options:{responsive:true, scales:{y:{beginAtZero:true,max:80,ticks:{callback:v=>v+'%'}}}, plugins:{legend:{position:'bottom'}}}
});

// --- Chart 2: Donut fatores ---
new Chart(document.getElementById('chartDonut'), {
  type:'doughnut',
  data:{
    labels:['Ações de manejo executadas','Déficit hídrico regional','Herbivoria','Irrigação emergencial','Rebrota das mudas'],
    datasets:[{data:[30,12,15,25,18], backgroundColor:[GREEN_D,AMBER,RED,BLUE,CYAN]}]
  },
  options:{responsive:true, plugins:{legend:{position:'bottom',labels:{boxWidth:10,font:{size:11}}}}}
});

// --- Chart 3: Indicadores integrados (Figura 4) ---
new Chart(document.getElementById('chartIndicators'), {
  type:'bar',
  data:{
    labels:['Funcionamento da irrigação','Estabilidade do plantio','Rebrota observada','Controle operacional','Herbivoria','Déficit hídrico'],
    datasets:[{data:[100,90,85,92,35,25], backgroundColor:[GREEN,GREEN,CYAN,GREEN,AMBER,AMBER], borderRadius:6}]
  },
  options:{indexAxis:'y', responsive:true, plugins:{legend:{display:false}}, scales:{x:{max:120}}}
});

// --- Chart Growth ---
new Chart(document.getElementById('chartGrowth'), {
  type:'line',
  data:{
    labels:['Dez','Jan','Fev','Mar','Abr','Mai','Jun','Jul'],
    datasets:[{label:'Altura média (cm)', data:[0,15,32,55,73,89,96,100], borderColor:CYAN, backgroundColor:CYAN+'25', tension:.4, fill:true, pointBackgroundColor:CYAN}]
  },
  options:{responsive:true, plugins:{legend:{display:false}}, scales:{y:{beginAtZero:true,max:110,ticks:{callback:v=>v+'cm'}}}}
});

// --- Chart Herbivoria ---
new Chart(document.getElementById('chartHerbivoria'), {
  type:'line',
  data:{
    labels:['Jan','Fev','Mar','Abr','Mai','Jun','Jul'],
    datasets:[{label:'Índice herbivoria', data:[0,2,4,6,9,7,2], borderColor:RED, backgroundColor:RED+'22', tension:.4, fill:true, pointBackgroundColor:RED}]
  },
  options:{responsive:true, plugins:{legend:{display:false}}, scales:{y:{beginAtZero:true,max:10}}}
});

// --- Chart Radar Ambiental ---
new Chart(document.getElementById('chartRadar'), {
  type:'radar',
  data:{
    labels:['Solo','Umidade','Cobertura','Rebrota','Pragas','Resiliência','Sobrevivência'],
    datasets:[{label:'Índice', data:[88,72,85,95,60,91,70], borderColor:CYAN, backgroundColor:CYAN+'2A', pointBackgroundColor:CYAN}]
  },
  options:{responsive:true, plugins:{legend:{display:false}}, scales:{r:{beginAtZero:true,max:100,
    grid:{color:'#232c3d'}, angleLines:{color:'#232c3d'}, pointLabels:{color:'#c9d1d9',font:{size:11}}, ticks:{display:false}}}}
});

// --- Historico table ---
const historico = [
 ['Fevereiro/2026','Plantio concluído','Início da fase de estabelecimento'],
 ['Março/2026','Irrigação intensiva','Funcionamento contínuo do sistema'],
 ['Abril/2026','Continuidade da irrigação','Manutenções preventivas de motobombas e mangueiras'],
 ['Maio/2026','Encerramento da irrigação emergencial','Consolidação das mudas sobreviventes'],
 ['Junho/2026','Estabilidade do cenário','Sem alterações significativas nos indicadores'],
 ['Julho/2026','Estabilidade do cenário','Sem alterações significativas nos indicadores'],
];
document.getElementById('tblHistorico').innerHTML = historico.map(r=>
 `<tr><td><b>${r[0]}</b></td><td>${r[1]}</td><td>${r[2]}</td></tr>`).join('');

// --- Comparacao Maio x Julho (Tabela 1) ---
const comp = [
 ['Mortalidade','Estável','Estável','Estável','flat'],
 ['Regeneração Natural','Elevada','Elevada','Elevada','flat'],
 ['Cobertura Vegetal','Estável','Estável','Estável','flat'],
 ['Pragas','Moderada/Alta','Moderada','Baixa','down'],
 ['Rebrota','Presente','Presente','Presente','flat'],
 ['Necessidade de Irrigação','Não','Não','Não','flat'],
 ['Necessidade de Capina','Sim','Sim','Sim','flat'],
 ['Necessidade de Coroamento','Sim','Sim','Sim','flat'],
];
const arrow = t => t==='down' ? '<span class="arrow" style="color:var(--success)">↓</span>' : '<span class="arrow" style="color:#8b949e">→</span>';
document.getElementById('tblComparacao').innerHTML = comp.map(r=>
 `<tr><td>${r[0]}</td><td>${r[1]}</td><td>${r[2]}</td><td>${r[3]}</td><td>${arrow(r[4])}</td></tr>`).join('');

// --- Indicadores ecologicos (Tabela 4) ---
const ecolog = [
 ['Regeneração Natural','Favorável','Favorável','Favorável'],
 ['Rebrota','Favorável','Favorável','Favorável'],
 ['Cobertura do Solo','Favorável','Favorável','Favorável'],
 ['Controle de Processos Erosivos','Favorável','Favorável','Favorável'],
 ['Serviços Ecossistêmicos','Em recuperação','Em recuperação','Em recuperação'],
];
document.getElementById('tblEcologicos').innerHTML = ecolog.map(r=>
 `<tr><td>${r[0]}</td><td><span class="pill green">${r[1]}</span></td><td><span class="pill green">${r[2]}</span></td><td><span class="pill green">${r[3]}</span></td></tr>`).join('');

// --- Acoes de manejo (Tabela 3) ---
const acoes = [
 ['Irrigação emergencial','Concluída','green'],
 ['Manutenção das motobombas','Executada','green'],
 ['Reparo das mangueiras','Executado','green'],
 ['Reinstalação das bombas','Executada','green'],
 ['Capina seletiva','Em execução','amber'],
 ['Coroamento','Em execução','amber'],
 ['Monitoramento','Contínuo','blue'],
];
document.getElementById('tblAcoes').innerHTML = acoes.map(r=>
 `<tr><td>${r[0]}</td><td><span class="pill ${r[2]}">${r[1]}</span></td></tr>`).join('');

// --- Chart Fatores Supervenientes (bar horizontal) ---
new Chart(document.getElementById('chartFactorsBar'), {
  type:'bar',
  data:{
    labels:['Estiagem prolongada','Elevadas temperaturas','Herbivoria (lagartas/gafanhotos)','Competição por vegetação espontânea','Necessidade de roçagem','Falhas hidráulicas pontuais'],
    datasets:[{data:[5,4,4,3,3,2], backgroundColor:[RED,RED,AMBER,AMBER,AMBER,BLUE], borderRadius:6}]
  },
  options:{indexAxis:'y', responsive:true, plugins:{legend:{display:false}}, scales:{x:{max:5}}}
});

// --- Matriz de risco (Quadro 3) ---
const risco = [
 ['Mortalidade adicional','Baixa','Média','Controlado','green'],
 ['Nova estiagem','Média','Alta','Monitorado','amber'],
 ['Herbivoria','Média','Média','Monitorado','amber'],
 ['Competição por gramíneas','Alta','Média','Em manejo','amber'],
 ['Erosão','Baixa','Baixa','Sem evidências','green'],
];
document.getElementById('tblRisco').innerHTML = risco.map(r=>
 `<tr><td>${r[0]}</td><td>${r[1]}</td><td>${r[2]}</td><td><span class="pill ${r[4]}">${r[3]}</span></td></tr>`).join('');

// --- Painel indicadores (Quadro 2) ---
const painel = [
 ['Irrigação inicial','Redução do estresse pós-plantio','Medida executada'],
 ['Manutenção hidráulica','Garantia operacional','Ação preventiva/corretiva realizada'],
 ['Ambiente semiárido','Restrição hídrica natural','Condicionante ambiental'],
 ['Espécies implantadas','Diferentes respostas','Maior adaptação das nativas'],
 ['Vegetação concorrente','Competição localizada','Manejo iniciado'],
 ['Herbivoria','Danos foliares e brotações','Fator superveniente'],
 ['Rebrota','Recuperação fisiológica de alguns indivíduos','Indicador positivo'],
];
document.getElementById('tblPainel').innerHTML = painel.map(r=>
 `<tr><td><b>${r[0]}</b></td><td>${r[1]}</td><td>${r[2]}</td></tr>`).join('');

// --- Fatores consolidados influencia ---
const fcons = [
 ['Estiagem prolongada','Muito alta','red'],
 ['Elevadas temperaturas','Alta','red'],
 ['Herbivoria','Alta','amber'],
 ['Competição com vegetação espontânea','Moderada','amber'],
 ['Necessidade de roçagem','Moderada','amber'],
 ['Manutenção do sistema de irrigação','Controlada','green'],
 ['Interrupções operacionais','Pontuais','green'],
];
document.getElementById('tblFatoresConsolidados').innerHTML = fcons.map(r=>
 `<tr><td>${r[0]}</td><td><span class="pill ${r[2]}">${r[1]}</span></td></tr>`).join('');

// --- Chart Manejo (Figura 3) ---
new Chart(document.getElementById('chartManejo'), {
  type:'line',
  data:{
    labels:['Irrigação','Manutenção hidráulica','Monitoramento','Capina/roçagem','Inspeções técnicas'],
    datasets:[
      {label:'Maio', data:[5,2,2,2,4], borderColor:BLUE, backgroundColor:BLUE+'30', tension:.4, fill:true},
      {label:'Junho', data:[2,2,5,5,5], borderColor:GREEN, backgroundColor:GREEN+'30', tension:.4, fill:true}
    ]
  },
  options:{responsive:true, scales:{y:{beginAtZero:true,max:6}}, plugins:{legend:{position:'bottom'}}}
});

// --- Areas monitoradas ---
const areas = [
 ['A1',"7°42'45\"","36°32'38\"",0.65],
 ['A4',"7°42'43\"","36°32'45\"",0.36],
 ['A5',"7°42'46\"","36°32'54\"",0.10],
 ['A6',"7°42'53\"","36°33'12\"",0.04],
 ['A9',"7°42'57\"","36°32'25\"",0.11],
 ['A10',"7°43'07\"","36°32'21\"",0.10],
 ['A12',"7°42'57\"","36°32'25\"",0.33],
 ['A13',"7°42'51\"","36°32'38\"",0.88],
 ['A14',"7°42'49\"","36°32'44\"",0.33],
 ['A15',"7°42'53\"","36°32'51\"",0.26],
 ['A16',"7°42'52\"","36°32'52\"",0.17],
 ['A17',"7°42'52\"","36°32'56\"",0.26],
 ['A20',"7°43'10\"","36°33'13\"",1.15],
];
document.getElementById('tblAreas').innerHTML = areas.map(r=>
 `<tr><td><b>${r[0]}</b></td><td>${r[1]} S</td><td>${r[2]} W</td><td>${r[3].toFixed(2)} ha</td></tr>`).join('')
 + `<tr style="background:#101a2c;font-weight:700"><td colspan="3">TOTAL</td><td>4,74 ha</td></tr>`;

new Chart(document.getElementById('chartAreas'), {
  type:'bar',
  data:{
    labels: areas.map(a=>a[0]),
    datasets:[{data: areas.map(a=>a[3]), backgroundColor:CYAN, borderRadius:5}]
  },
  options:{responsive:true, plugins:{legend:{display:false}}, scales:{y:{title:{display:true,text:'hectares'}}}}
});

// --- Cronograma ---
const crono = [
 ['Monitoramento 1','15/12/2025',true],
 ['Monitoramento 2','15/01/2026',true],
 ['Monitoramento 3','15/02/2026',true],
 ['Monitoramento 4','15/03/2026',true],
 ['Monitoramento 5','15/04/2026',true],
 ['Monitoramento 6','15/05/2026',true],
 ['Monitoramento 7','15/06/2026',true],
 ['Monitoramento 8','15/07/2026',false],
 ['Monitoramento 9','15/08/2026',false],
 ['Monitoramento 10','15/09/2026',false],
 ['Monitoramento 11','15/10/2026',false],
 ['Monitoramento 12','15/11/2026',false],
];
document.getElementById('tblCronograma').innerHTML = crono.map(r=>
 `<tr><td>${r[0]}</td><td>${r[1]}</td><td>${r[2]?'<span class="pill green">✓ Concluído</span>':'<span class="pill blue">Programado</span>'}</td></tr>`).join('');

// ===================== NEW: DYNAMIC WIDGETS =====================

// Exec ring animation (stroke-dashoffset)
document.querySelectorAll('.exec-card').forEach(card=>{
  const pct = parseFloat(card.dataset.ring);
  const circle = card.querySelector('.ring-fg');
  const r = 38, circumference = 2*Math.PI*r;
  circle.style.strokeDasharray = circumference;
  circle.style.strokeDashoffset = circumference;
  requestAnimationFrame(()=>{ circle.style.strokeDashoffset = circumference - (pct/100)*circumference; });
});

// Gauge arc animation (semi-circle path length ~251.3)
requestAnimationFrame(()=>{
  const arcLen = 251.3, pct = 83;
  document.getElementById('gaugeArc').style.strokeDashoffset = arcLen - (pct/100)*arcLen;
});

// Fitossanitário panel
const fito = [
 ['Jan','#00C853'],['Fev','#00C853'],['Mar','#FFC107'],['Abr','#FF9800'],['Mai','#FF5252'],['Jun','#FF9800'],['Jul','#00C853']
];
document.getElementById('fitoRow').innerHTML = fito.map(f=>
 `<div class="fito-item"><div class="fito-dot" style="background:${f[1]};color:${f[1]}"></div><div class="fito-month">${f[0]}</div></div>`).join('');

// Semáforo Ambiental
const semaforo = [
 ['Solo','#00C853'],['Irrigação','#00C853'],['Crescimento','#00C853'],['Rebrota','#00C853'],
 ['Cobertura','#00C853'],['Estiagem','#FFC107'],['Herbivoria','#00C853']
];
document.getElementById('semaforoRow').innerHTML = semaforo.map(s=>
 `<div class="sem-item"><span class="sem-dot" style="background:${s[1]};color:${s[1]}"></span>${s[0]}</div>`).join('');

// IA Ambiental conclusões
const iaConclusoes = [
 'Sem necessidade de replantio',
 'Herbivoria em redução',
 'Regeneração ativa',
 'Manejo adequado',
 'Recuperação fisiológica positiva',
 'Tendência ecológica estável'
];
document.getElementById('iaGrid').innerHTML = iaConclusoes.map(c=>
 `<div class="ia-item"><span class="check">✓</span>${c}</div>`).join('');

// ===================== LIVE CLOCK / DATE / COUNTERS =====================
const IMPLANT_DATE = new Date(2026,1,1,0,0,0); // 01/02/2026 - referência para estágio de desenvolvimento
const EXEC_END_DATE = new Date(2025,11,15,0,0,0); // 15/12/2025 - fim da execução do plantio
const IMPLANT_BASE_DAYS = 75; // tempo total do processo de implantação
const NEXT_MONITOR = new Date(2026,7,15,0,0,0); // 15/08/2026

function pad(n){return String(n).padStart(2,'0');}

function updateClock(){
  const now = new Date();
  document.getElementById('liveClock').textContent = `${pad(now.getHours())}:${pad(now.getMinutes())}:${pad(now.getSeconds())}`;
  const dias=['domingo','segunda-feira','terça-feira','quarta-feira','quinta-feira','sexta-feira','sábado'];
  const meses=['janeiro','fevereiro','março','abril','maio','junho','julho','agosto','setembro','outubro','novembro','dezembro'];
  document.getElementById('liveDate').textContent = `${dias[now.getDay()]}, ${now.getDate()} de ${meses[now.getMonth()]} de ${now.getFullYear()}`;

  // Tempo desde fim da execução (15/12/2025)
  const diffMs = now - EXEC_END_DATE;
  const totalDays = Math.floor(diffMs/86400000);
  const years = Math.floor(totalDays/365);
  const months = Math.floor((totalDays%365)/30);
  const days = (totalDays%365)%30;
  document.getElementById('kpiImplantTime').textContent = `${years}a ${months}m ${days}d`;

  // Idade fisiológica = 75 dias de implantação + dias desde fim da execução
  const physioAgeDays = IMPLANT_BASE_DAYS + totalDays;
  document.getElementById('kpiPhysioAge').textContent = `${physioAgeDays} dias`;

  // Crescimento médio cm/dia = 100 / idade fisiológica total
  const growth = physioAgeDays>0 ? (100/physioAgeDays) : 0;
  document.getElementById('kpiGrowthRate').textContent = `${growth.toFixed(3)} cm/dia`;

  // Countdown próximo monitoramento
  const rem = NEXT_MONITOR - now;
  if(rem>0){
    const rd = Math.floor(rem/86400000);
    const rh = Math.floor((rem%86400000)/3600000);
    const rm = Math.floor((rem%3600000)/60000);
    const rs = Math.floor((rem%60000)/1000);
    document.getElementById('kpiCountdown').textContent = `${rd}d ${pad(rh)}:${pad(rm)}:${pad(rs)}`;
  } else {
    document.getElementById('kpiCountdown').textContent = 'Vencido';
  }
}
// ===================== DEV STAGE (Nativas x Não Nativas) =====================
const devStages = [
 {icon:'🌱',name:'Aquisição'},
 {icon:'🌿',name:'Estabelecimento'},
 {icon:'🪴',name:'Crescimento Ativo'},
 {icon:'🌳',name:'Consolidação'}
];
function renderDevTrack(activeIdx){
  const track = document.getElementById('devStageTrack');
  track.innerHTML = devStages.map((s,i)=>
   `<div class="dev-step ${i===activeIdx?'active':''} ${i<activeIdx?'done':''}">
      <div class="dev-icon">${s.icon}</div><div class="dev-name">${s.name}</div>
    </div>`).join('');
}
function updateDevStage(totalDays){
  // Nativas: desenvolvimento mais rápido (plasticidade maior)
  const nativeIdx = totalDays<45?0:totalDays<110?1:totalDays<180?2:3;
  // Não nativas: desenvolvimento mais lento (maior sensibilidade hídrica)
  const exoticIdx = totalDays<70?0:totalDays<150?1:totalDays<230?2:3;
  renderDevTrack(nativeIdx);
  document.getElementById('devNativeStage').textContent = devStages[nativeIdx].name;
  document.getElementById('devExoticStage').textContent = devStages[exoticIdx].name;
}

// ===================== LIVE WEATHER (Open-Meteo — API pública, sem chave) =====================
const WX_LAT=-7.727, WX_LON=-36.492;
async function loadWeather(){
  const el = document.getElementById('weatherLive');
  try{
    const url = `https://api.open-meteo.com/v1/forecast?latitude=${WX_LAT}&longitude=${WX_LON}&current=temperature_2m,relative_humidity_2m,precipitation,wind_speed_10m,wind_direction_10m&daily=precipitation_sum,temperature_2m_max,temperature_2m_min&timezone=America%2FSao_Paulo`;
    const res = await fetch(url);
    if(!res.ok) throw new Error('fetch failed');
    const data = await res.json();
    const c = data.current;
    const d = data.daily;
    const dirs=['N','NE','L','SE','S','SO','O','NO'];
    const dirTxt = dirs[Math.round(c.wind_direction_10m/45)%8];
    el.innerHTML = `
      <div class="w-item"><div class="w-val">${c.temperature_2m.toFixed(1)}°C</div><div class="w-lbl">Temperatura</div></div>
      <div class="w-item"><div class="w-val">${c.relative_humidity_2m}%</div><div class="w-lbl">Umidade</div></div>
      <div class="w-item"><div class="w-val">${c.wind_speed_10m.toFixed(1)} km/h</div><div class="w-lbl">Vento ${dirTxt}</div></div>
      <div class="w-item"><div class="w-val">${c.precipitation.toFixed(1)} mm</div><div class="w-lbl">Precipitação atual</div></div>
      <div class="w-item"><div class="w-val">${d.temperature_2m_max[0].toFixed(0)}° / ${d.temperature_2m_min[0].toFixed(0)}°</div><div class="w-lbl">Máx / Mín hoje</div></div>
      <div class="w-item"><div class="w-val">${d.precipitation_sum[0].toFixed(1)} mm</div><div class="w-lbl">Chuva acumulada (dia)</div></div>
      <div class="w-updated">Atualizado ${new Date().toLocaleTimeString('pt-BR')} · fonte: Open-Meteo (lat ${WX_LAT}, lon ${WX_LON})</div>`;
  }catch(e){
    el.innerHTML = `<div class="weather-loading">Sem conexão com a API meteorológica no momento. Consulte as fontes oficiais abaixo.</div>`;
  }
}
loadWeather();
setInterval(loadWeather, 10*60*1000);

updateClock();
updateDevStage(Math.floor((new Date()-IMPLANT_DATE)/86400000));
setInterval(updateClock, 1000);
setInterval(()=>updateDevStage(Math.floor((new Date()-IMPLANT_DATE)/86400000)), 60000);
</script>
</body>
</html>
