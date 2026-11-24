<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ultimate Rizz — Македонски линии</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Space+Grotesk:wght@500;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0a0a0f;
      --bg-card: #12121a;
      --bg-card-hover: #1a1a25;
      --text: #f0f0f5;
      --text-muted: #9a9aad;
      --accent: #ff2d6a;
      --accent-2: #a855f7;
      --accent-3: #22d3ee;
      --border: #2a2a38;
      --success: #34d399;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', system-ui, sans-serif;
      background: var(--bg);
      color: var(--text);
      min-height: 100vh;
      line-height: 1.5;
      overflow-x: hidden;
    }

    /* Background glow */
    body::before {
      content: '';
      position: fixed;
      top: -30%;
      left: -20%;
      width: 70%;
      height: 70%;
      background: radial-gradient(circle, rgba(168, 85, 247, 0.12) 0%, transparent 70%);
      pointer-events: none;
      z-index: 0;
    }

    body::after {
      content: '';
      position: fixed;
      bottom: -20%;
      right: -10%;
      width: 60%;
      height: 60%;
      background: radial-gradient(circle, rgba(255, 45, 106, 0.1) 0%, transparent 70%);
      pointer-events: none;
      z-index: 0;
    }

    .container {
      max-width: 900px;
      margin: 0 auto;
      padding: 0 20px 80px;
      position: relative;
      z-index: 1;
    }

    /* Header */
    header {
      text-align: center;
      padding: 60px 0 40px;
    }

    .logo {
      font-family: 'Space Grotesk', sans-serif;
      font-size: clamp(2.4rem, 6vw, 3.5rem);
      font-weight: 700;
      background: linear-gradient(135deg, var(--accent) 0%, var(--accent-2) 50%, var(--accent-3) 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      letter-spacing: -0.03em;
      margin-bottom: 12px;
    }

    .tagline {
      color: var(--text-muted);
      font-size: 1.1rem;
      max-width: 480px;
      margin: 0 auto 32px;
    }

    /* Random Generator */
    .generator {
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 28px 24px;
      margin-bottom: 40px;
      text-align: center;
      box-shadow: 0 0 40px rgba(168, 85, 247, 0.08);
    }

    .generator-label {
      font-size: 0.8rem;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: var(--accent-2);
      margin-bottom: 16px;
      font-weight: 600;
    }

    #random-line {
      font-size: clamp(1.15rem, 3.5vw, 1.45rem);
      font-weight: 600;
      line-height: 1.4;
      min-height: 70px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 24px;
      padding: 0 8px;
      transition: opacity 0.2s;
    }

    .gen-buttons {
      display: flex;
      gap: 12px;
      justify-content: center;
      flex-wrap: wrap;
    }

    button {
      font-family: inherit;
      cursor: pointer;
      border: none;
      border-radius: 12px;
      font-weight: 600;
      font-size: 0.95rem;
      transition: all 0.2s ease;
      display: inline-flex;
      align-items: center;
      gap: 8px;
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--accent), var(--accent-2));
      color: white;
      padding: 14px 28px;
      box-shadow: 0 4px 20px rgba(255, 45, 106, 0.3);
    }

    .btn-primary:hover {
      transform: translateY(-2px);
      box-shadow: 0 6px 28px rgba(255, 45, 106, 0.4);
    }

    .btn-secondary {
      background: transparent;
      color: var(--text);
      border: 1px solid var(--border);
      padding: 13px 22px;
    }

    .btn-secondary:hover {
      background: var(--bg-card-hover);
      border-color: var(--accent-2);
    }

    .btn-copy {
      background: transparent;
      color: var(--text-muted);
      border: 1px solid var(--border);
      padding: 6px 12px;
      font-size: 0.8rem;
      border-radius: 8px;
      opacity: 0.7;
    }

    .btn-copy:hover {
      opacity: 1;
      color: var(--accent-3);
      border-color: var(--accent-3);
    }

    .btn-copy.copied {
      color: var(--success);
      border-color: var(--success);
      opacity: 1;
    }

    /* Tabs */
    .tabs {
      display: flex;
      gap: 8px;
      overflow-x: auto;
      padding-bottom: 8px;
      margin-bottom: 28px;
      scrollbar-width: none;
    }

    .tabs::-webkit-scrollbar {
      display: none;
    }

    .tab {
      background: var(--bg-card);
      color: var(--text-muted);
      border: 1px solid var(--border);
      padding: 10px 18px;
      border-radius: 999px;
      white-space: nowrap;
      font-size: 0.9rem;
    }

    .tab:hover {
      color: var(--text);
      border-color: #3a3a4a;
    }

    .tab.active {
      background: linear-gradient(135deg, rgba(255, 45, 106, 0.15), rgba(168, 85, 247, 0.15));
      color: var(--text);
      border-color: var(--accent);
    }

    /* Lines grid */
    .lines-grid {
      display: grid;
      gap: 12px;
    }

    .line-card {
      background: var(--bg-card);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 18px 18px 18px 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 16px;
      transition: all 0.2s ease;
      animation: fadeIn 0.35s ease both;
    }

    .line-card:hover {
      background: var(--bg-card-hover);
      border-color: #3a3a4a;
      transform: translateY(-1px);
    }

    .line-text {
      font-size: 1rem;
      font-weight: 500;
      flex: 1;
    }

    .category-badge {
      display: none;
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 48px 20px 24px;
      color: var(--text-muted);
      font-size: 0.85rem;
    }

    footer span {
      color: var(--accent);
    }

    /* Toast */
    .toast {
      position: fixed;
      bottom: 28px;
      left: 50%;
      transform: translateX(-50%) translateY(80px);
      background: #1f1f2e;
      color: var(--success);
      padding: 12px 24px;
      border-radius: 12px;
      font-weight: 600;
      font-size: 0.9rem;
      border: 1px solid rgba(52, 211, 153, 0.3);
      box-shadow: 0 8px 30px rgba(0,0,0,0.4);
      transition: transform 0.3s ease;
      z-index: 100;
      pointer-events: none;
    }

    .toast.show {
      transform: translateX(-50%) translateY(0);
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(8px); }
      to { opacity: 1; transform: translateY(0); }
    }

    /* Mobile tweaks */
    @media (max-width: 560px) {
      header { padding: 40px 0 28px; }
      .generator { padding: 22px 18px; }
      .line-card { padding: 16px; }
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <h1 class="logo">Ultimate Rizz</h1>
      <p class="tagline">Најглатките, најсмешните и најдобрите линии за да го кренеш нивото.</p>
    </header>

    <!-- Random Generator -->
    <section class="generator">
      <div class="generator-label">Случаен Риз</div>
      <div id="random-line">Кликни за нова линија</div>
      <div class="gen-buttons">
        <button class="btn-primary" onclick="generateRandom()">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><path d="M21 12a9 9 0 1 1-9-9c2.5 0 4.8 1 6.5 2.7"/><path d="M21 3v6h-6"/></svg>
          Удри
        </button>
        <button class="btn-secondary" onclick="copyRandom()">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="9" y="9" width="13" height="13" rx="2"/><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"/></svg>
          Копирај
        </button>
      </div>
    </section>

    <!-- Category Tabs -->
    <div class="tabs" id="tabs">
      <button class="tab active" data-cat="all">Сите</button>
      <button class="tab" data-cat="smooth">Глатки</button>
      <button class="tab" data-cat="funny">Смешни</button>
      <button class="tab" data-cat="cheesy">Кичеви</button>
      <button class="tab" data-cat="modern">Модерни</button>
      <button class="tab" data-cat="text">За пораки</button>
    </div>

    <!-- Lines -->
    <div class="lines-grid" id="lines-grid"></div>
  </div>

  <footer>
    Направено со <span>♥</span> за максимален риз · Користи одговорно<br>
    <em style="display:inline-block; margin-top:10px; color:var(--text-muted); font-size:0.9rem;">Made by Бојан Јовановски</em>
  </footer>

  <div class="toast" id="toast">Копирано!</div>

  <script>
    const lines = [
      // Smooth / Глатки
      { text: "Не сум фотограф, но можам да нè замислам заедно.", cat: "smooth" },
      { text: "Мора да си Wi-Fi, бидејќи чувствувам силна врска.", cat: "smooth" },
      { text: "Ако убавината беше кривично дело, ќе добиеш доживотна казна.", cat: "smooth" },
      { text: "Дали си маѓепсник? Бидејќи секојпат кога те гледам, сите други исчезнуваат.", cat: "smooth" },
      { text: "Сакав да бидам кул, ама ти целосно ми го расипа тоа.", cat: "smooth" },
      { text: "Нешто кај тебе ми е лесно да разговарам. Тоа е ретко.", cat: "smooth" },
      { text: "Имаш насмевка што прави луѓето да заборават што сакале да кажат. Јас штотуку заборавив.", cat: "smooth" },
      { text: "Можев да пратам pickup линија, или едноставно да кажам дека си прекрасна. Значи, тоа.", cat: "smooth" },
      { text: "Дури и да немаше гравитација, пак ќе паднам за тебе.", cat: "smooth" },
      { text: "Веруваш ли во љубов на прв поглед, или треба уште еднаш да поминам покрај тебе?", cat: "smooth" },
      { text: "Не си на мојата листа на желби, ама си сè што некогаш сум сакал.", cat: "smooth" },
      { text: "Не планирав да флертувам, ама ти се случи.", cat: "smooth" },
      { text: "Ти си како мојата омилена песна — цел ден ми си во глава.", cat: "smooth" },
      { text: "Ако убавината беше време, ти ќе беше вечност.", cat: "smooth" },
      { text: "Би кажал нешто паметно, ама си премногу расејувачки.", cat: "smooth" },

      // Funny / Смешни
      { text: "Дали си паркинг казна? Бидејќи имаш „фина“ напишано насекаде.", cat: "funny" },
      { text: "Дали си Французинка? Бидејќи Ејфел за тебе.", cat: "funny" },
      { text: "Мора да си од бакар и телуриум, бидејќи си Cu-Te.", cat: "funny" },
      { text: "Дали си логорски оган? Бидејќи си жешка и сакам уште.", cat: "funny" },
      { text: "Сакаш ли суво грозје? Не? Што велиш за еден дејт?", cat: "funny" },
      { text: "Ако погледите можеа да убиваат, ти ќе беше цело бојно поле.", cat: "funny" },
      { text: "Дали си од Тенеси? Бидејќи си единствената десетка што ја гледам.", cat: "funny" },
      { text: "Мојот терапевт вели дека треба да се соочам со стравовите. Значи, здраво.", cat: "funny" },
      { text: "Лош сум во small talk. Ајде да прескокнеме до делот каде што ми кажуваш најлошото мислење.", cat: "funny" },
      { text: "Дали си кредит? Бидејќи имаш цел мој интерес.", cat: "funny" },
      { text: "На скала од 1 до Америка, колку си слободна во петок навечер?", cat: "funny" },
      { text: "Ако можев да ја преуредам азбуката, ќе ги ставам У и Ј заедно.", cat: "funny" },
      { text: "Дали си тастатура? Бидејќи си токму мој тип.", cat: "funny" },
      { text: "Имаш ли фластер? Бидејќи штотуку се пресив на колено додека паѓав за тебе.", cat: "funny" },
      { text: "Математиката е збунувачка бидејќи постојано зборува за X и Y, а никогаш за У и Ј.", cat: "funny" },

      // Cheesy / Кичеви
      { text: "Дали си уморна? Бидејќи цел ден ми трчаш низ мислите.", cat: "cheesy" },
      { text: "Имаш ли име, или може да те викам моја?", cat: "cheesy" },
      { text: "Ако можев да сменам нешто кај тебе, ќе го сменам само презимето.", cat: "cheesy" },
      { text: "Мора да си речник, бидејќи додаваш значење во мојот живот.", cat: "cheesy" },
      { text: "Дали си патник низ времето? Бидејќи те гледам во мојата иднина.", cat: "cheesy" },
      { text: "Дали ти е името Google? Бидејќи имаш сè што сум го барал.", cat: "cheesy" },
      { text: "Ако беше зеленчук, ќе беше слатко-краставица.", cat: "cheesy" },
      { text: "Дали си камера? Бидејќи секојпат кога те гледам, се насмевнувам.", cat: "cheesy" },
      { text: "Мора да сум снегулка, бидејќи паднав за тебе.", cat: "cheesy" },
      { text: "Сакаш ли наука? Бидејќи имаме сериозна хемија.", cat: "cheesy" },
      { text: "Ти и јас сме како Billboard 100 — најжешките синглови во земјата.", cat: "cheesy" },
      { text: "Би те поканил надвор, ама срцето веќе рече да.", cat: "cheesy" },
      { text: "Дали си молив? Бидејќи ми го привлекуваш вниманието.", cat: "cheesy" },
      { text: "Извини, ама мислам дека ти падна нешто: мојата вилица.", cat: "cheesy" },
      { text: "Раката ти изгледа тешка — можам ли да ти ја држам?", cat: "cheesy" },

      // Modern / Модерни
      { text: "Сакав да почнам со нешто паметно, ама искрено твоите слики веќе ја завршија работата.", cat: "modern" },
      { text: "Имаш профил што тера некого да престане да скролува. Еве ме, запрев.", cat: "modern" },
      { text: "Обично не пишувам прв, ама твојот био ме натера да ги прекршам правилата.", cat: "modern" },
      { text: "Нема да лажам, го прочитав биото двапати. Тоа никогаш не се случува.", cat: "modern" },
      { text: "Сакав да бидам кул, ама изгледаш како некој за кого вреди да не бидам кул.", cat: "modern" },
      { text: "Брзо прашање: секогаш си вака убава или денес е специјална пригода?", cat: "modern" },
      { text: "Нема да се преправам дека не сум заинтересиран. Како ти е неделата?", cat: "modern" },
      { text: "Изгледаш како тип што прави здодевен вторник да биде интересен.", cat: "modern" },
      { text: "Имаш W риз и сум катастрофално заинтересиран.", cat: "modern" },
      { text: "Даваш green flag енергија и сум ослепел за сè друго.", cat: "modern" },
      { text: "Го помина vibe check-от уште пред да кажеш било што.", cat: "modern" },
      { text: "Знаам дека штотуку се матчнавме, ама веќе имам чувство дека ова ќе биде една од тие приказни.", cat: "modern" },
      { text: "Предупредување: решив дека си мојата омилена личност за разговор.", cat: "modern" },
      { text: "Ти си причината зошто се насмевнувам на телефонот како идиот.", cat: "modern" },
      { text: "Се обидував да најдам гладок начин да кажам дека ми се допаѓаш. Ова е тоа.", cat: "modern" },

      // Text Openers / За пораки
      { text: "ок твојот профил е опасно мој тип, ќе треба да ми ја објасниш третата слика", cat: "text" },
      { text: "изгледаш како човек што има силно мислење за пица со ананас. Морам да знам", cat: "text" },
      { text: "Чувствувам дека твојот вајб е или добри кафулиња или спонтани патувања. Кажи ми дека грешам.", cat: "text" },
      { text: "Нешто ми кажува дека си многу поинтересна од што може да фати една апликација.", cat: "text" },
      { text: "На скала од 1 до твојот профил, колку труд треба да вложам во оваа порака?", cat: "text" },
      { text: "Гледам дека сакаш такос. Смело од тебе да го ставиш најдоброто квалитет директно во биото.", cat: "text" },
      { text: "Ако личноста ти е барем пола добра како вкусот за музика, ќе се сложуваме одлично.", cat: "text" },
      { text: "Твојот пес изгледа како тој да одлучува со кого ќе излезеш.", cat: "text" },
      { text: "Имав цела порака подготвена, ама ги видов сликите и ја заборавив.", cat: "text" },
      { text: "Биди искрена, имаш ли дозвола за толку многу риз?", cat: "text" },
      { text: "Обично не пишувам прв, ама твојот профил изгледаше како исклучок што би жалел да не го направам.", cat: "text" },
      { text: "Пишуваш како некој што може да направи сув леб да звучи интересно — кој е секретот?", cat: "text" },
      { text: "Сакав да спијам, ама телефонот ми потсети дека постоиш.", cat: "text" },
      { text: "Здраво. Мислев дека е подобро од ништо.", cat: "text" },
      { text: "Ти ќе бидеш причината зошто нема да можам да се фокусирам цел остаток од вечерта.", cat: "text" },
    ];

    let currentCat = "all";
    let currentRandom = null;

    function renderLines() {
      const grid = document.getElementById("lines-grid");
      const filtered = currentCat === "all" ? lines : lines.filter(l => l.cat === currentCat);
      
      grid.innerHTML = filtered.map((line, i) => `
        <div class="line-card" style="animation-delay: ${i * 0.03}s">
          <div class="line-text">${line.text}</div>
          <button class="btn-copy" onclick="copyText(this, \`${line.text.replace(/`/g, "\\`")}\`)">Копирај</button>
        </div>
      `).join("");
    }

    function generateRandom() {
      const el = document.getElementById("random-line");
      el.style.opacity = "0";
      setTimeout(() => {
        const pool = currentCat === "all" ? lines : lines.filter(l => l.cat === currentCat);
        currentRandom = pool[Math.floor(Math.random() * pool.length)].text;
        el.textContent = currentRandom;
        el.style.opacity = "1";
      }, 150);
    }

    function copyText(btn, text) {
      navigator.clipboard.writeText(text).then(() => {
        btn.textContent = "Копирано!";
        btn.classList.add("copied");
        showToast();
        setTimeout(() => {
          btn.textContent = "Копирај";
          btn.classList.remove("copied");
        }, 1800);
      });
    }

    function copyRandom() {
      if (!currentRandom) {
        generateRandom();
        setTimeout(copyRandom, 200);
        return;
      }
      navigator.clipboard.writeText(currentRandom).then(showToast);
    }

    function showToast() {
      const toast = document.getElementById("toast");
      toast.classList.add("show");
      setTimeout(() => toast.classList.remove("show"), 2000);
    }

    // Tabs
    document.getElementById("tabs").addEventListener("click", (e) => {
      if (!e.target.classList.contains("tab")) return;
      document.querySelectorAll(".tab").forEach(t => t.classList.remove("active"));
      e.target.classList.add("active");
      currentCat = e.target.dataset.cat;
      renderLines();
    });

    // Init
    renderLines();
    generateRandom();
  </script>
</body>
</html>
