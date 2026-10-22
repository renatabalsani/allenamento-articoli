<!doctype html><html><head><meta charset=utf8><meta name=viewport content="width=device-width,initial-scale=1,viewport-fit=cover"><style>:root{color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}html{scroll-padding-top:env(safe-area-inset-top,0px)}body{margin:0;padding:0;font:14px -apple-system,BlinkMacSystemFont,sans-serif;background:#fff;color:#000}img{max-width:100%}[hidden]:not([hidden=until-found i]){display:none!important}</style></head><body>
<title>Allenamento Articoli</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,500;9..144,700&family=Atkinson+Hyperlegible:wght@400;700&display=swap">
<style>
/* Layout: palestra di italiano — due schede (Esercizi / Grammatica); esercizi in griglia di tessere che aprono un'area di gioco; colonna unica */
:root{
  --bg:#f6f7f4; --surface:#ffffff; --fg:#1f2a26; --muted:#5d6b65; --line:#d9dfdb;
  --accent:#1d6b52; --accent-soft:#e3f0ea; --fem:#9a3b56; --fem-soft:#f6e6ec;
  --hl:#8a5a00; --hl-soft:#fbf0d9; --blue:#2f5d8a; --blue-soft:#e4edf6;
  --ok:#1f7a3d; --ok-soft:#e2f3e7; --bad:#b3261e; --bad-soft:#fbe5e3;
  --display:"Fraunces",Georgia,serif; --body:"Atkinson Hyperlegible",system-ui,sans-serif;
}
@media (prefers-color-scheme: dark){:root:not([data-theme="light"]){
  --bg:#141a18; --surface:#1c2421; --fg:#e7ece9; --muted:#9aa8a2; --line:#2e3935;
  --accent:#6fc7a5; --accent-soft:#1f3a30; --fem:#e894ad; --fem-soft:#3d2430;
  --hl:#f0c46a; --hl-soft:#3a2f17; --blue:#8fb8e3; --blue-soft:#1e2d3d;
  --ok:#7ed69a; --ok-soft:#1d3a27; --bad:#f2938a; --bad-soft:#3e2220; color-scheme:dark}}
:root[data-theme="dark"]{
  --bg:#141a18; --surface:#1c2421; --fg:#e7ece9; --muted:#9aa8a2; --line:#2e3935;
  --accent:#6fc7a5; --accent-soft:#1f3a30; --fem:#e894ad; --fem-soft:#3d2430;
  --hl:#f0c46a; --hl-soft:#3a2f17; --blue:#8fb8e3; --blue-soft:#1e2d3d;
  --ok:#7ed69a; --ok-soft:#1d3a27; --bad:#f2938a; --bad-soft:#3e2220; color-scheme:dark}
body{background:var(--bg);color:var(--fg);font-family:var(--body);font-size:16px;line-height:1.55;
  padding-left:max(16px,env(safe-area-inset-left,0px));padding-right:max(16px,env(safe-area-inset-right,0px));padding-block:24px 56px}
main{max-width:800px;margin:0 auto;display:grid;gap:28px}
h1,h2,h3{font-family:var(--display);text-wrap:balance;margin:0}
h1{font-size:2rem;line-height:1.15}
h2{font-size:1.35rem}
h3{font-size:1.05rem}
p{margin:0}
.lead{color:var(--muted);margin-top:6px}
.note{font-size:.92rem;color:var(--muted)}
[hidden]{display:none!important}
button{font:inherit;color:inherit}
button:focus-visible,a:focus-visible,select:focus-visible,input:focus-visible{outline:2px solid var(--accent);outline-offset:2px}

/* schede */
.tabs{display:flex;gap:4px;border-bottom:1px solid var(--line)}
.tabs button{padding:10px 16px;border:0;background:none;cursor:pointer;color:var(--muted);font-weight:700;border-bottom:3px solid transparent;margin-bottom:-1px}
.tabs button[aria-selected="true"]{color:var(--fg);border-color:var(--accent)}

/* statistiche */
.stats{display:grid;grid-template-columns:repeat(4,1fr);gap:8px}
.stat{background:var(--surface);border:1px solid var(--line);border-radius:10px;padding:10px 12px;min-width:0}
.stat b{display:block;font-family:var(--display);font-size:1.5rem;font-variant-numeric:tabular-nums;line-height:1.2}
.stat span{font-size:.78rem;color:var(--muted)}
@media (max-width:520px){.stats{grid-template-columns:repeat(2,1fr)}}

/* tessere */
.tiles{display:grid;grid-template-columns:repeat(auto-fill,minmax(230px,1fr));gap:12px}
.tile{text-align:left;background:var(--surface);border:1px solid var(--line);border-radius:12px;padding:16px;cursor:pointer;display:grid;gap:6px;align-content:start;min-width:0}
.tile:hover{border-color:var(--accent)}
.tile h3{font-size:1.1rem}
.tile p{font-size:.9rem;color:var(--muted)}
.chip{justify-self:start;font-size:.7rem;font-weight:700;letter-spacing:.06em;text-transform:uppercase;padding:2px 8px;border-radius:99px}
.c-art{background:var(--accent-soft);color:var(--accent)}
.c-verb{background:var(--fem-soft);color:var(--fem)}
.c-voc{background:var(--blue-soft);color:var(--blue)}
.c-mix{background:var(--hl-soft);color:var(--hl)}
.groupt{font-size:.78rem;text-transform:uppercase;letter-spacing:.08em;color:var(--muted);font-weight:700;margin-top:6px}

/* area di gioco */
.ghead{display:flex;flex-wrap:wrap;align-items:center;gap:10px 14px}
.back{border:1px solid var(--line);background:var(--surface);border-radius:99px;padding:6px 14px;cursor:pointer;font-size:.9rem}
.modes{display:flex;flex-wrap:wrap;gap:8px}
.modes button{font-size:.86rem;padding:6px 13px;border-radius:99px;border:1px solid var(--line);background:transparent;cursor:pointer}
.modes button[aria-pressed="true"]{background:var(--accent);border-color:var(--accent);color:var(--surface)}
.card{background:var(--surface);border:1px solid var(--line);border-radius:14px;padding:20px;display:grid;gap:16px;min-width:0}
.prog{height:6px;background:var(--line);border-radius:99px;overflow:hidden}
.prog span{display:block;height:100%;background:var(--accent);transition:width .3s}
.qmeta{color:var(--muted);font-size:.9rem}
.word{font-family:var(--display);font-size:1.7rem;font-weight:700;line-height:1.35;overflow-wrap:anywhere}
.word.big{font-size:2.2rem}
.blank{display:inline-block;min-width:2.8em;border-bottom:3px solid var(--hl);text-align:center;color:var(--hl)}
.pron{color:var(--muted);font-weight:500}
.opts{display:grid;grid-template-columns:repeat(auto-fill,minmax(84px,1fr));gap:8px}
.opts.wide{grid-template-columns:repeat(auto-fill,minmax(180px,1fr))}
.opt{font-family:var(--display);font-size:1.12rem;font-weight:700;padding:12px 8px;border-radius:10px;border:1px solid var(--line);background:var(--bg);cursor:pointer;line-height:1.25}
.opts.wide .opt{font-family:var(--body);font-size:1rem;font-weight:400;text-align:left;padding:12px 14px}
.opt:hover:not(:disabled){border-color:var(--accent)}
.opt.right{background:var(--ok-soft);border-color:var(--ok);color:var(--ok)}
.opt.wrong{background:var(--bad-soft);border-color:var(--bad);color:var(--bad)}
.opt:disabled{cursor:default}
.typing{display:flex;gap:8px;flex-wrap:wrap}
.typing input{flex:1 1 180px;min-width:0;font-family:var(--display);font-size:1.25rem;padding:10px 12px;border-radius:10px;border:1px solid var(--line);background:var(--bg);color:var(--fg)}
.btn2{font-weight:700;padding:10px 18px;border-radius:10px;border:1px solid var(--accent);background:transparent;color:var(--accent);cursor:pointer}
.fb{min-height:3.5em}
.fb.ok{color:var(--ok)} .fb.no{color:var(--bad)}
.fb small{display:block;color:var(--muted);margin-top:4px;font-size:.92rem}
.bar{display:flex;flex-wrap:wrap;justify-content:space-between;align-items:center;gap:12px}
.score{font-variant-numeric:tabular-nums;color:var(--muted);font-size:.92rem}
.next{font-weight:700;padding:10px 20px;border-radius:10px;border:0;background:var(--accent);color:var(--surface);cursor:pointer}
.next:disabled{opacity:.4;cursor:default}
.summary{display:grid;gap:12px}
.summary .big{font-family:var(--display);font-size:2.6rem;font-weight:700;font-variant-numeric:tabular-nums}
.errlist{display:grid;gap:8px;margin:0;padding:0;list-style:none}
.errlist li{border-left:3px solid var(--bad);padding:4px 10px;font-size:.93rem}
.errlist li small{display:block;color:var(--muted)}
.row{display:flex;flex-wrap:wrap;gap:8px}

/* raffica */
.timer{display:flex;align-items:center;gap:12px}
.timer .prog{flex:1}
.timer .prog span{background:var(--hl);transition:width .25s linear}
.clock{font-family:var(--display);font-weight:700;font-size:1.3rem;font-variant-numeric:tabular-nums;min-width:2.5em;text-align:right}
.combo{font-weight:700;color:var(--hl)}
.flash{animation:fl .35s}
@keyframes fl{from{transform:scale(1.04)}to{transform:none}}
@media (prefers-reduced-motion:reduce){.flash{animation:none}.prog span{transition:none}}

/* trova l'errore / riordina */
.tokens{display:flex;flex-wrap:wrap;gap:6px}
.tok{font-family:var(--display);font-size:1.25rem;padding:6px 10px;border-radius:8px;border:1px solid var(--line);background:var(--bg);cursor:pointer}
.tok:hover:not(:disabled){border-color:var(--accent)}
.tok.right{background:var(--ok-soft);border-color:var(--ok);color:var(--ok)}
.tok.wrong{background:var(--bad-soft);border-color:var(--bad);color:var(--bad)}
.tok.used{opacity:.25}
.tok:disabled{cursor:default}
.answerline{min-height:3.2em;border:2px dashed var(--line);border-radius:10px;padding:8px;display:flex;flex-wrap:wrap;gap:6px;align-items:center}
.answerline.ok{border-color:var(--ok);border-style:solid}
.answerline.no{border-color:var(--bad);border-style:solid}
.hint{color:var(--muted);font-style:italic}

/* testo da completare */
.cloze{font-size:1.08rem;line-height:2.3}
.cloze select{font:inherit;font-weight:700;padding:2px 6px;border-radius:8px;border:1px solid var(--hl);background:var(--hl-soft);color:var(--fg);max-width:100%}
.cloze select.right{border-color:var(--ok);background:var(--ok-soft);color:var(--ok)}
.cloze select.wrong{border-color:var(--bad);background:var(--bad-soft);color:var(--bad)}

/* abbinamenti */
.match{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.match .col{display:grid;gap:8px;align-content:start;min-width:0}
.mt{text-align:left;padding:10px 12px;border-radius:10px;border:1px solid var(--line);background:var(--bg);cursor:pointer;font-size:.95rem;line-height:1.3;overflow-wrap:anywhere}
.mt.it{font-family:var(--display);font-weight:700;font-size:1.02rem}
.mt.sel{border-color:var(--accent);background:var(--accent-soft)}
.mt.done{background:var(--ok-soft);border-color:var(--ok);color:var(--ok);cursor:default}
.mt.bad{background:var(--bad-soft);border-color:var(--bad)}

/* grammatica */
.gram{display:grid;gap:32px}
.gram section{display:grid;gap:14px}
.toc{display:flex;flex-wrap:wrap;gap:8px}
.toc a{font-size:.85rem;color:var(--accent);text-decoration:none;border:1px solid var(--line);border-radius:99px;padding:4px 12px;background:var(--surface)}
.tw{overflow-x:auto;border:1px solid var(--line);border-radius:10px;background:var(--surface)}
table{border-collapse:collapse;width:100%}
.wide{min-width:560px}
th,td{padding:9px 12px;text-align:left;border-bottom:1px solid var(--line);vertical-align:top}
tr:last-child td,tr:last-child th{border-bottom:0}
thead th{font-size:.74rem;text-transform:uppercase;letter-spacing:.06em;color:var(--muted);font-weight:700}
.art{font-family:var(--display);font-weight:700;font-size:1.1rem;color:var(--accent)}
.f .art,.ff{color:var(--fem)}
.g{font-size:.7rem;font-weight:700;letter-spacing:.05em;text-transform:uppercase;padding:2px 8px;border-radius:99px;background:var(--accent-soft);color:var(--accent);white-space:nowrap}
.f .g{background:var(--fem-soft);color:var(--fem)}
.ex{color:var(--muted);font-style:italic}
.pa td{font-family:var(--display);font-weight:700;color:var(--accent)}
.pa td.ff{color:var(--fem)}
.pa th[scope=row]{font-family:var(--display)}
.pa thead th small,.vt th small{display:block;text-transform:none;letter-spacing:0;font-weight:400;color:var(--muted)}
.vt td{white-space:nowrap;font-family:var(--display)}
.box{background:var(--surface);border:1px solid var(--line);border-radius:12px;padding:16px;display:grid;gap:10px}
.box ul,.box ol{margin:0;padding-left:1.2em;display:grid;gap:6px}
.trap{border-left:4px solid var(--hl);background:var(--hl-soft);border-radius:0 10px 10px 0;padding:14px 16px;display:grid;gap:6px}
.uses{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:12px}
.use{background:var(--surface);border:1px solid var(--line);border-radius:10px;padding:14px;display:grid;gap:6px;align-content:start;min-width:0}
.use p{font-size:.93rem}
.conj{display:flex;flex-wrap:wrap;gap:8px;align-items:center}
.conj select{font:inherit;padding:8px 10px;border-radius:8px;border:1px solid var(--line);background:var(--surface);color:var(--fg)}
</style>

<main>
  <header>
    <h1>Allenamento: verso il C1</h1>
    <p class="lead">Articoli, preposizioni, verbi e lessico. Esercizi veloci, a tempo e in contesto. Gli errori tornano finché non li impari.</p>
  </header>

  <div class="tabs" role="tablist">
    <button role="tab" id="tab-ex" aria-selected="true" aria-controls="p-ex">Esercizi</button>
    <button role="tab" id="tab-gr" aria-selected="false" aria-controls="p-gr">Grammatica</button>
  </div>

  <!-- ESERCIZI -->
  <div id="p-ex" role="tabpanel" aria-labelledby="tab-ex" style="display:grid;gap:22px">
    <div class="stats">
      <div class="stat"><b id="st-today">0</b><span>risposte giuste oggi</span></div>
      <div class="stat"><b id="st-streak">0</b><span>giorni di fila</span></div>
      <div class="stat"><b id="st-err">0</b><span>errori da ripassare</span></div>
      <div class="stat"><b id="st-best">0</b><span>record della raffica</span></div>
    </div>

    <div id="home" style="display:grid;gap:14px"></div>

    <section id="game" hidden style="display:grid;gap:14px">
      <div class="ghead"><button class="back" id="back">← Tutti gli esercizi</button><h2 id="gtitle"></h2></div>
      <p class="note" id="gdesc"></p>
      <div class="modes" id="gchips" role="group" aria-label="Opzioni"></div>
      <div class="card" id="gbody"></div>
    </section>
  </div>

  <!-- GRAMMATICA -->
  <div id="p-gr" role="tabpanel" aria-labelledby="tab-gr" hidden>
    <div class="gram">
      <nav class="toc">
        <a href="#g-art">Articoli</a><a href="#g-c1">Articoli C1</a><a href="#g-prep">Preposizioni articolate</a><a href="#g-sit">Quale preposizione?</a><a href="#g-vp">Verbi + preposizione</a><a href="#g-part">Partitivo</a><a href="#g-poss">Possessivi</a><a href="#g-conj">Coniugatore</a><a href="#g-tempi">Quale tempo?</a><a href="#g-cong">Congiuntivo</a><a href="#g-ipo">Periodo ipotetico</a>
      </nav>

      <section id="g-art">
        <h2>Articoli determinativi e indeterminativi</h2>
        <div class="tw"><table class="wide">
          <thead><tr><th>Genere</th><th>La parola comincia con</th><th>Det. sing.</th><th>Det. plur.</th><th>Indet.</th><th>Esempi</th></tr></thead>
          <tbody>
            <tr><td><span class="g">masc.</span></td><td>consonante</td><td class="art">il</td><td class="art">i</td><td class="art">un</td><td class="ex">il libro, i libri, un libro</td></tr>
            <tr><td><span class="g">masc.</span></td><td>s + consonante, z, gn, ps, pn, x, y, i + vocale</td><td class="art">lo</td><td class="art">gli</td><td class="art">uno</td><td class="ex">lo studente, gli zaini, uno yogurt</td></tr>
            <tr><td><span class="g">masc.</span></td><td>vocale (anche h muta)</td><td class="art">l'</td><td class="art">gli</td><td class="art">un</td><td class="ex">l'amico, gli hotel, un amico</td></tr>
            <tr class="f"><td><span class="g">femm.</span></td><td>consonante</td><td class="art">la</td><td class="art">le</td><td class="art">una</td><td class="ex">la casa, le case, una casa</td></tr>
            <tr class="f"><td><span class="g">femm.</span></td><td>vocale</td><td class="art">l'</td><td class="art">le</td><td class="art">un'</td><td class="ex">l'amica, le amiche, un'amica</td></tr>
          </tbody>
        </table></div>
        <div class="trap">
          <h3>Tre regole che si dimenticano</h3>
          <p><strong>L'articolo guarda la parola che viene subito dopo</strong>, non il nome: <em>lo zaino</em> ma <em>il nuovo zaino</em>; <em>un'amica</em> ma <em>una cara amica</em>; <em>lo scorso anno</em>.</p>
          <p><strong>Un amico</strong> (maschile) è senza apostrofo; <strong>un'amica</strong> (femminile) ha l'apostrofo.</p>
          <p>Al plurale femminile non si apostrofa più: <em>le amiche</em>, <em>le uova</em>.</p>
        </div>
        <h3>Nomi difficili</h3>
        <div class="tw"><table class="wide">
          <thead><tr><th>Caso</th><th>Esempi</th></tr></thead>
          <tbody>
            <tr><td>Maschili in <strong>-a</strong> (dal greco)</td><td class="ex">il problema, il tema, il sistema, il programma, il clima, il pianeta, il cinema, il pigiama</td></tr>
            <tr><td>Femminili in <strong>-o</strong></td><td class="ex">la mano (le mani), la radio, la foto, la moto, l'auto</td></tr>
            <tr><td>Plurale femminile in <strong>-a</strong></td><td class="ex">l'uovo → le uova, il braccio → le braccia, il dito → le dita, il labbro → le labbra</td></tr>
            <tr><td>Invariabili</td><td class="ex">la città → le città, il film → i film, la crisi → le crisi, l'analisi → le analisi, la serie → le serie</td></tr>
            <tr><td>Parole straniere</td><td class="ex">il weekend, il whisky, il jazz, l'hotel, lo yogurt, lo yacht, lo shampoo</td></tr>
            <tr><td>Eccezioni</td><td class="ex">gli dei, l'uomo → gli uomini, il bue → i buoi</td></tr>
          </tbody>
        </table></div>
      </section>

      <section id="g-c1">
        <h2>Articoli C1: quando sì e quando no</h2>
        <div class="tw"><table class="wide">
          <thead><tr><th>Caso</th><th>Con articolo</th><th>Senza articolo</th></tr></thead>
          <tbody>
            <tr><td>Giorni</td><td class="ex"><strong>il</strong> lunedì vado in palestra (= ogni lunedì)</td><td class="ex">lunedì vado dal medico (= questo lunedì)</td></tr>
            <tr><td>Date e anni</td><td class="ex"><strong>il</strong> 19 ottobre; <strong>nel</strong> 2025; <strong>negli</strong> anni Novanta</td><td class="ex">—</td></tr>
            <tr><td>Ore</td><td class="ex">sono <strong>le</strong> tre; è <strong>l'</strong>una; <strong>alle</strong> otto</td><td class="ex">a mezzogiorno, a mezzanotte</td></tr>
            <tr><td>Percentuali</td><td class="ex"><strong>il</strong> 20% degli italiani; aumentare <strong>del</strong> 5%</td><td class="ex">—</td></tr>
            <tr><td>Titoli</td><td class="ex"><strong>la</strong> signora Rossi è arrivata; <strong>il</strong> dottor Bianchi</td><td class="ex">Buongiorno, signora Rossi! (quando parli con lei)</td></tr>
            <tr><td>Corpo</td><td class="ex">mi lavo <strong>le</strong> mani; mi fa male <strong>la</strong> testa</td><td class="ex">(non “le mie mani”)</td></tr>
            <tr><td>Paesi e regioni</td><td class="ex"><strong>l'</strong>Italia è bella; <strong>nell'</strong>Italia del Nord; <strong>negli</strong> Stati Uniti; vengo <strong>dal</strong> Brasile</td><td class="ex">vivo in Italia; vado in Sicilia</td></tr>
            <tr><td>Lingue</td><td class="ex"><strong>l'</strong>italiano è difficile</td><td class="ex">parlo italiano; un corso di italiano</td></tr>
            <tr><td>Sport e strumenti</td><td class="ex">suono <strong>il</strong> pianoforte</td><td class="ex">gioco a calcio, a tennis</td></tr>
            <tr><td>Espressioni fisse</td><td class="ex">—</td><td class="ex">avere fame, fare colazione, andare a letto, in treno, a casa, a piedi</td></tr>
            <tr><td>Negazione</td><td class="ex">—</td><td class="ex">non ho tempo, non ci sono problemi</td></tr>
            <tr><td>Tutto</td><td class="ex">tutto <strong>il</strong> giorno, tutti <strong>i</strong> giorni, tutte <strong>le</strong> volte</td><td class="ex">—</td></tr>
            <tr><td>Cognomi</td><td class="ex">stasera vengono <strong>i</strong> Rossi (la famiglia)</td><td class="ex">Mario Rossi</td></tr>
          </tbody>
        </table></div>
      </section>

      <section id="g-prep">
        <h2>Preposizioni articolate</h2>
        <div class="box">
          <p><strong>Metodo:</strong> 1) trova l'articolo della parola; 2) <strong>di → de</strong>, <strong>in → ne</strong> (a, da, su non cambiano); 3) unisci. Con lo/la/l'/le la L raddoppia (de + lo = <strong>dello</strong>); con il resta una L sola (de + il = <strong>del</strong>).</p>
        </div>
        <div class="tw"><table class="pa wide">
          <thead><tr><th></th><th>il</th><th>lo</th><th>l'</th><th>la</th><th>i</th><th>gli</th><th>le</th></tr></thead>
          <tbody>
            <tr><th scope="row">di</th><td>del</td><td>dello</td><td>dell'</td><td class="ff">della</td><td>dei</td><td>degli</td><td class="ff">delle</td></tr>
            <tr><th scope="row">a</th><td>al</td><td>allo</td><td>all'</td><td class="ff">alla</td><td>ai</td><td>agli</td><td class="ff">alle</td></tr>
            <tr><th scope="row">da</th><td>dal</td><td>dallo</td><td>dall'</td><td class="ff">dalla</td><td>dai</td><td>dagli</td><td class="ff">dalle</td></tr>
            <tr><th scope="row">in</th><td>nel</td><td>nello</td><td>nell'</td><td class="ff">nella</td><td>nei</td><td>negli</td><td class="ff">nelle</td></tr>
            <tr><th scope="row">su</th><td>sul</td><td>sullo</td><td>sull'</td><td class="ff">sulla</td><td>sui</td><td>sugli</td><td class="ff">sulle</td></tr>
          </tbody>
        </table></div>
        <div class="uses">
          <div class="use"><h3>di</h3><p>Possesso e specificazione: <em>il libro dello studente</em>. Partitivo: <em>dei libri</em>.</p></div>
          <div class="use"><h3>a</h3><p>Dove vai/sei: <em>al cinema, al mare</em>. A chi: <em>agli amici</em>. Ore: <em>alle otto</em>. Città: <em>a Ivrea</em>.</p></div>
          <div class="use"><h3>da</h3><p>Provenienza: <em>dall'ufficio</em>. Da una persona: <em>dal medico</em>. Tempo: <em>vivo qui da due anni</em>.</p></div>
          <div class="use"><h3>in</h3><p>Dentro qualcosa di preciso: <em>nella borsa rossa</em>. Paesi: <em>in Italia</em>. Mezzi: <em>in treno</em>.</p></div>
          <div class="use"><h3>su</h3><p>Sopra: <em>sul divano</em>. Argomento: <em>un articolo sull'economia</em>.</p></div>
        </div>
        <div class="trap">
          <h3>Senza articolo</h3>
          <p>Città → <strong>a</strong> (a Torino). Paesi e regioni → <strong>in</strong> (in Piemonte). Luoghi e stanze in senso generale → <strong>in</strong>: in giardino, in cucina, in banca, in ufficio, in centro, in stazione, in farmacia. Fissi con <strong>a</strong>: a casa, a scuola, a letto, a teatro.</p>
          <p><strong>Se il luogo è specificato torna l'articolo:</strong> in giardino → <em>nel giardino della nonna</em>.</p>
        </div>
      </section>

      <section id="g-sit">
        <h2>Quale preposizione? Fatti una domanda</h2>
        <p>La preposizione dipende dalla <strong>domanda</strong> a cui risponde la frase. Prima chiediti: dove? quando? come? di chi? per chi?</p>
        <div class="uses">
          <div class="use"><h3>Dove vai / dove sei?</h3><p><strong>Città</strong> → a (a Torino). <strong>Paese, regione</strong> → in (in Italia). <strong>Persona</strong> → da (dal medico, da Marco). <strong>Luoghi fissi</strong>: a casa, a scuola, a teatro · al cinema, al mare, al bar, al lavoro · in ufficio, in banca, in centro, in palestra.</p></div>
          <div class="use"><h3>Da dove vieni / esci?</h3><p>Sempre <strong>da</strong>, e l'articolo torna con i paesi: da Torino, <strong>dall'</strong>Italia, <strong>dal</strong> Brasile, <strong>dall'</strong>ufficio, da casa. Origine con essere: sono <strong>di</strong> San Paolo.</p></div>
          <div class="use"><h3>Quando?</h3><p>Ora → <strong>alle</strong> tre. Data → <strong>il</strong> 5 maggio. Anno → <strong>nel</strong> 2025. Da un momento a un altro → <strong>dalle</strong> 9 <strong>alle</strong> 18.</p></div>
          <div class="use"><h3>Per quanto tempo?</h3><p>Ancora in corso → <strong>da</strong> (vivo qui da due anni). Finito → <strong>per</strong> (ho vissuto lì per due anni). Nel futuro → <strong>tra/fra</strong> (tra un'ora). Nel passato → <strong>fa</strong>, dopo (due anni fa). Scadenza → <strong>entro</strong> (entro venerdì).</p></div>
          <div class="use"><h3>Come? Con che mezzo?</h3><p><strong>in</strong> + mezzo senza articolo: in treno, in macchina, in aereo, in bici. Ma <strong>a</strong> piedi, <strong>a</strong> cavallo. Pagare <strong>in</strong> contanti, <strong>con</strong> la carta.</p></div>
          <div class="use"><h3>Di chi? Di che cosa?</h3><p><strong>di</strong>: possesso (la casa di Marco), materiale (un tavolo di legno), argomento (un libro di storia), età (una bambina di 5 anni), quantità (un bicchiere di vino).</p></div>
          <div class="use"><h3>Per chi? Per che cosa?</h3><p><strong>per</strong>: destinatario (è per te), motivo (grazie per l'aiuto), destinazione di partire (parto per Roma), passaggio (passo per Milano).</p></div>
          <div class="use"><h3>A cosa serve? Come chi?</h3><p><strong>da</strong>: scopo (macchina da scrivere, occhiali da sole), qualcosa da fare (ho molto da fare), età passata (da bambina), come (si comporta da amico).</p></div>
          <div class="use"><h3>Sopra cosa? Circa?</h3><p><strong>su</strong>: sopra (sul tavolo), media (sul giornale, su internet), argomento (un film su Leonardo), approssimazione (avrà sui 50 anni), proporzione (tre su dieci).</p></div>
        </div>
        <h3>Mappa dei luoghi</h3>
        <p class="note">Tocca un luogo: vedi come si dice andare, stare e tornare.</p>
        <div class="modes" id="plc" role="group" aria-label="Luoghi"></div>
        <div class="box" id="plout" aria-live="polite"></div>
      </section>

      <section id="g-vp">
        <h2>Verbi e aggettivi che vogliono una preposizione</h2>
        <p>Qui non c'è logica: si imparano a memoria, come il verbo. Studiali in coppia (cominciare <strong>a</strong>, smettere <strong>di</strong>).</p>
        <div class="tw"><table class="wide">
          <thead><tr><th>Preposizione</th><th>Verbi + infinito</th><th>Verbi + nome</th></tr></thead>
          <tbody>
            <tr><td class="art">a</td><td class="ex">cominciare a, continuare a, riuscire a, provare a, imparare a, aiutare a, andare a, venire a, abituarsi a, prepararsi a</td><td class="ex">pensare a, partecipare a, credere a (una storia), rinunciare a, assistere a, telefonare a</td></tr>
            <tr><td class="art">di</td><td class="ex">decidere di, smettere di, finire di, cercare di, sperare di, dimenticarsi di, ricordarsi di, avere paura di, avere bisogno di, accettare di, pensare di (= avere intenzione)</td><td class="ex">parlare di, occuparsi di, fidarsi di, innamorarsi di, accorgersi di, avere bisogno di, ridere di</td></tr>
            <tr><td class="art">da</td><td class="ex">—</td><td class="ex">dipendere da, imparare da, guarire da, difendersi da</td></tr>
            <tr><td class="art">in</td><td class="ex">—</td><td class="ex">credere in (avere fiducia), sperare in, consistere in, laurearsi in</td></tr>
            <tr><td class="art">su</td><td class="ex">—</td><td class="ex">contare su, riflettere su, puntare su, investire su</td></tr>
            <tr><td class="art">per</td><td class="ex">—</td><td class="ex">ringraziare per, scusarsi per, lavorare per, partire per, preoccuparsi per</td></tr>
          </tbody>
        </table></div>
        <div class="tw"><table class="wide">
          <thead><tr><th>Aggettivo</th><th>Esempi</th></tr></thead>
          <tbody>
            <tr><td>contento <strong>di</strong>, capace <strong>di</strong>, sicuro <strong>di</strong>, stanco <strong>di</strong></td><td class="ex">Sono contenta di vederti. Sono stanca di aspettare.</td></tr>
            <tr><td>pronto <strong>a</strong>, abituato <strong>a</strong>, disposto <strong>a</strong>, attento <strong>a</strong></td><td class="ex">Sono pronta a partire. Sono disposta a trasferirmi.</td></tr>
            <tr><td>facile / difficile <strong>da</strong> + infinito (riferito a una cosa)</td><td class="ex">Questo esercizio è facile da capire.</td></tr>
            <tr><td>È facile / difficile + infinito (senza preposizione)</td><td class="ex">È difficile trovare casa a Milano.</td></tr>
          </tbody>
        </table></div>
        <div class="trap">
          <h3>Pensare: tre significati</h3>
          <p><strong>Penso a te</strong> = estou pensando em você. <strong>Che cosa pensi di questo progetto?</strong> = o que você acha. <strong>Penso di partire</strong> = estou pensando em viajar (intenção).</p>
        </div>
      </section>

      <section id="g-part">
        <h2>Partitivo: dei, degli, delle</h2>
        <p><strong>Degli</strong> non vuol dire sempre “dos”: spesso è il plurale di un/uno/una (= alcuni). Al singolare, con cose che non si contano, vuol dire “un po' di”.</p>
        <div class="tw"><table class="wide">
          <thead><tr><th>Singolare</th><th>Plurale</th><th>Massa (un po' di)</th></tr></thead>
          <tbody>
            <tr><td class="ex">un libro</td><td class="ex">dei libri</td><td class="ex">del pane</td></tr>
            <tr><td class="ex">uno studente / un amico</td><td class="ex">degli studenti / degli amici</td><td class="ex">dello zucchero / dell'olio</td></tr>
            <tr class="f"><td class="ex">una mela / un'amica</td><td class="ex">delle mele / delle amiche</td><td class="ex">della pasta / dell'acqua</td></tr>
          </tbody>
        </table></div>
        <p class="note">Prova: se puoi tradurre con “alguns/umas”, è partitivo. Con la negazione sparisce: <em>non ho pane</em>.</p>
      </section>

      <section id="g-poss">
        <h2>Possessivi</h2>
        <div class="tw"><table class="wide">
          <thead><tr><th>Caso</th><th>Articolo?</th><th>Esempi</th></tr></thead>
          <tbody>
            <tr><td>Cose, luoghi, amici</td><td class="art">sì</td><td class="ex">la mia casa, il mio lavoro</td></tr>
            <tr><td>Parente al singolare</td><td class="art">no</td><td class="ex">mia madre, mio marito, mio figlio</td></tr>
            <tr><td>Parente al plurale</td><td class="art">sì</td><td class="ex">i miei figli</td></tr>
            <tr><td>Con “loro”</td><td class="art">sì</td><td class="ex">il loro figlio</td></tr>
            <tr><td>Affettivo, diminutivo o con aggettivo</td><td class="art">sì</td><td class="ex">la mia mamma, la mia sorellina, il mio figlio maggiore</td></tr>
          </tbody>
        </table></div>
      </section>

      <section id="g-conj">
        <h2>Coniugatore</h2>
        <p>Scegli un verbo e guarda tutti i tempi. Gli stessi verbi compaiono nell'esercizio “Coniuga”.</p>
        <div class="conj"><label for="conjSel">Verbo</label><select id="conjSel"></select></div>
        <div class="tw"><table class="vt" id="conjTable" style="min-width:900px"></table></div>
      </section>

      <section id="g-tempi">
        <h2>Quale tempo del passato?</h2>
        <div class="uses">
          <div class="use"><h3>Passato prossimo</h3><p>Azione finita, con un inizio e una fine: <em>Ieri <strong>sono stata</strong> tre ore in riunione.</em> Ausiliare <strong>essere</strong> con movimento, cambiamento, riflessivi (il participio concorda: <em>sono andata</em>); <strong>avere</strong> con gli altri.</p></div>
          <div class="use"><h3>Imperfetto</h3><p>Abitudini, descrizioni, azioni in corso: <em>Da bambina <strong>andavo</strong> al mare. <strong>Cucinavo</strong> quando è suonato il telefono.</em></p></div>
          <div class="use"><h3>Trapassato prossimo</h3><p>Prima di un'altra azione passata: <em>Quando sono arrivata, il treno <strong>era</strong> già <strong>partito</strong>.</em></p></div>
          <div class="use"><h3>Passato remoto</h3><p>Fatti storici e letteratura (va riconosciuto): <em>Dante <strong>scrisse</strong>, Garibaldi <strong>nacque</strong>, <strong>fu</strong>, <strong>ebbe</strong>.</em></p></div>
          <div class="use"><h3>Futuro anteriore</h3><p>Prima di un'azione futura, o probabilità: <em>Appena <strong>avrò finito</strong>, ti chiamo. Non risponde: <strong>sarà uscita</strong>.</em></p></div>
          <div class="use"><h3>Futuro nel passato</h3><p>Condizionale composto: <em>Mi ha detto che <strong>sarebbe venuto</strong>.</em></p></div>
        </div>
      </section>

      <section id="g-cong">
        <h2>Quando si usa il congiuntivo</h2>
        <div class="box">
          <ul>
            <li><strong>Opinione e dubbio:</strong> penso, credo, mi sembra, non sono sicura che… <em>Penso che sia giusto.</em></li>
            <li><strong>Volontà e desiderio:</strong> voglio, spero, preferisco che… <em>Spero che tu venga.</em></li>
            <li><strong>Emozione:</strong> sono contenta, ho paura che…</li>
            <li><strong>Espressioni impersonali:</strong> è importante, è necessario, bisogna, è possibile che…</li>
            <li><strong>Congiunzioni:</strong> benché, sebbene, nonostante, affinché, perché (= affinché), purché, a meno che, prima che, senza che.</li>
            <li><strong>Relativa con requisito:</strong> <em>cerco una casa che abbia un giardino.</em></li>
            <li><strong>Superlativo relativo:</strong> <em>il film più bello che io abbia mai visto.</em></li>
            <li><strong>Si dice che, pare che, magari, come se.</strong></li>
          </ul>
          <p class="note">Con verbi di certezza (so, sono sicura, è chiaro che) si usa l'indicativo.</p>
        </div>
        <h3>Concordanza dei tempi</h3>
        <div class="tw"><table class="wide">
          <thead><tr><th>Principale</th><th>Azione contemporanea</th><th>Azione anteriore</th></tr></thead>
          <tbody>
            <tr><td>Presente: <em>Penso che…</em></td><td class="ex">tu abbia ragione (cong. presente)</td><td class="ex">tu abbia avuto ragione (cong. passato)</td></tr>
            <tr><td>Passato: <em>Pensavo che…</em></td><td class="ex">tu avessi ragione (cong. imperfetto)</td><td class="ex">tu avessi avuto ragione (cong. trapassato)</td></tr>
            <tr><td>Condizionale: <em>Vorrei che…</em></td><td class="ex">tu venissi (cong. imperfetto)</td><td class="ex">tu fossi venuto (cong. trapassato)</td></tr>
          </tbody>
        </table></div>
      </section>

      <section id="g-ipo">
        <h2>Periodo ipotetico</h2>
        <div class="tw"><table class="wide">
          <thead><tr><th>Tipo</th><th>Se…</th><th>allora…</th><th>Esempio</th></tr></thead>
          <tbody>
            <tr><td>Realtà</td><td>presente / futuro</td><td>presente / futuro / imperativo</td><td class="ex">Se piove, resto a casa.</td></tr>
            <tr><td>Possibilità</td><td>congiuntivo imperfetto</td><td>condizionale presente</td><td class="ex">Se avessi tempo, studierei di più.</td></tr>
            <tr><td>Irrealtà (passato)</td><td>congiuntivo trapassato</td><td>condizionale passato</td><td class="ex">Se avessi studiato, avrei superato l'esame.</td></tr>
          </tbody>
        </table></div>
        <p class="note">Mai il condizionale dopo “se”: <em>se avrei</em> è sbagliato, si dice <em>se avessi</em>.</p>
      </section>
    </div>
  </div>
</main>

<script>
/* ================= UTILITÀ ================= */
const $=id=>document.getElementById(id);
const rnd=a=>a[Math.floor(Math.random()*a.length)];
const shuffle=a=>{a=a.slice();for(let i=a.length-1;i>0;i--){const j=Math.floor(Math.random()*(i+1));[a[i],a[j]]=[a[j],a[i]];}return a;};
const cap=s=>s?s.charAt(0).toUpperCase()+s.slice(1):s;
const esc=s=>String(s).replace(/[&<>"]/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;"}[c]));
const norm=s=>s.toLowerCase().replace(/[’`´]/g,"'").replace(/\s+/g," ").trim();
const loose=s=>norm(s).normalize("NFD").replace(/[̀-ͯ]/g,"").replace(/'/g,"");

/* ================= STATO (solo in questo browser) ================= */
const KEY="allenamento-c1";
let S={best:0,errs:[],streak:0,last:"",today:"",n:0};
try{const raw=localStorage.getItem(KEY);if(raw)S=Object.assign(S,JSON.parse(raw));}catch(e){}
const save=()=>{try{localStorage.setItem(KEY,JSON.stringify(S));}catch(e){}};
const dayStr=d=>d.toISOString().slice(0,10);
function tick(good){
  const t=dayStr(new Date());
  if(S.today!==t){S.today=t;S.n=0;}
  if(good){S.n++;
    if(S.last!==t){const y=new Date();y.setDate(y.getDate()-1);S.streak=(S.last===dayStr(y))?S.streak+1:1;S.last=t;}
  }
  save();renderStats();
}
function renderStats(){
  const t=dayStr(new Date());
  $("st-today").textContent=S.today===t?S.n:0;
  const y=new Date();y.setDate(y.getDate()-1);
  $("st-streak").textContent=(S.last===t||S.last===dayStr(y))?S.streak:0;
  $("st-err").textContent=S.errs.length;$("st-best").textContent=S.best;
}
function addErr(q){if(!q.key)return;S.errs=S.errs.filter(e=>e.key!==q.key);S.errs.push(q);if(S.errs.length>250)S.errs.shift();save();renderStats();}
function delErr(q){const n=S.errs.length;S.errs=S.errs.filter(e=>e.key!==q.key);if(n!==S.errs.length){save();renderStats();}}

/* ================= NOMI ================= */
// [parola, genere, numero, inizio (c consonante, v vocale, s = s+cons/z/gn/ps/pn/x/y), traduzione, nota, articolo speciale]
const N=[
["libro","m","s","c","livro"],["libri","m","p","c","livros"],["tavolo","m","s","c","mesa"],["ragazzo","m","s","c","menino"],["cane","m","s","c","cachorro"],["giorni","m","p","c","dias"],["treno","m","s","c","trem"],["cassetto","m","s","c","gaveta"],["bambini","m","p","c","crianças"],["divano","m","s","c","sofá"],["mercato","m","s","c","mercado"],["fratelli","m","p","c","irmãos"],["contratto","m","s","c","contrato"],["colloquio","m","s","c","entrevista"],
["studente","m","s","s","estudante"],["studenti","m","p","s","estudantes"],["zaino","m","s","s","mochila"],["zaini","m","p","s","mochilas"],["zio","m","s","s","tio"],["zii","m","p","s","tios"],["specchio","m","s","s","espelho"],["sport","m","s","s","esporte","Invariabile: lo sport, gli sport."],["gnomo","m","s","s","gnomo"],["psicologo","m","s","s","psicólogo"],["psicologi","m","p","s","psicólogos"],["yogurt","m","s","s","iogurte","y → lo yogurt."],["zucchero","m","s","s","açúcar"],["spaghetti","m","p","s","espaguete"],["scontrino","m","s","s","cupom fiscal"],["stadio","m","s","s","estádio"],["sconto","m","s","s","desconto"],["stipendio","m","s","s","salário"],["straordinari","m","p","s","horas extras"],["sciopero","m","s","s","greve","sc + vocale conta come s + consonante: lo sciopero."],["gnocchi","m","p","s","nhoque"],["xilofono","m","s","s","xilofone"],["iodio","m","s","s","iodo","i + vocale (semiconsonante) → lo iodio."],["pneumatico","m","s","s","pneu","pn → lo pneumatico (nell'uso si sente anche il)."],["yacht","m","s","s","iate"],
["amico","m","s","v","amigo"],["amici","m","p","v","amigos"],["albero","m","s","v","árvore"],["ufficio","m","s","v","escritório"],["orologio","m","s","v","relógio"],["occhi","m","p","v","olhos"],["esame","m","s","v","exame"],["aeroporto","m","s","v","aeroporto"],["armadio","m","s","v","armário"],["autobus","m","s","v","ônibus"],["uffici","m","p","v","escritórios"],["hotel","m","s","v","hotel","h muta = vocale: l'hotel, gli hotel."],["euro","m","p","v","euros","Invariabile: l'euro, gli euro."],["uomini","m","p","v","homens","Plurale irregolare di l'uomo."],["uovo","m","s","v","ovo","Al plurale diventa femminile: le uova."],["obiettivo","m","s","v","objetivo"],
["casa","f","s","c","casa"],["case","f","p","c","casas"],["mela","f","s","c","maçã"],["mele","f","p","c","maçãs"],["scuola","f","s","c","escola","Femminile: la, anche con s + consonante."],["zia","f","s","c","tia"],["strada","f","s","c","rua"],["finestre","f","p","c","janelas"],["sedia","f","s","c","cadeira"],["borsa","f","s","c","bolsa"],["stazione","f","s","c","estação"],["spesa","f","s","c","compras"],["scadenza","f","s","c","prazo"],["riunione","f","s","c","reunião"],["zucchine","f","p","c","abobrinhas"],
["mano","f","s","c","mão","Femminile anche se finisce in -o. Plurale: le mani."],["mani","f","p","c","mãos"],["radio","f","s","c","rádio","Femminile (la radiofonia)."],["foto","f","s","c","foto","Femminile (la fotografia): la foto, le foto."],["moto","f","s","c","moto","Femminile (la motocicletta)."],["braccia","f","p","c","braços","Il braccio → le braccia."],["dita","f","p","c","dedos","Il dito → le dita."],["labbra","f","p","c","lábios","Il labbro → le labbra."],["crisi","f","s","c","crise","Femminile in -i, invariabile."],["città","f","p","c","cidades","Le parole accentate sono invariabili: le città."],["serie","f","s","c","série","Femminile, invariabile."],["specie","f","s","c","espécie","Femminile, invariabile."],
["amica","f","s","v","amiga"],["acqua","f","s","v","água"],["isola","f","s","v","ilha"],["ora","f","s","v","hora"],["università","f","s","v","universidade"],["amiche","f","p","v","amigas"],["estate","f","s","v","verão"],["aula","f","s","v","sala de aula"],["azienda","f","s","v","empresa"],["idea","f","s","v","ideia"],["auto","f","s","v","carro","Femminile (l'automobile): l'auto, le auto."],["uova","f","p","v","ovos","Plurale femminile di l'uovo."],["analisi","f","s","v","análise","Femminile in -i: l'analisi, le analisi."],["ipotesi","f","s","v","hipótese","Femminile in -i."],["ali","f","p","v","asas","L'ala → le ali."],["offerta","f","s","v","oferta"],
["problema","m","s","c","problema","Maschile anche se finisce in -a (dal greco)."],["tema","m","s","c","tema/redação","Maschile in -a."],["sistema","m","s","c","sistema","Maschile in -a."],["programmi","m","p","c","programas","Il programma (maschile in -a) → i programmi."],["clima","m","s","c","clima","Maschile in -a."],["pianeta","m","s","c","planeta","Maschile in -a."],["cinema","m","s","c","cinema","Maschile in -a, invariabile."],["pigiama","m","s","c","pijama","Maschile in -a."],["dei","m","p","c","deuses","Eccezione: gli dei.","gli"],["whisky","m","s","c","uísque","w si comporta come consonante: il whisky."],["weekend","m","s","c","fim de semana","Parola straniera: il weekend."],["jazz","m","s","c","jazz","j si legge come consonante: il jazz."],["bar","m","s","c","bar","Invariabile: il bar, i bar."],["film","m","p","c","filmes","Invariabile: il film → i film."],["computer","m","s","c","computador"],["sale","m","s","c","sal","s + vocale non è 's impura': il sale."]
];
const ARTS=["il","lo","l'","la","i","gli","le"],IND=["un","uno","una","un'"];
function det(w){if(w[6])return w[6];const[,g,n,t]=w;if(g==="f")return n==="p"?"le":(t==="v"?"l'":"la");if(n==="p")return t==="c"?"i":"gli";return t==="c"?"il":t==="s"?"lo":"l'";}
function ind(w){const[,g,,t]=w;if(g==="f")return t==="v"?"un'":"una";return t==="s"?"uno":"un";}
const withWord=(a,w)=>a==="∅"?w:(a.endsWith("'")?a+w:a+" "+w);
function why(w){if(w[5])return w[5];const[,g,n,t]=w;const ini=t==="c"?"comincia con consonante":t==="v"?"comincia con vocale":"comincia con s + consonante, z, gn, ps o y";
  return `${g==="m"?"Maschile":"Femminile"} ${n==="s"?"singolare":"plurale"}, ${ini}.`;}
const PREP={di:"de",a:"a",da:"da",in:"ne",su:"su"};
const JOIN={"il":"l","lo":"llo","l'":"ll'","la":"lla","i":"i","gli":"gli","le":"lle"};
const fuse=(p,a)=>PREP[p]+JOIN[a];
const formsOf=p=>[p,...ARTS.map(a=>fuse(p,a))];

/* ================= FRASI: ARTICOLI E PREPOSIZIONI ================= */
// [frase con ___, opzioni, risposta, spiegazione]
const AC=[
["___ lunedì vado in palestra.",["Il","Lo","∅"],"Il","Il lunedì = tutti i lunedì (abitudine). Senza articolo, lunedì = questo lunedì."],
["Ci vediamo ___ lunedì prossimo.",["il","∅","al"],"∅","Un giorno preciso (lunedì prossimo) → senza articolo."],
["Oggi è ___ 19 ottobre.",["il","lo","∅"],"il","Le date vogliono l'articolo: il 19 ottobre, l'8 marzo."],
["Sono nata ___ 1980.",["nel","in","al"],"nel","Anni: in + articolo → nel 1980."],
["Sono ___ tre e mezza.",["le","∅","alle"],"le","Ore: sono le tre (le ore tre)."],
["È ___ una e un quarto.",["l'","la","∅"],"l'","L'una è singolare: è l'una."],
["Pranziamo ___ mezzogiorno.",["a","al","alle"],"a","Mezzogiorno e mezzanotte sono senza articolo."],
["___ signora Rossi è arrivata.",["La","∅","Una"],"La","Titolo + cognome quando parli DI una persona → articolo."],
["Buongiorno, ___ signora Rossi!",["la","∅","una"],"∅","Quando parli CON la persona → niente articolo."],
["Mi lavo ___ mani prima di mangiare.",["le","le mie","∅"],"le","Parti del corpo con verbo riflessivo: articolo, non possessivo."],
["Mi fa male ___ testa.",["la","mia","∅"],"la","Parti del corpo: la testa, non “la mia testa”."],
["___ inflazione è salita al 3%.",["L'","La","Lo"],"L'","Inflazione: femminile con vocale → l'inflazione."],
["Il prezzo è aumentato ___ 20%.",["del","di","dal"],"del","Le percentuali vogliono l'articolo: il 20% → del 20%."],
["___ Sicilia è la regione più grande d'Italia.",["La","∅","In"],"La","Regione come soggetto → articolo."],
["Ho vissuto due anni ___ Stati Uniti.",["negli","in","agli"],"negli","Paesi al plurale → in + articolo: negli Stati Uniti."],
["Mio cugino abita ___ Marche.",["nelle","in","alle"],"nelle","Regione al plurale → nelle Marche."],
["Vivo ___ Italia del Nord.",["nell'","in","all'"],"nell'","Paese con specificazione → torna l'articolo."],
["Mio marito viene ___ Brasile.",["dal","da","di"],"dal","Venire da + paese: l'articolo resta (dal Brasile)."],
["Torno ___ Svizzera domani.",["in","nella","alla"],"in","Andare/tornare in + paese, senza articolo."],
["Non ho ___ tempo per uscire.",["∅","del","il"],"∅","Con la negazione niente partitivo: non ho tempo."],
["Ho lavorato tutto ___ giorno.",["il","∅","un"],"il","Tutto + articolo + nome: tutto il giorno."],
["Stasera vengono a cena ___ Rossi.",["i","∅","gli"],"i","Cognome al plurale (la famiglia) → i Rossi."],
["___ uova sono in frigorifero.",["Le","Gli","I"],"Le","L'uovo → le uova (plurale femminile)."],
["Mio figlio ha ___ braccia lunghe.",["le","i","gli"],"le","Il braccio → le braccia."],
["___ problema è che non abbiamo dati.",["Il","La","Lo"],"Il","Problema è maschile anche se finisce in -a."],
["Abbiamo ___ problema con il server.",["un","una","uno"],"un","Problema è maschile → un problema."],
["___ dei dell'Olimpo erano dodici.",["Gli","I","Le"],"Gli","Eccezione storica: gli dei."],
["___ italiano non è una lingua facile.",["L'","Il","Lo"],"L'","Lingua come soggetto → articolo."],
["Ho ___ fame, mangiamo?",["∅","la","una"],"∅","Avere fame/sete/sonno: senza articolo."],
["Faccio ___ colazione alle sette.",["∅","la","una"],"∅","Fare colazione: espressione fissa."],
["Gioco ___ tennis il sabato.",["a","al","il"],"a","Giocare a + sport, senza articolo."],
["Mio figlio suona ___ pianoforte.",["il","∅","al"],"il","Suonare + strumento, con articolo."],
["___ mio figlio maggiore studia a Torino.",["Il","∅","Lo"],"Il","Parente con aggettivo (maggiore) → articolo."],
["___ mia sorellina ha dieci anni.",["La","∅","Una"],"La","Parente al diminutivo → articolo."],
["Prendo ___ autobus delle otto.",["l'","∅","un"],"l'","Autobus preciso (quello delle otto) → l'autobus."],
["Vado al lavoro ___ autobus.",["in","nell'","all'"],"in","Mezzo di trasporto → in, senza articolo."],
["È ___ studente molto in gamba.",["uno","un","una"],"uno","s + consonante → uno studente."],
["Ho comprato ___ yogurt greco.",["uno","un","lo"],"uno","y → uno yogurt."],
["Mi piace ___ jazz.",["il","lo","l'"],"il","j di jazz è consonante → il jazz."],
["Abbiamo prenotato ___ hotel in centro.",["un","uno","un'"],"un","h muta, maschile → un hotel."],
["___ scorso anno ho cambiato lavoro.",["Lo","Il","L'"],"Lo","L'articolo guarda la parola dopo: scorso (s + consonante) → lo."],
["Ho mangiato ___ ottima pizza.",["un'","un","una"],"un'","La parola dopo è ottima (femminile con vocale) → un'ottima."],
["Ho visto ___ bellissimo film.",["un","uno","il"],"un","bellissimo comincia con consonante → un."],
["Lavoro con ___ psicologa della scuola.",["la","lo","l'"],"la","Femminile: sempre la, anche con ps."],
["Domani c'è ___ sciopero dei treni.",["uno","un","lo"],"uno","sc + vocale → uno sciopero."],
["Ho portato ___ foto delle vacanze.",["le","i","gli"],"le","La foto → le foto (femminile, invariabile)."],
["Ci sono ancora ___ crisi da risolvere.",["delle","dei","degli"],"delle","La crisi → le crisi → delle crisi (femminile)."]
];
const FB=[
["Il gatto dorme","divano.","sul","su","su + il divano = sul."],
["Le chiavi sono","borsa rossa.","nella","in","Borsa precisa (quella rossa) → nella."],
["Domani vado","medico.","dal","da","Andare da una persona → da: dal medico."],
["Il libro","studente è nuovo.","dello","di","di + lo studente = dello."],
["Telefono","amici stasera.","agli","a","a + gli amici = agli."],
["Torno","ufficio alle sei.","dall'","da","da + l'ufficio = dall'."],
["Metto le forchette","cassetto.","nel","in","Dentro un oggetto → nel cassetto."],
["Al mercato ho comprato","mele.","delle","di","Partitivo: delle mele = umas maçãs."],
["In aula ci sono","studenti nuovi.","degli","di","Partitivo: degli studenti."],
["Stasera andiamo","cinema.","al","a","Fisso: andare al cinema."],
["Il cane","zio è simpatico.","dello","di","di + lo zio = dello."],
["I bambini giocano","giardino della nonna.","nel","in","Giardino specificato → nel. In generale: in giardino."],
["I bambini giocano","giardino.","in","in","In senso generale → in giardino."],
["D'estate andiamo","mare.","al","a","Fisso: andare al mare."],
["Il colore","occhi è verde.","degli","di","di + gli occhi = degli."],
["Metto i libri","zaino.","nello","in","in + lo zaino = nello."],
["Bevo","acqua fresca.","dell'","di","Partitivo: dell'acqua = un po' d'acqua."],
["Abito","Ivrea.","a","a","Città → a, senza articolo."],
["Oggi devo andare","banca.","in","in","Luogo in generale → in banca."],
["La macchina","amici è rossa.","degli","di","Possesso: la macchina degli amici."],
["Metto","zucchero nel caffè.","dello","di","Partitivo: dello zucchero."],
["I ragazzi escono","stadio.","dallo","da","da + lo stadio = dallo."],
["Pensiamo già","vacanze.","alle","a","pensare a + le vacanze = alle."],
["La lezione comincia","nove.","alle","a","Ore: alle nove."],
["Ci vediamo","una e mezza.","all'","a","a + l'una = all'una."],
["Sono","nonna per il pranzo.","dalla","da","A casa di qualcuno → dalla nonna."],
["Vado a Torino","treno.","in","in","Mezzo di trasporto → in treno."],
["Ho letto un articolo","intelligenza artificiale.","sull'","su","Argomento → su: sull'intelligenza artificiale."],
["Prendo i soldi","portafoglio.","dal","da","Tirare fuori da → dal portafoglio."],
["Lavoro","ufficio, ma oggi sono a casa.","in","in","Luogo in generale → in ufficio."],
["Il report è","scrivania del direttore.","sulla","su","su + la scrivania = sulla."],
["Ho parlato","responsabile delle risorse umane.","con il","con","con non si unisce: con il responsabile."]
];
const AB=[
["","mia madre è brasiliana.","∅","Parente al singolare con possessivo → niente articolo."],
["","mie sorelle abitano a San Paolo.","le","Parente al plurale → le mie sorelle."],
["","mia casa è vicino alla stazione.","la","Possessivo con cose e luoghi → articolo."],
["","loro figlio è medico.","il","Con loro l'articolo resta sempre."],
["","mia mamma cucina benissimo.","la","Forma affettiva (mamma) → articolo."],
["Mi piacciono","spaghetti.","gli","spaghetti: maschile plurale con s + consonante → gli."],
["","sport fa bene alla salute.","lo","sport: s + consonante → lo."],
["","Italia è un paese bellissimo.","l'","Paese come soggetto → articolo."],
["Ho perso","orologio.","l'","orologio: maschile con vocale → l'."],
["Puoi chiudere","finestre?","le","finestre: femminile plurale → le."],
["Ho comprato","auto nuova.","un'","auto è femminile con vocale → un'auto.","ind"],
["Ho","amico a Milano.","un","Maschile con vocale → un amico, senza apostrofo.","ind"],
["Ho","idea!","un'","idea: femminile con vocale → un'idea.","ind"],
["Mi serve","psicologo.","uno","ps → uno psicologo.","ind"],
["Ho fatto","errore.","un","errore: maschile → un errore, senza apostrofo.","ind"]
];

/* ================= VERBI ================= */
const P6=["io","tu","lui/lei","noi","voi","loro"];
const VB=[
{v:"essere",t:"ser/estar",a:"e",pp:"stato",p:"sono sei è siamo siete sono",cp:"sia sia sia siamo siate siano",f:"sar",i:"ero eri era eravamo eravate erano",ci:"fo",irr:1},
{v:"avere",t:"ter",a:"a",pp:"avuto",p:"ho hai ha abbiamo avete hanno",cp:"abbia abbia abbia abbiamo abbiate abbiano",f:"avr",irr:1},
{v:"andare",t:"ir",a:"e",pp:"andato",p:"vado vai va andiamo andate vanno",cp:"vada vada vada andiamo andiate vadano",f:"andr",irr:1},
{v:"fare",t:"fazer",a:"a",pp:"fatto",p:"faccio fai fa facciamo fate fanno",cp:"faccia faccia faccia facciamo facciate facciano",f:"far",i:"face",ci:"face",irr:1},
{v:"venire",t:"vir",a:"e",pp:"venuto",p:"vengo vieni viene veniamo venite vengono",cp:"venga venga venga veniamo veniate vengano",f:"verr",irr:1},
{v:"stare",t:"estar/ficar",a:"e",pp:"stato",p:"sto stai sta stiamo state stanno",cp:"stia stia stia stiamo stiate stiano",f:"star",ci:"ste",irr:1},
{v:"potere",t:"poder",a:"a",pp:"potuto",p:"posso puoi può possiamo potete possono",cp:"possa possa possa possiamo possiate possano",f:"potr",irr:1},
{v:"volere",t:"querer",a:"a",pp:"voluto",p:"voglio vuoi vuole vogliamo volete vogliono",cp:"voglia voglia voglia vogliamo vogliate vogliano",f:"vorr",irr:1},
{v:"dovere",t:"dever",a:"a",pp:"dovuto",p:"devo devi deve dobbiamo dovete devono",cp:"debba debba debba dobbiamo dobbiate debbano",f:"dovr",irr:1},
{v:"sapere",t:"saber",a:"a",pp:"saputo",p:"so sai sa sappiamo sapete sanno",cp:"sappia sappia sappia sappiamo sappiate sappiano",f:"sapr",irr:1},
{v:"dire",t:"dizer",a:"a",pp:"detto",p:"dico dici dice diciamo dite dicono",cp:"dica dica dica diciamo diciate dicano",f:"dir",i:"dice",ci:"dice",irr:1},
{v:"uscire",t:"sair",a:"e",pp:"uscito",p:"esco esci esce usciamo uscite escono",cp:"esca esca esca usciamo usciate escano",irr:1},
{v:"dare",t:"dar",a:"a",pp:"dato",p:"do dai dà diamo date danno",cp:"dia dia dia diamo diate diano",f:"dar",ci:"de",irr:1},
{v:"bere",t:"beber",a:"a",pp:"bevuto",p:"bevo bevi beve beviamo bevete bevono",f:"berr",i:"beve",ci:"beve",irr:1},
{v:"rimanere",t:"permanecer",a:"e",pp:"rimasto",p:"rimango rimani rimane rimaniamo rimanete rimangono",f:"rimarr",irr:1},
{v:"tenere",t:"segurar/manter",a:"a",pp:"tenuto",p:"tengo tieni tiene teniamo tenete tengono",f:"terr",irr:1},
{v:"scegliere",t:"escolher",a:"a",pp:"scelto",p:"scelgo scegli sceglie scegliamo scegliete scelgono",irr:1},
{v:"piacere",t:"agradar/gostar",a:"e",pp:"piaciuto",p:"piaccio piaci piace piacciamo piacete piacciono",irr:1},
{v:"salire",t:"subir",a:"e",pp:"salito",p:"salgo sali sale saliamo salite salgono",irr:1},
{v:"vedere",t:"ver",a:"a",pp:"visto",f:"vedr"},
{v:"vivere",t:"viver",a:"a",pp:"vissuto",f:"vivr"},
{v:"parlare",t:"falar",a:"a",pp:"parlato"},{v:"lavorare",t:"trabalhar",a:"a",pp:"lavorato"},{v:"mangiare",t:"comer",a:"a",pp:"mangiato"},{v:"studiare",t:"estudar",a:"a",pp:"studiato"},
{v:"cercare",t:"procurar",a:"a",pp:"cercato"},{v:"pagare",t:"pagar",a:"a",pp:"pagato"},{v:"arrivare",t:"chegar",a:"e",pp:"arrivato"},{v:"tornare",t:"voltar",a:"e",pp:"tornato"},
{v:"cominciare",t:"começar",a:"a",pp:"cominciato"},{v:"viaggiare",t:"viajar",a:"a",pp:"viaggiato"},{v:"spiegare",t:"explicar",a:"a",pp:"spiegato"},{v:"aspettare",t:"esperar",a:"a",pp:"aspettato"},{v:"lasciare",t:"deixar",a:"a",pp:"lasciato"},
{v:"prendere",t:"pegar/tomar",a:"a",pp:"preso"},{v:"leggere",t:"ler",a:"a",pp:"letto"},{v:"scrivere",t:"escrever",a:"a",pp:"scritto"},{v:"mettere",t:"colocar",a:"a",pp:"messo"},
{v:"chiedere",t:"pedir/perguntar",a:"a",pp:"chiesto"},{v:"rispondere",t:"responder",a:"a",pp:"risposto"},{v:"decidere",t:"decidir",a:"a",pp:"deciso"},{v:"conoscere",t:"conhecer",a:"a",pp:"conosciuto"},{v:"chiudere",t:"fechar",a:"a",pp:"chiuso"},{v:"nascere",t:"nascer",a:"e",pp:"nato"},
{v:"dormire",t:"dormir",a:"a",pp:"dormito"},{v:"partire",t:"partir",a:"e",pp:"partito"},{v:"sentire",t:"ouvir/sentir",a:"a",pp:"sentito"},{v:"aprire",t:"abrir",a:"a",pp:"aperto"},{v:"offrire",t:"oferecer",a:"a",pp:"offerto"},
{v:"capire",t:"entender",a:"a",pp:"capito",isc:1},{v:"finire",t:"terminar",a:"a",pp:"finito",isc:1},{v:"preferire",t:"preferir",a:"a",pp:"preferito",isc:1},{v:"pulire",t:"limpar",a:"a",pp:"pulito",isc:1},{v:"gestire",t:"gerir",a:"a",pp:"gestito",isc:1}
];
function joinA(st,e){
  if(/[cg]i$/.test(st)&&/^e/.test(e))st=st.slice(0,-1);
  else if(/[cg]$/.test(st)&&/^[ie]/.test(e))st+="h";
  if(/i$/.test(st)&&/^i/.test(e))st=st.slice(0,-1);
  return st+e;
}
const TENSES=[["pres","Presente"],["pp","Passato prossimo"],["imp","Imperfetto"],["fut","Futuro"],["cond","Condizionale"],["cpres","Congiuntivo presente"],["cimp","Congiuntivo imperfetto"]];
const AUX={a:"ho hai ha abbiamo avete hanno".split(" "),e:"sono sei è siamo siete sono".split(" ")};
function conj(V,t){
  const typ=V.v.slice(-3),st=V.v.slice(0,-3),sp=s=>s.split(" ");
  const pres=()=>{if(V.p)return sp(V.p);
    if(typ==="are")return ["o","i","a","iamo","ate","ano"].map(e=>joinA(st,e));
    if(typ==="ere")return ["o","i","e","iamo","ete","ono"].map(e=>st+e);
    return (V.isc?["isco","isci","isce","iamo","ite","iscono"]:["o","i","e","iamo","ite","ono"]).map(e=>st+e);};
  const fstem=()=>V.f||(typ==="are"?joinA(st,"er"):V.v.slice(0,-1));
  if(t==="pres")return pres();
  if(t==="imp"){if(V.i&&V.i.includes(" "))return sp(V.i);const b=V.i||V.v.slice(0,-2);return ["vo","vi","va","vamo","vate","vano"].map(e=>b+e);}
  if(t==="fut")return ["ò","ai","à","emo","ete","anno"].map(e=>fstem()+e);
  if(t==="cond")return ["ei","esti","ebbe","emmo","este","ebbero"].map(e=>fstem()+e);
  if(t==="cimp"){const b=V.ci||V.v.slice(0,-2);return ["ssi","ssi","sse","ssimo","ste","ssero"].map(e=>b+e);}
  if(t==="cpres"){if(V.cp)return sp(V.cp);
    if(typ==="are")return ["i","i","i","iamo","iate","ino"].map(e=>joinA(st,e));
    const p=pres(),s=p[0].slice(0,-1);return [s+"a",s+"a",s+"a",p[3],p[3].replace(/mo$/,"te"),s+"ano"];}
  if(t==="pp"){const aux=AUX[V.a];if(V.a==="a")return aux.map(x=>x+" "+V.pp);const b=V.pp.slice(0,-1);
    return aux.map((x,i)=>x+" "+(i<3?b+"o/a":b+"i/e"));}
}

// verbi in contesto: [frase, opzioni, risposta, spiegazione]
const VC=[
["Penso che Marco ___ ragione.",["abbia","ha","avesse"],"abbia","Pensare che + congiuntivo presente."],
["Pensavo che Marco ___ ragione.",["avesse","abbia","aveva"],"avesse","Principale al passato → congiuntivo imperfetto."],
["Se ___ più tempo, studierei di più.",["avessi","avrei","ho"],"avessi","Possibilità: se + congiuntivo imperfetto, poi condizionale."],
["Se avessi studiato, ___ l'esame.",["avrei superato","avessi superato","superavo"],"avrei superato","Irrealtà nel passato: condizionale passato."],
["Se domani piove, ___ a casa.",["restiamo","restassimo","resteremmo"],"restiamo","Realtà: se + presente, poi presente o futuro."],
["Vorrei che tu ___ con me.",["venissi","venga","vieni"],"venissi","Vorrei (condizionale) che + congiuntivo imperfetto."],
["Voglio che tu ___ con me.",["venga","venissi","vieni"],"venga","Voglio (presente) che + congiuntivo presente."],
["Benché ___ tardi, continuiamo a lavorare.",["sia","è","fosse"],"sia","Benché + congiuntivo."],
["È importante che tutti ___ in orario.",["arrivino","arrivano","arriverebbero"],"arrivino","È importante che + congiuntivo."],
["So che tu ___ ragione.",["hai","abbia","avessi"],"hai","Sapere = certezza → indicativo."],
["Quando ero bambina, ___ al mare ogni estate.",["andavo","sono andata","andai"],"andavo","Abitudine nel passato → imperfetto."],
["Mentre ___, è suonato il telefono.",["cucinavo","ho cucinato","cucinerei"],"cucinavo","Azione in corso interrotta → imperfetto."],
["Ieri ___ tre ore in riunione.",["sono stata","ero","stavo"],"sono stata","Azione conclusa con durata precisa → passato prossimo."],
["Non risponde al telefono: ___ in riunione.",["sarà","sia","fosse"],"sarà","Futuro di probabilità: forse è in riunione."],
["Appena ___ il report, te lo mando.",["avrò finito","finirò","avessi finito"],"avrò finito","Futuro anteriore: azione futura che viene prima di un'altra."],
["Mi ha detto che ___ il giorno dopo.",["sarebbe venuto","verrebbe","venga"],"sarebbe venuto","Futuro nel passato → condizionale passato."],
["Al tuo posto, non lo ___.",["farei","facessi","faccio"],"farei","Ipotesi (al tuo posto) → condizionale."],
["Cerco una casa che ___ un giardino.",["abbia","ha","avrebbe"],"abbia","Relativa con requisito → congiuntivo."],
["È il film più bello che io ___.",["abbia mai visto","ho mai visto","vedessi mai"],"abbia mai visto","Superlativo relativo + che → congiuntivo."],
["Prima che tu ___, devo dirti una cosa.",["parta","parti","partirai"],"parta","Prima che + congiuntivo."],
["Nonostante ___ freddo, siamo usciti.",["facesse","faceva","faccia"],"facesse","Nonostante + congiuntivo; passato → imperfetto."],
["Magari ___ la lotteria!",["vincessi","vinco","vincerei"],"vincessi","Magari (desiderio) + congiuntivo imperfetto."],
["Si comporta come se non ___ successo niente.",["fosse","sia","è"],"fosse","Come se + congiuntivo imperfetto o trapassato."],
["Bisogna che voi ___ subito.",["partiate","partite","partireste"],"partiate","Bisogna che + congiuntivo."],
["Lo faccio purché tu mi ___.",["aiuti","aiuta","aiuteresti"],"aiuti","Purché + congiuntivo."],
["Credevo che tu ___ già partita.",["fossi","eri","saresti"],"fossi","Credevo + azione anteriore → congiuntivo trapassato (fossi partita)."],
["Sarei venuta se me lo ___.",["avessi detto","avresti detto","dicevi"],"avessi detto","Irrealtà nel passato: se + congiuntivo trapassato."],
["Dante ___ la Divina Commedia nel Trecento.",["scrisse","scrivesse","scriverebbe"],"scrisse","Fatto storico → passato remoto di scrivere."],
["Garibaldi ___ nel 1807.",["nacque","nascesse","nascerebbe"],"nacque","Passato remoto di nascere: nacque."],
["Si dice che il nuovo direttore ___ molto severo.",["sia","è","sarà"],"sia","Si dice che + congiuntivo."],
["Se fossi in te, ___ un altro lavoro.",["cercherei","cercassi","cerco"],"cercherei","Se fossi in te → condizionale."],
["Quando sono arrivata, il treno ___ già partito.",["era","è","fosse"],"era","Prima di un'azione passata → trapassato prossimo (era partito)."],
["Le ragazze sono ___ presto.",["uscite","uscito","usciti"],"uscite","Con essere il participio concorda: femminile plurale."],
["La lettera, l'ho ___ ieri.",["scritta","scritto","scritte"],"scritta","Con il pronome lo/la prima di avere, il participio concorda."],
["Affinché il progetto ___, serve più tempo.",["riesca","riesce","riuscirà"],"riesca","Affinché + congiuntivo."],
["Ti telefono appena ___ a casa.",["arrivo","arrivassi","arriverei"],"arrivo","Appena + presente (o futuro) per un'azione futura."],
["Non sapevo che tu ___ sposata.",["fossi","sei","saresti"],"fossi","Non sapevo che (dubbio, passato) → congiuntivo imperfetto."],
["Dopo che ___ la cena, siamo usciti.",["avevamo mangiato","abbiamo mangiato","mangiavamo"],"avevamo mangiato","Prima di un'altra azione passata → trapassato prossimo."]
];

/* ================= LESSICO ================= */
// [italiano, portoghese, esempio]
const VOC={
"Connettivi":[["tuttavia","contudo, no entanto","È bravo, tuttavia è spesso in ritardo."],["pertanto","portanto","Il server è lento, pertanto il report arriverà domani."],["benché","embora","Benché sia stanca, continua a lavorare."],["affinché","para que","Te lo spiego affinché tu capisca."],["purché","desde que (condição)","Vengo purché tu guidi."],["nonostante","apesar de","Nonostante la pioggia, siamo usciti."],["eppure","e mesmo assim","Ha studiato tanto, eppure non ha passato l'esame."],["bensì","mas sim","Non è un problema tecnico, bensì organizzativo."],["anzi","pelo contrário; aliás","Non è difficile, anzi è facilissimo."],["dunque","então, logo","Dunque, cominciamo."],["infatti","de fato","Era stanca, infatti è andata a letto presto."],["inoltre","além disso","Il lavoro è vicino; inoltre lo stipendio è buono."],["invece","por outro lado; em vez disso","Io lavoro, mio marito invece viaggia."],["ovvero","ou seja","Il KPI, ovvero l'indicatore chiave."],["qualora","caso (se acontecer)","Qualora ci fossero problemi, mi chiami."],["a meno che","a menos que","Esco, a meno che non piova."],["dato che","já que","Dato che sei qui, aiutami."],["comunque","de qualquer forma","Comunque vada, sarà un'esperienza."]],
"Modi di dire":[["in bocca al lupo","boa sorte (resposta: crepi!)","Domani hai il colloquio? In bocca al lupo!"],["essere al verde","estar sem dinheiro","A fine mese sono sempre al verde."],["costare un occhio della testa","custar os olhos da cara","Quella borsa costa un occhio della testa."],["non vedere l'ora","mal poder esperar","Non vedo l'ora di andare in vacanza."],["prendere un granchio","cometer um erro grosseiro","Ho preso un granchio con quei numeri."],["essere in gamba","ser muito capaz","La nuova analista è molto in gamba."],["avere un diavolo per capello","estar furioso","Oggi il capo ha un diavolo per capello."],["fare il ponte","emendar o feriado","Giovedì è festa: facciamo il ponte?"],["fare le ore piccole","ficar acordado até tarde","Ieri ho fatto le ore piccole per finire il progetto."],["rompere il ghiaccio","quebrar o gelo","Ha raccontato una barzelletta per rompere il ghiaccio."],["stare con le mani in mano","ficar de braços cruzados","Non posso stare con le mani in mano."],["a quattr'occhi","a sós, em particular","Ne parliamo a quattr'occhi."],["acqua in bocca!","bico calado!","È una sorpresa: acqua in bocca!"],["tagliare la corda","dar no pé","Alla fine della festa abbiamo tagliato la corda."],["avere le mani in pasta","estar envolvido em tudo","Lui ha le mani in pasta in ogni progetto."],["fare due passi","dar uma volta","Dopo cena facciamo due passi."],["cadere dalle nuvole","ficar surpreso, cair das nuvens","Quando l'ho saputo, sono caduta dalle nuvole."],["mettere i puntini sulle i","esclarecer os detalhes","Prima di firmare, mettiamo i puntini sulle i."]],
"Lavoro e ufficio":[["colloquio","entrevista","Ho un colloquio lunedì."],["busta paga","holerite","Controlla la busta paga."],["contratto a tempo indeterminato","contrato efetivo, sem prazo","Mi hanno offerto un contratto a tempo indeterminato."],["preavviso","aviso prévio","Il preavviso è di un mese."],["ferie","férias","Ad agosto vado in ferie."],["straordinari","horas extras","Questo mese ho fatto molti straordinari."],["scadenza","prazo","La scadenza è venerdì."],["mansioni","funções do cargo","Quali sono le mansioni?"],["dipendente","funcionário","L'azienda ha cinquanta dipendenti."],["datore di lavoro","empregador","Il mio datore di lavoro è brasiliano."],["assumere","contratar","Stanno assumendo analisti."],["licenziare","demitir","Hanno licenziato due persone."],["dimettersi","pedir demissão","Si è dimessa dopo un anno."],["tirocinio","estágio","Ho fatto un tirocinio di sei mesi."],["sede","sede, escritório","La sede è a Milano."],["partita IVA","registro de autônomo","Lavoro con partita IVA."],["candidatura","candidatura","Ho inviato la candidatura."],["lavoro da remoto","trabalho remoto","Lavoro da remoto tre giorni a settimana."]],
"Falsi amici":[["salire","subir","Saliamo al terzo piano."],["subire","sofrer (algo)","Ha subito un'operazione."],["burro","manteiga","Pane, burro e marmellata."],["squisito","delicioso","Questa torta è squisita."],["caldo","quente","Oggi fa caldo."],["cena","jantar","A che ora è la cena?"],["palestra","academia","Vado in palestra il lunedì."],["prato","gramado","I bambini giocano sul prato."],["topo","rato","C'è un topo in cantina!"],["costume","maiô / fantasia","Non dimenticare il costume da bagno."],["tasca","bolso","Le chiavi sono in tasca."],["rumore","barulho","Che rumore fa questa macchina!"],["morbido","macio","Un cuscino morbido."],["guardare","olhar","Guarda il cielo!"],["stanza","cômodo, quarto","La casa ha quattro stanze."],["tirare","puxar","Tira la porta, non spingerla."],["fermata","ponto (de ônibus)","Scendo alla prossima fermata."],["camera","quarto","La camera da letto è grande."]],
"Verbi utili C1":[["affrontare","enfrentar","Dobbiamo affrontare il problema."],["sottolineare","sublinhar, enfatizar","Vorrei sottolineare un punto."],["ritenere","considerar, achar","Ritengo che sia la scelta giusta."],["rendersi conto","dar-se conta","Mi sono resa conto dell'errore."],["approfondire","aprofundar","Approfondiamo i dati di vendita."],["raggiungere","alcançar","Abbiamo raggiunto l'obiettivo."],["svolgere","realizar, desempenhar","Svolgo attività di analisi."],["valutare","avaliar","Valutiamo le opzioni."],["impegnarsi","empenhar-se","Mi impegno a finire entro venerdì."],["risparmiare","economizar","Risparmiamo per le vacanze."],["scadere","vencer (prazo)","Il contratto scade a dicembre."],["trascurare","negligenciar","Non trascurare i dettagli."],["sfruttare","aproveitar","Sfruttiamo questa opportunità."],["ottenere","obter","Ho ottenuto il certificato."],["coinvolgere","envolver","Coinvolgiamo tutto il team."],["condividere","compartilhar","Condivido lo schermo."],["rimandare","adiar","Rimandiamo la riunione a domani."],["ammettere","admitir","Ammetto di aver sbagliato."]]
};

/* ================= TROVA L'ERRORE ================= */
// la parola sbagliata è tra *asterischi*; [frase, correzione ("∅" = da togliere), spiegazione]
const TE=[
["Ho visto *dei* studenti in biblioteca.","degli","studenti: s + consonante → gli → degli."],
["*La* problema è che non ho tempo.","Il","Problema è maschile."],
["Ieri *ho* andata al mare con i bambini.","sono","Andare usa l'ausiliare essere."],
["Abito *in* Torino da tre anni.","a","Città → a."],
["*La* mia madre lavora in banca.","∅","Parente al singolare: mia madre, senza articolo."],
["Spero che tu *hai* ragione.","abbia","Sperare che + congiuntivo."],
["Se *avrei* tempo, verrei con voi.","avessi","Dopo se mai il condizionale: se avessi."],
["Penso che lui *è* già partito.","sia","Pensare che + congiuntivo: sia partito."],
["Mi lavo le *mie* mani prima di mangiare.","∅","Parti del corpo: mi lavo le mani."],
["Ho comprato *un* zaino nuovo.","uno","zaino: z → uno."],
["Le chiavi sono *nel* borsa.","nella","borsa è femminile → nella."],
["Domani vado *alla* banca.","in","Luogo in generale: vado in banca."],
["Benché *è* stanca, continua a lavorare.","sia","Benché + congiuntivo."],
["Quando ero piccola, *sono andata* al mare ogni estate.","andavo","Abitudine → imperfetto."],
["*Gli* uova sono in frigorifero.","Le","Le uova: plurale femminile."],
["Vorrei che tu *vieni* alla festa.","venissi","Vorrei che + congiuntivo imperfetto."],
["Il libro *del* studente è sul tavolo.","dello","studente → lo → dello."],
["Ho mangiato *dello* pane.","del","pane → il → del."],
["Le ragazze sono *uscito* presto.","uscite","Con essere il participio concorda: uscite."],
["Ci vediamo *alla* mezzanotte.","a","A mezzanotte, senza articolo."],
["Gioco *al* tennis il sabato.","a","Giocare a tennis, senza articolo."],
["Mi piacciono *il* film italiani.","i","Il film → i film (plurale invariabile)."],
["*L'* zio di Marco abita a Milano.","Lo","zio: z → lo zio."],
["Credo che loro *hanno* ragione.","abbiano","Credere che + congiuntivo."],
["Il prezzo è aumentato *di* 20%.","del","Percentuali con articolo: del 20%."],
["Ho *un'* amico a Napoli.","un","Maschile: un amico, senza apostrofo."],
["Non ho *del* tempo per uscire.","∅","Con la negazione niente partitivo: non ho tempo."],
["Mio figlio suona *∅* pianoforte.","il","Suonare + strumento con articolo: il pianoforte."],
["Ieri *sono stato* al cinema con mio marito e i bambini, è stato bello.","sono stata","Se a parlare è una donna: sono stata."],
["Ho letto un articolo *sulla* intelligenza artificiale.","sull'","Davanti a vocale: sull'intelligenza."],
["Se lo sapevo prima, *venivo* anch'io.","sarei venuta","Nell'italiano formale: se l'avessi saputo, sarei venuta."],
["Lavoro qui *per* due anni.","da","Azione che continua ancora: da due anni."]
];

/* ================= RIORDINA ================= */
const RO=[
["Se avessi più tempo, studierei di più l'italiano.","Se eu tivesse mais tempo, estudaria mais italiano."],
["Benché fosse stanca, è andata alla riunione.","Embora estivesse cansada, foi à reunião."],
["Penso che sia la soluzione migliore.","Acho que é a melhor solução."],
["Gli studenti sono usciti dall'aula alle cinque.","Os alunos saíram da sala às cinco."],
["Vorrei che tu venissi con me a Torino.","Gostaria que você viesse comigo a Turim."],
["Lo scorso weekend siamo andati al mare.","No fim de semana passado fomos à praia."],
["Mi ha detto che sarebbe arrivato in ritardo.","Ele me disse que chegaria atrasado."],
["Nonostante la pioggia, abbiamo fatto una passeggiata.","Apesar da chuva, demos um passeio."],
["Le uova sono nel frigorifero.","Os ovos estão na geladeira."],
["Ho bisogno di un'informazione sul contratto.","Preciso de uma informação sobre o contrato."],
["Il problema è che non abbiamo abbastanza dati.","O problema é que não temos dados suficientes."],
["Appena avrò finito il report, te lo manderò.","Assim que terminar o relatório, te mando."],
["È il film più bello che io abbia mai visto.","É o filme mais bonito que já vi."],
["Si comporta come se fosse il capo.","Ele se comporta como se fosse o chefe."],
["Dopo il colloquio mi hanno offerto il posto.","Depois da entrevista me ofereceram a vaga."],
["Da quanto tempo vivi in Italia?","Há quanto tempo você mora na Itália?"],
["Non vedo l'ora di cominciare il nuovo lavoro.","Mal posso esperar para começar o novo trabalho."],
["Se fossi in te, accetterei l'offerta.","Se eu fosse você, aceitaria a oferta."]
];

/* ================= TESTI DA COMPLETARE ================= */
// {!giusta|altra|altra#spiegazione}
const CL=[
{t:"Ivrea",x:"Ivrea si trova {!in|nel|a#Regione → in, senza articolo.} Piemonte, a pochi chilometri {!da|di|dalla#Città → da, senza articolo.} Torino. {!La|Il|∅#Soggetto con articolo: la città.} città è conosciuta {!nel|in|al#Nel mondo (in + il).} mondo soprattutto per {!la|il|lo#Le aziende sono femminili: la Olivetti.} Olivetti, {!un'|una|un#azienda: femminile con vocale → un'azienda.} azienda che nel 1950 ha lanciato {!la|lo|il#La (macchina) Lettera 22.} Lettera 22, una macchina da scrivere portatile. Ogni anno, {!a|al|nel#Mesi: a febbraio, senza articolo.} febbraio, {!gli|i|le#abitanti: maschile plurale con vocale → gli.} abitanti festeggiano {!il|lo|l'#il Carnevale.} Carnevale con {!la|il|le#la battaglia.} famosa battaglia {!delle|dei|degli#arance: femminile plurale → delle.} arance. Dal 2018 Ivrea fa parte {!del|dello|della#patrimonio: il → del.} patrimonio UNESCO."},
{t:"Il weekend degli zii",x:"{!Lo|Il|L'#scorso: s + consonante → lo.} scorso weekend {!gli|i|le#zii: z → gli.} zii di mio marito sono {!venuti|venuto|venute#Essere + participio concorda: maschile plurale.} a trovarci. Hanno portato {!uno|un|una#yogurt: y → uno.} yogurt artigianale, {!delle|dei|degli#uova è femminile plurale → delle.} uova fresche e {!un'|una|un#enorme (femminile con vocale) → un'.} enorme torta. {!Lo|Il|L'#zio: z → lo.} zio ci ha raccontato {!le|i|gli#storie: femminile plurale.} storie della sua giovinezza, mentre {!la|lo|l'#zia: femminile → la, anche con z.} zia parlava {!del|dello|della#lavoro: il → del.} suo lavoro. A pranzo i bambini hanno mangiato {!gli|i|lo#gnocchi: gn → gli.} gnocchi e alla fine gli adulti hanno bevuto {!un|uno|una#whisky: w è consonante → un.} whisky."},
{t:"Il colloquio",x:"Ieri {!sono andata|ho andato|sono andato#Andare + essere; chi parla è donna.} a un colloquio per {!un|uno|una#posto: maschile con consonante.} posto da analista. Il direttore mi ha detto che {!cercano|cerchino|cercherebbero#Dire che + indicativo (informazione).} una persona che {!conosca|conosce|conoscesse#Relativa con requisito → congiuntivo presente.} bene Power BI e che {!sia|è|fosse#Stesso motivo: congiuntivo presente.} disponibile a lavorare in team. Credo che il colloquio {!sia andato|è andato|fosse andato#Credere che + congiuntivo passato.} bene. Se mi {!chiamassero|chiamano|chiamerebbero#Possibilità: se + congiuntivo imperfetto.}, {!accetterei|accettassi|accetto#…allora condizionale.} subito. Prima di uscire, ho lasciato {!il|lo|l'#curriculum: il.} curriculum {!alla|a|nella#Dare qualcosa a qualcuno: alla segretaria.} segretaria."},
{t:"Una giornata a Torino",x:"Sabato scorso siamo andati {!a|in|al#Città → a.} Torino {!in|col|nel#Mezzo di trasporto → in treno.} treno. Appena arrivati, abbiamo fatto colazione {!al|a|in#Fisso: al bar.} bar {!della|di|dalla#Specificazione: il bar della stazione.} stazione. Poi abbiamo visitato {!il|lo|l'#il Museo Egizio.} Museo Egizio, che è {!uno|un|una#uno dei musei (pronome).} dei musei più importanti del mondo. Nel pomeriggio ci siamo seduti {!sulla|sul|nella#riva è femminile → sulla.} riva del Po e la sera abbiamo cenato {!dagli|da|dai#A casa di persone precise: dagli amici.} amici di mio marito. Siamo tornati {!a|in|alla#Fisso: a casa.} casa a mezzanotte, stanchi ma felici."},
{t:"Se avessi saputo",x:"Quando {!sono arrivata|arrivavo|arrivai#Azione puntuale → passato prossimo.} in Italia, non {!parlavo|ho parlato|parlassi#Descrizione di una situazione → imperfetto.} bene l'italiano. Se {!avessi saputo|sapevo|avrei saputo#Irrealtà nel passato: congiuntivo trapassato.} quanto era importante la lingua, {!avrei studiato|studiassi|avessi studiato#…condizionale passato.} prima. Adesso penso che {!sia|è|fosse#Pensare che + congiuntivo presente.} fondamentale parlare bene per trovare lavoro. Benché {!faccia|fa|facesse#Benché + congiuntivo presente.} ancora qualche errore, {!capisco|capisca|capirei#Fatto reale → indicativo.} quasi tutto. L'anno prossimo {!farò|faccio|farei#Progetto futuro → futuro.} l'esame C1."}
];


/* ================= LUOGHI ================= */
// [luogo, vado ___, sono ___, torno ___ (null = non si usa), regola]
const PL=[
["casa","a","a","da","Casa propria → a casa / da casa, senza articolo. Con specificazione: nella casa di Marco."],
["scuola","a","a","da","Fisso: a scuola / da scuola."],
["teatro","a","a","da","Fisso: a teatro."],
["cinema","al","al","dal","Fisso con articolo: al cinema."],
["mare","al","al","dal","Al mare / dal mare."],
["lavoro","al","al","dal","Vado al lavoro, sono al lavoro, torno dal lavoro."],
["bar","al","al","dal","Al bar."],
["ristorante","al","al","dal","Al ristorante (ma in pizzeria, in trattoria)."],
["supermercato","al","al","dal","Al supermercato."],
["mercato","al","al","dal","Al mercato."],
["stadio","allo","allo","dallo","stadio: s + consonante → allo / dallo."],
["università","all'","all'","dall'","All'università."],
["estero","all'","all'","dall'","Fisso: all'estero (vivere all'estero)."],
["montagna","in","in","dalla","In montagna (in senso generale) → al ritorno: dalla montagna."],
["campagna","in","in","dalla","In campagna / dalla campagna."],
["centro","in","in","dal","In centro / dal centro."],
["ufficio","in","in","dall'","Luogo di tutti i giorni → in ufficio. Uscire: dall'ufficio."],
["banca","in","in","dalla","In banca / dalla banca."],
["farmacia","in","in","dalla","Negozi in -ia → in: in farmacia, in libreria, in pizzeria."],
["palestra","in","in","dalla","In palestra."],
["biblioteca","in","in","dalla","In biblioteca."],
["piscina","in","in","dalla","In piscina."],
["pizzeria","in","in","dalla","In pizzeria."],
["giardino","in","in","dal","Stanze e spazi della casa → in: in giardino, in cucina, in camera."],
["cucina","in","in","dalla","In cucina."],
["vacanza","in","in",null,"Fisso: andare / essere in vacanza (tornare dalle vacanze)."],
["medico","dal","dal","dal","Persona → da: dal medico, dal dentista."],
["dentista","dal","dal","dal","Persona → da."],
["parrucchiere","dal","dal","dal","Persona (e il suo negozio) → da."],
["nonna","dalla","dalla","dalla","A casa di una persona → da: dalla nonna."],
["Marco","da","da","da","Persona con nome → da, senza articolo."],
["amici","dagli","dagli","dagli","Persone al plurale → dagli amici."],
["Torino","a","a","da","Città → a / da, senza articolo."],
["Ivrea","a","a","da","Città → a / da."],
["Capri","a","a","da","Piccole isole come città → a Capri."],
["Italia","in","in","dall'","Paese → in, senza articolo. Provenienza: dall'Italia, con articolo."],
["Brasile","in","in","dal","Paese → in Brasile; vengo dal Brasile."],
["Francia","in","in","dalla","In Francia / dalla Francia."],
["Piemonte","in","in","dal","Regione → in Piemonte; dal Piemonte."],
["Sardegna","in","in","dalla","Grandi isole come regioni → in Sardegna."],
["Stati Uniti","negli","negli","dagli","Paese al plurale → sempre con articolo: negli Stati Uniti."]
];
const PLV=[["Vado","vado"],["Sono","sono"],["Torno","torno"]];
const PREPPOOL=["a","al","alla","all'","in","nel","nella","nell'","da","dal","dalla","dall'","negli","dagli"];
function qPlace(){let it,k;do{it=rnd(PL);k=Math.floor(Math.random()*3);}while(it[k+1]===null);
  const ans=it[k+1];const verb=["Vado","Sono","Torno"][k];const extra=it[0]==="vacanza"?"":"";
  const front=shuffle([...new Set([it[1],it[3],"a","in","da"])].filter(x=>x&&x!==ans));
  const rest=shuffle(PREPPOOL).filter(x=>x!==ans&&!front.includes(x));
  const opts=shuffle([ans,...front.concat(rest).slice(0,3)]);
  return{key:"Luoghi|"+verb+it[0],cat:"Luoghi",meta:k===0?"Dove vai?":k===1?"Dove sei?":"Da dove torni?",html:`${verb} <span class="blank">___</span> ${esc(it[0])}.`,opts,ans:[ans],show:ans,full:`${verb} ${withWord(ans,it[0])}.`,expl:it[4]};}

/* ================= SITUAZIONI ================= */
// [frase, opzioni, risposta, regola, categoria]
const SIT=[
["Vivo in Italia ___ due anni.",["da","per","fa"],"da","Azione che continua ancora → da.","Tempo"],
["Ho vissuto a Roma ___ due anni, poi mi sono trasferita.",["per","da","fra"],"per","Azione finita, durata → per.","Tempo"],
["Il treno parte ___ dieci minuti.",["tra","da","fa"],"tra","Nel futuro, a partire da adesso → tra/fra.","Tempo"],
["Sono arrivata in Italia due anni ___.",["fa","da","per"],"fa","Nel passato, contando da oggi → fa (dopo il tempo).","Tempo"],
["Devi consegnare il report ___ venerdì.",["entro","fra","per"],"entro","Scadenza (non più tardi di) → entro.","Tempo"],
["Lavoro dal lunedì ___ venerdì.",["al","a","fino"],"al","Da… a… con i giorni: dal lunedì al venerdì.","Tempo"],
["Il negozio è aperto ___ 9 alle 18.",["dalle","da","alle"],"dalle","Orario: dalle 9 alle 18 (le ore).","Tempo"],
["Mio figlio è nato ___ 2015.",["nel","in","al"],"nel","Anno → nel.","Tempo"],
["Ci vediamo ___ 15 marzo.",["il","al","nel"],"il","Data → il 15 marzo (senza preposizione).","Tempo"],
["La riunione è ___ tre.",["alle","le","a"],"alle","A che ora? → alle tre. (Che ore sono? → sono le tre.)","Tempo"],
["___ quanto tempo studi italiano?",["Da","Per","Fra"],"Da","Domanda su un'azione che continua → da quanto tempo.","Tempo"],
["Torno ___ un'ora.",["tra","da","fa"],"tra","Futuro → tra un'ora.","Tempo"],
["___ mattina vado in palestra.",["La","Alla","Nella"],"La","Abitudine: la mattina, la sera (o di mattina).","Tempo"],
["Lavoro qui ___ marzo.",["da","per","fa"],"da","Da un momento del passato fino a oggi → da marzo.","Tempo"],
["Abito ___ terzo piano.",["al","nel","sul"],"al","Piani → al terzo piano.","Luoghi"],
["Abito ___ via Roma.",["in","a","nella"],"in","Vie e piazze → in via Roma, in piazza Duomo.","Luoghi"],
["L'ho letto ___ giornale.",["sul","nel","al"],"sul","Su = la superficie dove è scritta l'informazione, non 'sopra'. Si legge sul giornale, sulla rivista, sul sito, su internet, sullo schermo. (Nel giornale = dentro l'oggetto: c'era un volantino nel giornale.)","Luoghi"],
["L'ho trovato ___ internet.",["su","in","a"],"su","Internet, siti, social → su: su internet, su LinkedIn.","Luoghi"],
["Sono ___ San Paolo, ma vivo a Ivrea.",["di","da","a"],"di","Origine con essere → di + città: sono di San Paolo.","Luoghi"],
["Vengo ___ San Paolo.",["da","di","a"],"da","Provenienza con venire → da.","Luoghi"],
["Parto ___ Roma domani mattina.",["per","a","in"],"per","Partire per + destinazione.","Luoghi"],
["Per andare a Milano passiamo ___ Novara.",["per","da","a"],"per","Passaggio attraverso un luogo → per (anche da).","Luoghi"],
["Vivo ___ estero da dieci anni.",["all'","in","nell'"],"all'","Fisso: all'estero.","Luoghi"],
["Lavoro ___ un'azienda brasiliana.",["per","in","da"],"per","Lavorare per un'azienda (per chi lavori).","Luoghi"],
["Vado a Torino ___ treno.",["in","a","da"],"in","Mezzo di trasporto → in, senza articolo.","Come"],
["Vado al lavoro ___ piedi.",["a","in","con"],"a","Eccezione: a piedi.","Come"],
["Viaggiamo ___ aereo.",["in","con","a"],"in","Mezzo → in aereo.","Come"],
["I bambini vanno a scuola ___ bici.",["in","a","su"],"in","Mezzo → in bici (in bicicletta).","Come"],
["Pago ___ contanti.",["in","con","a"],"in","Pagare in contanti.","Come"],
["Pago ___ la carta.",["con","in","a"],"con","Pagare con la carta (con il bancomat).","Come"],
["Parto ___ mio marito e i bambini.",["con","a","da"],"con","Compagnia → con.","Come"],
["Ho scritto il messaggio ___ italiano.",["in","di","a"],"in","Lingua usata → in italiano.","Come"],
["Penso spesso ___ te.",["a","di","in"],"a","Pensare a qualcuno = avere in mente.","Verbi"],
["Che cosa pensi ___ questo progetto?",["di","a","su"],"di","Pensare di = avere un'opinione.","Verbi"],
["Penso ___ cambiare lavoro.",["di","a","per"],"di","Pensare di + infinito = avere intenzione.","Verbi"],
["Ho smesso ___ fumare.",["di","a","da"],"di","Smettere di.","Verbi"],
["Ho cominciato ___ studiare il tedesco.",["a","di","per"],"a","Cominciare a.","Verbi"],
["Finalmente sono riuscita ___ finire.",["a","di","da"],"a","Riuscire a.","Verbi"],
["Ho deciso ___ restare in Italia.",["di","a","per"],"di","Decidere di.","Verbi"],
["Ho bisogno ___ un consiglio.",["di","da","a"],"di","Avere bisogno di.","Verbi"],
["Non lo so, dipende ___ te.",["da","di","a"],"da","Dipendere da.","Verbi"],
["Mi fido ___ lei.",["di","a","in"],"di","Fidarsi di.","Verbi"],
["Partecipo ___ un corso di Power BI.",["a","in","di"],"a","Partecipare a.","Verbi"],
["Provo ___ chiamarlo più tardi.",["a","di","per"],"a","Provare a.","Verbi"],
["Cerco ___ capire il problema.",["di","a","per"],"di","Cercare di + infinito = tentar.","Verbi"],
["Mi sono innamorata ___ Italia.",["dell'","all'","nell'"],"dell'","Innamorarsi di + articolo → dell'Italia.","Verbi"],
["Ho paura ___ ragni.",["dei","di","ai"],"dei","Avere paura di + i ragni → dei ragni.","Verbi"],
["Mi occupo ___ analisi dei dati.",["di","dell'","a"],"di","Occuparsi di (in senso generale, senza articolo).","Verbi"],
["Ho imparato ___ guidare a vent'anni.",["a","di","per"],"a","Imparare a.","Verbi"],
["Ti aiuto ___ fare i compiti.",["a","di","per"],"a","Aiutare qualcuno a fare.","Verbi"],
["Continua ___ piovere.",["a","di","da"],"a","Continuare a.","Verbi"],
["Spero ___ trovare un buon lavoro.",["di","a","in"],"di","Sperare di + infinito.","Verbi"],
["Mi sono dimenticata ___ chiamarti.",["di","a","da"],"di","Dimenticarsi di.","Verbi"],
["Vado ___ fare la spesa.",["a","per","di"],"a","Andare a + infinito.","Verbi"],
["Ti ringrazio ___ l'aiuto.",["per","di","a"],"per","Ringraziare per.","Verbi"],
["Abbiamo parlato ___ nuovo progetto.",["del","sul","al"],"del","Parlare di + il → del.","Verbi"],
["Posso contare ___ di te?",["su","a","in"],"su","Contare su (qualcuno).","Verbi"],
["Mio figlio si è laureato ___ ingegneria.",["in","di","a"],"in","Laurearsi in + materia.","Verbi"],
["Credo ___ te, ce la farai!",["in","a","di"],"in","Credere in qualcuno = avere fiducia.","Verbi"],
["Non credo ___ questa storia.",["a","in","di"],"a","Credere a una cosa detta = ritenerla vera.","Verbi"],
["Sono contenta ___ vederti.",["di","a","da"],"di","Contento di.","Verbi"],
["Sono pronta ___ partire.",["a","di","per"],"a","Pronto a.","Verbi"],
["Questo testo è facile ___ capire.",["da","di","a"],"da","Facile da + infinito riferito a una cosa.","Verbi"],
["È difficile ___ trovare casa a Milano.",["∅","di","da"],"∅","È difficile + infinito (soggetto) → senza preposizione.","Verbi"],
["Sono disposta ___ trasferirmi.",["a","di","per"],"a","Disposto a.","Verbi"],
["Sono stanca ___ aspettare.",["di","a","da"],"di","Stanco di.","Verbi"],
["Ho comprato una macchina ___ caffè.",["da","di","per"],"da","Scopo (a cosa serve) → da: macchina da caffè.","Da e di"],
["Dove sono i miei occhiali ___ sole?",["da","di","per"],"da","Scopo → occhiali da sole.","Da e di"],
["___ bambina abitavo a San Paolo.",["Da","Di","Per"],"Da","Età o periodo della vita → da bambina, da giovane.","Da e di"],
["Vuoi qualcosa ___ bere?",["da","di","per"],"da","Qualcosa / niente / molto + da + infinito.","Da e di"],
["Oggi ho molto ___ fare.",["da","di","a"],"da","Molto da fare.","Da e di"],
["Per la festa mi serve un vestito ___ sera.",["da","di","per"],"da","Scopo / occasione → vestito da sera.","Da e di"],
["Mi ha parlato ___ amico.",["da","come","di"],"da","Da = come (nel ruolo di): da amico.","Da e di"],
["Abbiamo un tavolo ___ legno.",["di","da","in"],"di","Materiale → di legno (anche in legno).","Da e di"],
["Ho una nipote ___ cinque anni.",["di","da","con"],"di","Età → una bambina di cinque anni.","Da e di"],
["Ho letto un libro ___ storia.",["di","da","su"],"di","Materia o tipo → un libro di storia.","Da e di"],
["Vorrei un bicchiere ___ vino.",["di","da","con"],"di","Quantità → un bicchiere di vino (ma: un bicchiere da vino = per il vino).","Da e di"],
["___ solito faccio colazione al bar.",["Di","Da","Per"],"Di","Fisso: di solito.","Da e di"],
["Ho visto un documentario ___ Leonardo.",["su","da","a"],"su","Argomento → su Leonardo (di Leonardo = fatto da lui).","Su e per"],
["Avrà ___ cinquant'anni.",["sui","di","da"],"sui","Approssimazione → sui cinquant'anni.","Su e per"],
["Tre persone ___ dieci usano lo smartphone a letto.",["su","di","per"],"su","Proporzione → tre su dieci.","Su e per"],
["Questo regalo è ___ te.",["per","a","da"],"per","Destinatario → per.","Su e per"],
["Scusa, l'ho fatto ___ errore.",["per","di","da"],"per","Causa → per errore, per caso.","Su e per"],
["Ho studiato ___ tre ore senza pause.",["per","da","fra"],"per","Durata finita → per tre ore.","Su e per"]
];

/* ================= COSTRUTTORI DI DOMANDE ================= */
function fill(p,a){let s;if(a==="∅")s=p.replace(/\s*___\s*/," ").replace(/\s+([,.!?])/g,"$1").trim();
  else s=a.endsWith("'")?p.replace("___ ",a):p.replace("___",a);return cap(s);}
const blankHtml=p=>esc(p).replace("___",'<span class="blank">___</span>');
function qList(it,cat){return{key:cat+"|"+it[0],cat,meta:cat,html:blankHtml(it[0]),opts:shuffle(it[1]),ans:[it[2]],show:it[2],full:fill(it[0],it[2]),expl:it[3]};}
function qFB(f){const p=(f[0]?f[0]+" ":"")+"___ "+f[1];const o=f[3]==="con"?["con il","con lo","con l'"]:formsOf(f[3]);
  return{key:"Preposizioni|"+p,cat:"Preposizioni",meta:"Preposizione: "+f[3],html:blankHtml(p),opts:o,ans:[f[2]],show:f[2],full:fill(p,f[2]),expl:f[4]};}
function qAB(f){const p=(f[0]?f[0]+" ":"")+"___ "+f[1];const isInd=f[4]==="ind";
  return{key:"Articoli|"+p,cat:"Articoli",meta:isInd?"Articolo indeterminativo":"Articolo (∅ = nessun articolo)",html:blankHtml(p),opts:isInd?IND:[...ARTS,"∅"],ans:[f[2]],show:f[2],full:fill(p,f[2]),expl:f[3]};}
function qWordDet(){const w=rnd(N),r=det(w);return{key:"Det|"+w[0],cat:"Articolo determinativo",meta:`${w[4]} · determinativo`,html:`<span class="blank">___</span> ${w[0]}`,opts:ARTS,ans:[r],show:r,full:withWord(r,w[0]),expl:why(w)};}
function qWordInd(){const w=rnd(N.filter(x=>x[2]==="s"&&!x[6])),r=ind(w);return{key:"Ind|"+w[0],cat:"Articolo indeterminativo",meta:`${w[4]} · indeterminativo`,html:`<span class="blank">___</span> ${w[0]}`,opts:IND,ans:[r],show:r,full:withWord(r,w[0]),expl:why(w)};}
function qWordPrep(){const w=rnd(N.filter(x=>!x[6])),p=rnd(Object.keys(PREP)),a=det(w),r=fuse(p,a);
  return{key:"Prep|"+p+w[0],cat:"Preposizione + articolo",meta:`${w[4]} · unisci preposizione e articolo`,html:`${p} + <span class="blank">___</span> ${w[0]}`,opts:formsOf(p).slice(1),ans:[r],show:r,full:withWord(r,w[0]),expl:`Articolo: ${withWord(a,w[0])}. ${p}${p==="di"?" (→ de)":p==="in"?" (→ ne)":""} + ${a} = ${r}.`};}
function qConj(tense,onlyIrr){
  const pool=onlyIrr?VB.filter(v=>v.irr):VB;const V=rnd(pool);const t=tense==="all"?rnd(TENSES)[0]:tense;const tn=TENSES.find(x=>x[0]===t)[1];
  const forms=conj(V,t);let i=Math.floor(Math.random()*6),pr=P6[i],ans;
  if(t==="pp"){const opts=[["io",0],["tu",1],["lui",2],["lei",2],["noi",3],["voi",4],["loro",5]];const c=rnd(opts);pr=c[0];i=c[1];
    const aux=AUX[V.a][i];if(V.a==="a")ans=[aux+" "+V.pp];else{const b=V.pp.slice(0,-1);
      ans=pr==="lui"?[aux+" "+b+"o"]:pr==="lei"?[aux+" "+b+"a"]:i<3?[aux+" "+b+"o",aux+" "+b+"a"]:[aux+" "+b+"i",aux+" "+b+"e"];}}
  else{if(pr==="lui/lei")pr=rnd(["lui","lei"]);ans=[forms[i]];}
  const pre=t.startsWith("c")&&t!=="cond"?"che ":"";
  const tbl=forms.map((f,k)=>`${P6[k]} ${f}`).join(" · ");
  return{key:`Coniuga|${V.v}|${t}|${pr}`,cat:"Coniugazione",meta:`${V.v} (${V.t}) · ${tn}`,html:`<span class="pron">${pre}${pr}</span> <span class="blank">___</span>`,opts:null,ans,show:ans.join(" / "),full:`${pre}${pr} ${ans.join(" / ")}`,
    expl:`${tn} di ${V.v}: ${tbl}.${t==="pp"&&V.a==="e"?" Con essere il participio concorda.":""}`};}
function qVoc(cat){const list=cat==="all"?Object.values(VOC).flat():VOC[cat];const it=rnd(list);const rev=Math.random()<.4;
  const pool=shuffle(list.filter(x=>x!==it)).slice(0,3);
  const opts=shuffle([it,...pool]).map(x=>rev?x[0]:x[1]);
  return{key:"Lessico|"+it[0]+(rev?"|r":""),cat:"Lessico",meta:rev?"Come si dice in italiano?":"Che cosa significa?",html:rev?esc(it[1]):esc(it[0]),wide:true,opts,ans:[rev?it[0]:it[1]],show:rev?it[0]:it[1],full:`${it[0]} = ${it[1]}`,expl:`Esempio: ${it[2]}`};}

/* ================= NAVIGAZIONE ================= */
const GAMES=[
{id:"luoghi",tag:"art",group:"Articoli e preposizioni",title:"Dove vai? Dove sei?",desc:"a, in o da? Con o senza articolo? 40 luoghi: città, paesi, negozi, persone.",start:()=>runQuiz(qPlace)},
{id:"sit",tag:"art",group:"Articoli e preposizioni",title:"Preposizione per situazione",desc:"Tempo, luoghi, mezzi, verbi che vogliono a/di/da, usi speciali di da, di, su, per.",chips:[["Tutto","all"],["Tempo","Tempo"],["Luoghi","Luoghi"],["Come","Come"],["Verbi","Verbi"],["Da e di","Da e di"],["Su e per","Su e per"]],
  start:c=>runQuiz(()=>{const pool=c==="all"?SIT:SIT.filter(x=>x[4]===c);const it=rnd(pool);const q=qList(it,"Situazione: "+it[4]);return q;})},
{id:"raffica",tag:"art",group:"Articoli e preposizioni",title:"Raffica a tempo",desc:"60 secondi: più articoli giusti di fila, più punti. L'errore costa 3 secondi.",start:startRaffica,chips:[["Determinativi","det"],["Indeterminativi","ind"],["Misti","mix"]]},
{id:"art",tag:"art",group:"Articoli e preposizioni",title:"Articoli in contesto",desc:"Frasi vere con i casi difficili: date, ore, titoli, paesi, parenti, nessun articolo.",chips:[["Livello C1","c1"],["Base","base"],["Possessivi","poss"],["Tutto","all"]],
  start:c=>runQuiz(()=>{const b=c==="c1"?"c1":c==="base"?rnd(["d","i","p"]):c==="poss"?"poss":rnd(["c1","c1","d","i","p","poss"]);
    return b==="c1"?qList(rnd(AC),"Articoli C1"):b==="poss"?qAB(rnd(AB)):b==="d"?qWordDet():b==="i"?qWordInd():qWordPrep();})},
{id:"prep",tag:"art",group:"Articoli e preposizioni",title:"Preposizioni articolate",desc:"nel, degli, sul, dallo… e quando NON c'è l'articolo (in banca, a Ivrea).",chips:[["Frasi","frasi"],["Preposizione + parola","parola"],["Misto","mix"]],
  start:c=>runQuiz(()=>(c==="frasi"||(c==="mix"&&Math.random()<.5))?qFB(rnd(FB)):qWordPrep())},
{id:"errore",tag:"mix",group:"Articoli e preposizioni",title:"Trova l'errore",desc:"Ogni frase ha una parola sbagliata. Toccala.",start:startErrore},
{id:"cloze",tag:"mix",group:"Articoli e preposizioni",title:"Testi da completare",desc:"Testi interi con articoli, preposizioni e verbi da scegliere.",chips:CL.map((c,i)=>[c.t,String(i)]),start:startCloze},
{id:"coniuga",tag:"verb",group:"Verbi",title:"Coniuga",desc:"Scrivi la forma giusta. Tutti i tempi dell'indicativo, condizionale e congiuntivo.",chips:[...TENSES.map(t=>[t[1],t[0]]),["Tutti i tempi","all"]],
  start:c=>runQuiz(()=>qConj(c,irrOnly),{extra:true})},
{id:"vctx",tag:"verb",group:"Verbi",title:"Verbi in contesto",desc:"Congiuntivo o indicativo? Imperfetto o passato prossimo? Periodo ipotetico.",start:()=>runQuiz(()=>qList(rnd(VC),"Verbi in contesto"),{wide:true})},
{id:"riordina",tag:"mix",group:"Verbi",title:"Riordina la frase",desc:"Metti le parole in ordine. C'è la traduzione come aiuto.",start:startRiordina},
{id:"match",tag:"voc",group:"Lessico",title:"Abbinamenti",desc:"Collega parola e significato contro il tempo.",chips:Object.keys(VOC).map(k=>[k,k]),start:startMatch},
{id:"vocq",tag:"voc",group:"Lessico",title:"Quiz di lessico",desc:"Connettivi, modi di dire, lavoro, falsi amici e verbi C1. Nei due sensi.",chips:[["Tutto","all"],...Object.keys(VOC).map(k=>[k,k])],start:c=>runQuiz(()=>qVoc(c),{wide:true})},
{id:"ripasso",tag:"mix",group:"Ripasso",title:"Ripasso degli errori",desc:"Solo le domande che hai sbagliato. Spariscono quando le indovini.",start:startRipasso}
];
let irrOnly=false;
const TAGC={art:["c-art","Articoli"],verb:["c-verb","Verbi"],voc:["c-voc","Lessico"],mix:["c-mix","Misto"]};
function renderHome(){
  const groups={};GAMES.forEach(g=>(groups[g.group]=groups[g.group]||[]).push(g));
  $("home").innerHTML=Object.entries(groups).map(([gn,gs])=>`<div class="groupt">${gn}</div><div class="tiles">${gs.map(g=>`<button class="tile" data-g="${g.id}"><span class="chip ${TAGC[g.tag][0]}">${TAGC[g.tag][1]}</span><h3>${g.title}</h3><p>${g.desc}</p></button>`).join("")}</div>`).join("");
  $("home").querySelectorAll(".tile").forEach(b=>b.onclick=()=>openGame(b.dataset.g));
}
let curGame=null,curChip=null,cleanup=null;
function openGame(id,chip){
  if(cleanup){cleanup();cleanup=null;}
  const g=GAMES.find(x=>x.id===id);curGame=g;curChip=chip||(g.chips?g.chips[0][1]:null);
  $("home").hidden=true;$("game").hidden=false;$("gtitle").textContent=g.title;$("gdesc").textContent=g.desc;
  const ch=$("gchips");ch.innerHTML="";ch.hidden=!g.chips;
  if(g.chips){g.chips.forEach(([l,v])=>{const b=document.createElement("button");b.textContent=l;b.setAttribute("aria-pressed",v===curChip);b.onclick=()=>openGame(id,v);ch.appendChild(b);});
    if(id==="coniuga"){const b=document.createElement("button");b.textContent="Solo irregolari";b.setAttribute("aria-pressed",irrOnly);b.onclick=()=>{irrOnly=!irrOnly;openGame(id,curChip);};ch.appendChild(b);}}
  g.start(curChip);
  $("game").scrollIntoView({block:"start",behavior:"smooth"});
}
$("back").onclick=()=>{if(cleanup){cleanup();cleanup=null;}$("game").hidden=true;$("home").hidden=false;renderStats();};

/* ================= MOTORE QUIZ (10 domande) ================= */
function runQuiz(gen,o={}){
  const body=$("gbody"),total=o.n||10;let i=0,ok=0,wrongs=[],q,done,used=new Set();
  function render(){
    if(i>=total)return summary();
    let tries=0;do{q=gen(i);tries++;}while(used.has(q.key)&&tries<20);used.add(q.key);done=false;
    body.innerHTML=`<div class="prog"><span style="width:${i/total*100}%"></span></div>
      <div><div class="qmeta">${esc(q.meta)}</div><div class="word">${q.html}</div></div>
      ${q.opts?`<div class="opts${(q.wide||o.wide)?" wide":""}" id="qo"></div>`:`<form class="typing" id="qf"><input id="qi" type="text" autocomplete="off" autocapitalize="none" autocorrect="off" spellcheck="false" placeholder="scrivi la risposta" aria-label="Risposta"><button class="btn2" type="submit">Verifica</button></form>`}
      <div class="fb" id="qfb" aria-live="polite"></div>
      <div class="bar"><span class="score">Domanda ${i+1} di ${total} · ${ok} giuste</span><button class="next" id="qn" disabled>Avanti →</button></div>`;
    if(q.opts){const box=$("qo");q.opts.forEach(a=>{const b=document.createElement("button");b.className="opt";b.type="button";b.textContent=a;b.onclick=()=>answer(a,b);box.appendChild(b);});}
    else{$("qf").onsubmit=e=>{e.preventDefault();const v=$("qi").value;if(v.trim())answer(v,null);};$("qi").focus({preventScroll:true});}
    $("qn").onclick=()=>{i++;render();};
  }
  function answer(given,btn){
    if(done)return;done=true;
    const g=norm(given);let res=q.ans.some(a=>norm(a)===g)?"ok":q.ans.some(a=>loose(a)===loose(g))?"acc":"no";
    if(q.opts)body.querySelectorAll(".opt").forEach(b=>{b.disabled=true;if(q.ans.includes(b.textContent))b.classList.add("right");});
    else{$("qi").disabled=true;}
    const fb=$("qfb");
    if(res!=="no"){ok++;delErr(q);tick(true);fb.className="fb ok";fb.innerHTML=`<strong>Giusto!</strong> ${esc(q.full)}${res==="acc"?`<br>Attenzione all'accento: <strong>${esc(q.show)}</strong>.`:""}<small>${esc(q.expl)}</small>`;}
    else{if(btn)btn.classList.add("wrong");wrongs.push(q);addErr(q);tick(false);fb.className="fb no";fb.innerHTML=`<strong>Sbagliato.</strong> Giusto: ${esc(q.full)}<small>${esc(q.expl)}</small>`;}
    const bl=body.querySelector(".blank");if(bl)bl.textContent=q.show==="∅"?"∅":q.show;
    $("qn").disabled=false;$("qn").focus({preventScroll:true});
  }
  function summary(){
    const pct=Math.round(ok/total*100),msg=pct===100?"Perfetto!":pct>=80?"Ottimo lavoro!":pct>=60?"Bene, continua così.":"Ripassa la grammatica e riprova.";
    body.innerHTML=`<div class="summary"><div class="big">${ok}/${total}</div><p><strong>${msg}</strong></p>
      ${wrongs.length?`<h3>Da ripassare</h3><ul class="errlist">${wrongs.map(w=>`<li>${esc(w.full)}<small>${esc(w.expl)}</small></li>`).join("")}</ul>`:""}
      <div class="row"><button class="next" id="again">Nuovo giro</button>${wrongs.length?'<button class="btn2" id="redo">Ripeti gli errori</button>':""}</div></div>`;
    $("again").onclick=()=>runQuiz(gen,o);
    if(wrongs.length){const list=shuffle(wrongs);$("redo").onclick=()=>runQuiz(k=>list[k],Object.assign({},o,{n:list.length}));}
  }
  render();
}
function startRipasso(){
  if(!S.errs.length){$("gbody").innerHTML=`<p><strong>Nessun errore da ripassare.</strong></p><p class="note">Quando sbagli una domanda in un esercizio, la trovi qui.</p>`;return;}
  const list=shuffle(S.errs).slice(0,10);runQuiz(k=>list[k],{n:list.length});
}

/* ================= RAFFICA ================= */
function startRaffica(mode){
  const body=$("gbody");let time=60,score=0,combo=0,best=0,q,wrongs=[],timer=null,lock=false;
  body.innerHTML=`<div class="summary"><p>Rispondi più veloce che puoi. Ogni 5 risposte giuste di fila i punti raddoppiano.</p><p class="note">Record attuale: <strong>${S.best}</strong></p><div class="row"><button class="next" id="go">Via!</button></div></div>`;
  $("go").onclick=begin;
  function gen(){return mode==="det"?qWordDet():mode==="ind"?qWordInd():(Math.random()<.6?qWordDet():qWordInd());}
  function begin(){
    body.innerHTML=`<div class="timer"><div class="prog"><span id="tb" style="width:100%"></span></div><span class="clock" id="clk">60</span></div>
      <div class="bar"><span class="score">Punti: <strong id="pts">0</strong></span><span class="combo" id="cmb"></span></div>
      <div><div class="qmeta" id="rm"></div><div class="word big" id="rw"></div></div><div class="opts" id="ro"></div><div class="fb" id="rf" aria-live="polite"></div>`;
    timer=setInterval(()=>{time-=.25;if(time<=0){time=0;end();}upd();},250);cleanup=()=>clearInterval(timer);next();
  }
  function upd(){const c=$("clk");if(!c)return;c.textContent=Math.ceil(time);$("tb").style.width=(time/60*100)+"%";}
  function next(){q=gen();lock=false;$("rm").textContent=q.meta;$("rw").innerHTML=q.html;$("rw").classList.remove("flash");void $("rw").offsetWidth;$("rw").classList.add("flash");
    const box=$("ro");box.innerHTML="";q.opts.forEach(a=>{const b=document.createElement("button");b.className="opt";b.textContent=a;b.onclick=()=>pick(a,b);box.appendChild(b);});}
  function pick(a,b){
    if(lock||time<=0)return;lock=true;
    if(a===q.ans[0]){combo++;best=Math.max(best,combo);score+=combo>=5?2:1;b.classList.add("right");tick(true);$("rf").className="fb ok";$("rf").textContent=q.full;setTimeout(next,350);}
    else{combo=0;time=Math.max(0,time-3);b.classList.add("wrong");wrongs.push(q);addErr(q);tick(false);
      $("ro").querySelectorAll(".opt").forEach(x=>{if(x.textContent===q.ans[0])x.classList.add("right");});
      $("rf").className="fb no";$("rf").innerHTML=`<strong>${esc(q.full)}</strong> <small>${esc(q.expl)}</small>`;setTimeout(next,1500);}
    $("pts").textContent=score;$("cmb").textContent=combo>=5?`Serie ${combo} · punti ×2`:combo>=2?`Serie ${combo}`:"";
  }
  function end(){clearInterval(timer);cleanup=null;const rec=score>S.best;if(rec){S.best=score;save();renderStats();}
    body.innerHTML=`<div class="summary"><div class="big">${score} punti</div><p><strong>${rec?"Nuovo record!":"Record: "+S.best}</strong> · serie migliore: ${best}</p>
      ${wrongs.length?`<h3>Errori</h3><ul class="errlist">${wrongs.map(w=>`<li>${esc(w.full)}<small>${esc(w.expl)}</small></li>`).join("")}</ul>`:""}
      <div class="row"><button class="next" id="again">Gioca ancora</button></div></div>`;
    $("again").onclick=()=>startRaffica(mode);}
}

/* ================= TROVA L'ERRORE ================= */
function startErrore(){
  const body=$("gbody"),list=shuffle(TE).slice(0,10);let i=0,ok=0,wrongs=[];
  function render(){
    if(i>=list.length)return end();
    const [s,corr,ex]=list[i];const toks=s.split(" ");let bad=-1;
    const clean=toks.map((t,k)=>{if(/^\*.*\*[,.!?]?$/.test(t)||/^\*/.test(t)){bad=k;return t.replace(/\*/g,"");}return t;});
    // gestisce errori di più parole (*sono stato*)
    let badEnd=bad;if(bad>-1&&!/\*[,.!?]?$/.test(toks[bad])){for(let k=bad+1;k<toks.length;k++){if(/\*/.test(toks[k])){badEnd=k;break;}}}
    const parts=[];for(let k=0;k<toks.length;k++){if(k===bad){parts.push({t:toks.slice(bad,badEnd+1).join(" ").replace(/\*/g,""),bad:true});k=badEnd;}else parts.push({t:toks[k].replace(/\*/g,""),bad:false});}
    const vis=parts.filter(p=>p.t!=="∅"||p.bad);
    body.innerHTML=`<div class="prog"><span style="width:${i/list.length*100}%"></span></div>
      <p class="qmeta">Tocca la parola sbagliata${vis.some(p=>p.t==="∅")?" (∅ = manca una parola)":""}.</p>
      <div class="tokens" id="tk"></div><div class="fb" id="ef" aria-live="polite"></div>
      <div class="bar"><span class="score">Frase ${i+1} di ${list.length} · ${ok} giuste</span><button class="next" id="en" disabled>Avanti →</button></div>`;
    const tk=$("tk");let done=false;
    vis.forEach(p=>{const b=document.createElement("button");b.className="tok";b.textContent=p.t;b.onclick=()=>{
      if(done)return;done=true;tk.querySelectorAll(".tok").forEach(x=>x.disabled=true);
      const fixed=vis.map(x=>x.bad?(corr==="∅"?"":corr):x.t).filter(Boolean).join(" ").replace(/' /g,"'").replace(/ ([,.!?])/g,"$1");
      const fixedCap=cap(fixed);
      const tgt=[...tk.children][vis.indexOf(vis.find(x=>x.bad))];tgt.classList.add("right");
      if(p.bad){ok++;tick(true);$("ef").className="fb ok";$("ef").innerHTML=`<strong>Trovato!</strong> ${esc(p.t)} → <strong>${corr==="∅"?"(togli)":esc(corr)}</strong><br>${esc(fixedCap)}<small>${esc(ex)}</small>`;}
      else{b.classList.add("wrong");wrongs.push({full:fixedCap,expl:ex});tick(false);$("ef").className="fb no";$("ef").innerHTML=`<strong>No.</strong> L'errore era “${esc(vis.find(x=>x.bad).t)}” → <strong>${corr==="∅"?"(togli)":esc(corr)}</strong><br>${esc(fixedCap)}<small>${esc(ex)}</small>`;}
      $("en").disabled=false;$("en").focus({preventScroll:true});};tk.appendChild(b);});
    $("en").onclick=()=>{i++;render();};
  }
  function end(){body.innerHTML=`<div class="summary"><div class="big">${ok}/${list.length}</div>${wrongs.length?`<ul class="errlist">${wrongs.map(w=>`<li>${esc(w.full)}<small>${esc(w.expl)}</small></li>`).join("")}</ul>`:"<p><strong>Perfetto!</strong></p>"}<div class="row"><button class="next" id="again">Nuove frasi</button></div></div>`;$("again").onclick=startErrore;}
  render();
}

/* ================= RIORDINA ================= */
function startRiordina(){
  const body=$("gbody"),list=shuffle(RO).slice(0,8);let i=0,ok=0;
  function render(){
    if(i>=list.length){body.innerHTML=`<div class="summary"><div class="big">${ok}/${list.length}</div><div class="row"><button class="next" id="again">Nuove frasi</button></div></div>`;$("again").onclick=startRiordina;return;}
    const [s,pt]=list[i];const words=s.split(" ");let order=[];const pool=shuffle(words.map((w,k)=>({w,k})));
    body.innerHTML=`<div class="prog"><span style="width:${i/list.length*100}%"></span></div>
      <p class="hint">${esc(pt)}</p><div class="answerline" id="al" aria-label="La tua frase"></div><div class="tokens" id="pl"></div>
      <div class="fb" id="rf" aria-live="polite"></div>
      <div class="bar"><span class="score">Frase ${i+1} di ${list.length} · ${ok} giuste</span><div class="row"><button class="btn2" id="rc" disabled>Verifica</button><button class="next" id="rn" hidden>Avanti →</button></div></div>`;
    const draw=()=>{
      $("al").innerHTML="";order.forEach((it,idx)=>{const b=document.createElement("button");b.className="tok";b.textContent=it.w;b.onclick=()=>{order.splice(idx,1);draw();};$("al").appendChild(b);});
      $("pl").innerHTML="";pool.forEach(it=>{const b=document.createElement("button");b.className="tok"+(order.includes(it)?" used":"");b.textContent=it.w;b.disabled=order.includes(it);b.onclick=()=>{order.push(it);draw();};$("pl").appendChild(b);});
      $("rc").disabled=order.length!==words.length;};
    draw();
    $("rc").onclick=()=>{const got=order.map(o=>o.w).join(" ");const good=got===s;
      $("al").classList.add(good?"ok":"no");[...$("al").children].forEach(b=>b.disabled=true);$("pl").querySelectorAll(".tok").forEach(b=>b.disabled=true);
      if(good){ok++;tick(true);$("rf").className="fb ok";$("rf").innerHTML="<strong>Giusto!</strong>";}else{tick(false);$("rf").className="fb no";$("rf").innerHTML=`<strong>Ordine giusto:</strong> ${esc(s)}`;}
      $("rc").hidden=true;$("rn").hidden=false;$("rn").focus({preventScroll:true});};
    $("rn").onclick=()=>{i++;render();};
  }
  render();
}

/* ================= TESTI DA COMPLETARE ================= */
function startCloze(idx){
  const body=$("gbody"),c=CL[+idx||0];const blanks=[];
  const html=esc(c.x).replace(/\{([^}]*)\}/g,(m,inner)=>{const [opts,ex]=inner.split("#");const arr=opts.split("|");const right=arr.find(a=>a.startsWith("!")).slice(1);
    const all=shuffle(arr.map(a=>a.replace(/^!/,"")));const k=blanks.length;blanks.push({right,ex:ex||""});
    return `<select id="cz${k}" aria-label="Spazio ${k+1}"><option value="">…</option>${all.map(a=>`<option>${a}</option>`).join("")}</select>`;});
  body.innerHTML=`<h3>${esc(c.t)}</h3><div class="cloze">${html}</div><div class="fb" id="cf" aria-live="polite"></div>
    <div class="bar"><span class="score">${blanks.length} spazi</span><div class="row"><button class="btn2" id="cr">Ricomincia</button><button class="next" id="cc">Correggi</button></div></div>`;
  $("cr").onclick=()=>startCloze(idx);
  $("cc").onclick=()=>{let ok=0;const errs=[];blanks.forEach((b,k)=>{const s=$("cz"+k);s.classList.remove("right","wrong");const good=s.value===b.right;
      s.classList.add(good?"right":"wrong");if(good)ok++;else errs.push(`<li>Spazio ${k+1}: <strong>${b.right}</strong>${s.value?` (non “${esc(s.value)}”)`:""}<small>${b.ex}</small></li>`);});
    tick(ok===blanks.length);
    $("cf").className="fb "+(ok===blanks.length?"ok":"no");
    $("cf").innerHTML=`<strong>${ok} su ${blanks.length} giuste.</strong>${errs.length?`<ul class="errlist" style="margin-top:8px">${errs.join("")}</ul>`:" Perfetto!"}`;};
}

/* ================= ABBINAMENTI ================= */
function startMatch(cat){
  const body=$("gbody"),items=shuffle(VOC[cat]).slice(0,6);let selL=null,selR=null,found=0,errs=0,t0=Date.now(),timer;
  const L=shuffle(items),R=shuffle(items);
  body.innerHTML=`<div class="bar"><span class="score">Coppie: <strong id="mf">0</strong>/6 · errori: <strong id="me">0</strong></span><span class="clock" id="mc">0s</span></div>
    <div class="match"><div class="col" id="ml"></div><div class="col" id="mr"></div></div><div class="fb" id="mfb" aria-live="polite"></div>`;
  timer=setInterval(()=>{const c=$("mc");if(c)c.textContent=Math.round((Date.now()-t0)/1000)+"s";},500);cleanup=()=>clearInterval(timer);
  L.forEach(it=>{const b=document.createElement("button");b.className="mt it";b.textContent=it[0];b.onclick=()=>sel("L",b,it);$("ml").appendChild(b);});
  R.forEach(it=>{const b=document.createElement("button");b.className="mt";b.textContent=it[1];b.onclick=()=>sel("R",b,it);$("mr").appendChild(b);});
  function sel(side,b,it){
    if(b.classList.contains("done"))return;
    if(side==="L"){if(selL)selL.b.classList.remove("sel");selL={b,it};}else{if(selR)selR.b.classList.remove("sel");selR={b,it};}
    b.classList.add("sel");
    if(selL&&selR){const a=selL,c=selR;selL=selR=null;
      if(a.it===c.it){[a.b,c.b].forEach(x=>{x.classList.remove("sel");x.classList.add("done");x.disabled=true;});found++;tick(true);
        $("mfb").className="fb ok";$("mfb").innerHTML=`<strong>${esc(a.it[0])}</strong> = ${esc(a.it[1])}<small>${esc(a.it[2])}</small>`;
        if(found===6)finish();}
      else{errs++;tick(false);[a.b,c.b].forEach(x=>{x.classList.add("bad");setTimeout(()=>x.classList.remove("bad","sel"),600);});}
      $("mf").textContent=found;$("me").textContent=errs;}
  }
  function finish(){clearInterval(timer);cleanup=null;const s=Math.round((Date.now()-t0)/1000);
    setTimeout(()=>{body.innerHTML=`<div class="summary"><div class="big">${s} secondi</div><p><strong>${errs===0?"Nessun errore!":errs+" errori"}</strong></p>
      <ul class="errlist" style="--x:0">${items.map(it=>`<li style="border-color:var(--ok)"><strong>${esc(it[0])}</strong> = ${esc(it[1])}<small>${esc(it[2])}</small></li>`).join("")}</ul>
      <div class="row"><button class="next" id="again">Altre parole</button></div></div>`;$("again").onclick=()=>startMatch(cat);},700);}
}

/* ================= SCHEDE E CONIUGATORE ================= */
function setTab(t){const ex=t==="ex";$("tab-ex").setAttribute("aria-selected",ex);$("tab-gr").setAttribute("aria-selected",!ex);$("p-ex").hidden=!ex;$("p-gr").hidden=ex;
  try{localStorage.setItem(KEY+"-tab",t);}catch(e){}}
$("tab-ex").onclick=()=>setTab("ex");$("tab-gr").onclick=()=>setTab("gr");
document.querySelectorAll(".toc a").forEach(a=>a.onclick=e=>{e.preventDefault();document.querySelector(a.getAttribute("href")).scrollIntoView({behavior:"smooth"});});
const sel=$("conjSel");sel.innerHTML=VB.slice().sort((a,b)=>a.v.localeCompare(b.v)).map(v=>`<option value="${v.v}">${v.v} — ${v.t}</option>`).join("");sel.value="essere";
function drawConj(){const V=VB.find(v=>v.v===sel.value);const cols=TENSES.map(([k])=>conj(V,k));
  $("conjTable").innerHTML=`<thead><tr><th></th>${TENSES.map(t=>`<th>${t[1]}</th>`).join("")}</tr></thead><tbody>${P6.map((p,i)=>`<tr><th scope="row">${p}</th>${cols.map((c,k)=>`<td>${k>=5?"che ":""}${c[i]}</td>`).join("")}</tr>`).join("")}</tbody>`;}
sel.onchange=drawConj;drawConj();
try{if(localStorage.getItem(KEY+"-tab")==="gr")setTab("gr");}catch(e){}

const plc=$("plc");PL.forEach((it,k)=>{const b=document.createElement("button");b.textContent=it[0];b.setAttribute("aria-pressed",k===0);b.onclick=()=>{plc.querySelectorAll("button").forEach(x=>x.setAttribute("aria-pressed",x===b));showPlace(it);};plc.appendChild(b);});
function showPlace(it){const hl=a=>`<strong style="color:var(--hl)">${esc(a)}</strong>`;const w=(a)=>a.endsWith("'")?hl(a)+esc(it[0]):hl(a)+" "+esc(it[0]);
  $("plout").innerHTML=`<p>Vado ${w(it[1])} · Sono ${w(it[2])}${it[3]?` · Torno ${w(it[3])}`:""}</p><p class="note">${esc(it[4])}</p>`;}
showPlace(PL[0]);
renderHome();renderStats();
</script>

</body></html>
