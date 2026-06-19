<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>孫子の兵法 — 対話式学習</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Noto+Serif+JP:wght@300;400;700&family=Noto+Sans+JP:wght@300;400;500&display=swap');

  :root {
    --ink: #1a1208;
    --parchment: #f5f0e8;
    --aged: #e8dfc8;
    --vermillion: #c0392b;
    --gold: #a67c3a;
    --fog: #7a7060;
    --paper: #faf7f2;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--parchment);
    color: var(--ink);
    font-family: 'Noto Sans JP', sans-serif;
    font-weight: 300;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }

  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background:
      radial-gradient(ellipse at 10% 20%, rgba(166,124,58,0.06) 0%, transparent 60%),
      radial-gradient(ellipse at 90% 80%, rgba(192,57,43,0.04) 0%, transparent 50%);
    pointer-events: none;
    z-index: 0;
  }

  header {
    position: relative;
    z-index: 1;
    padding: 20px 24px 16px;
    border-bottom: 1px solid var(--aged);
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: var(--paper);
  }

  .header-title {
    font-family: 'Noto Serif JP', serif;
    font-size: 18px;
    font-weight: 700;
    letter-spacing: 0.1em;
  }

  .header-sub {
    font-size: 11px;
    color: var(--fog);
    letter-spacing: 0.05em;
    margin-top: 2px;
  }

  .chapter-badge {
    background: var(--vermillion);
    color: white;
    font-size: 11px;
    padding: 4px 10px;
    border-radius: 2px;
    font-weight: 500;
    letter-spacing: 0.05em;
  }

  .chapter-nav {
    position: relative;
    z-index: 1;
    background: var(--paper);
    border-bottom: 1px solid var(--aged);
    padding: 0 16px;
    display: flex;
    overflow-x: auto;
    scrollbar-width: none;
  }
  .chapter-nav::-webkit-scrollbar { display: none; }

  .chapter-tab {
    flex-shrink: 0;
    padding: 10px 14px;
    font-size: 12px;
    font-family: 'Noto Serif JP', serif;
    color: var(--fog);
    cursor: pointer;
    border-bottom: 2px solid transparent;
    transition: all 0.2s;
    white-space: nowrap;
    background: none;
    border-top: none;
    border-left: none;
    border-right: none;
  }
  .chapter-tab:hover { color: var(--ink); }
  .chapter-tab.active {
    color: var(--vermillion);
    border-bottom-color: var(--vermillion);
    font-weight: 700;
  }

  .progress-bar {
    height: 2px;
    background: var(--aged);
    position: relative;
    z-index: 1;
  }
  .progress-fill {
    height: 100%;
    background: linear-gradient(90deg, var(--vermillion), var(--gold));
    transition: width 0.4s ease;
  }

  /* スクロール可能なメインエリア */
  main {
    position: relative;
    z-index: 1;
    flex: 1;
    display: flex;
    flex-direction: column;
    max-width: 720px;
    width: 100%;
    margin: 0 auto;
  }

  /* ===== 篇概要カード ===== */
  .chapter-card {
    margin: 14px 16px 0;
    background: white;
    border: 1px solid var(--aged);
    border-radius: 4px;
    overflow: hidden;
  }

  .chapter-card-header {
    padding: 14px 18px;
    position: relative;
    cursor: pointer;
    user-select: none;
  }
  .chapter-card-header::before {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 3px;
    background: var(--vermillion);
  }

  .chapter-num {
    font-size: 10px;
    color: var(--vermillion);
    letter-spacing: 0.1em;
    font-weight: 500;
    margin-bottom: 2px;
  }

  .chapter-name {
    font-family: 'Noto Serif JP', serif;
    font-size: 18px;
    font-weight: 700;
  }

  .chapter-quote {
    font-family: 'Noto Serif JP', serif;
    font-size: 12px;
    color: var(--gold);
    margin-top: 4px;
    line-height: 1.5;
  }

  .chapter-desc {
    font-size: 12px;
    color: var(--fog);
    line-height: 1.7;
    margin-top: 6px;
  }

  .expand-toggle {
    display: inline-flex;
    align-items: center;
    gap: 4px;
    margin-top: 8px;
    font-size: 11px;
    color: var(--vermillion);
    cursor: pointer;
    background: none;
    border: none;
    padding: 0;
    font-family: 'Noto Sans JP', sans-serif;
    font-weight: 500;
  }

  .expand-toggle .arrow {
    display: inline-block;
    transition: transform 0.2s;
    font-size: 9px;
  }
  .expand-toggle.open .arrow { transform: rotate(180deg); }

  /* ===== 詳細パネル ===== */
  .detail-panel {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.35s ease;
    border-top: 0px solid var(--aged);
  }
  .detail-panel.open {
    max-height: 900px;
    border-top: 1px solid var(--aged);
  }

  .detail-inner {
    padding: 14px 18px 16px;
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  .detail-section-title {
    font-size: 10px;
    color: var(--fog);
    letter-spacing: 0.12em;
    font-weight: 500;
    text-transform: uppercase;
    margin-bottom: 6px;
  }

  /* 要点カード */
  .keypoint-list {
    display: flex;
    flex-direction: column;
    gap: 8px;
  }

  .keypoint-item {
    background: var(--parchment);
    border-radius: 4px;
    border: 1px solid var(--aged);
    overflow: hidden;
  }

  .keypoint-title {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    padding: 10px 12px;
    cursor: pointer;
    user-select: none;
  }

  .kp-num {
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background: var(--vermillion);
    color: white;
    font-size: 10px;
    font-weight: 700;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    margin-top: 1px;
  }

  .kp-label {
    font-size: 13px;
    font-weight: 500;
    font-family: 'Noto Serif JP', serif;
    flex: 1;
    line-height: 1.4;
  }

  .kp-arrow {
    font-size: 10px;
    color: var(--fog);
    transition: transform 0.2s;
    margin-top: 4px;
  }
  .keypoint-item.open .kp-arrow { transform: rotate(180deg); }

  .keypoint-body {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.25s ease;
  }
  .keypoint-item.open .keypoint-body {
    max-height: 400px;
  }

  .keypoint-body-inner {
    padding: 0 12px 12px 42px;
    display: flex;
    flex-direction: column;
    gap: 8px;
  }

  .kp-row {
    display: flex;
    flex-direction: column;
    gap: 2px;
  }

  .kp-row-label {
    font-size: 10px;
    color: var(--vermillion);
    font-weight: 500;
    letter-spacing: 0.08em;
  }

  .kp-row-text {
    font-size: 12px;
    color: var(--ink);
    line-height: 1.7;
  }

  .kp-original {
    font-family: 'Noto Serif JP', serif;
    font-size: 12px;
    color: var(--gold);
    line-height: 1.6;
    font-style: italic;
  }

  .kp-apply {
    background: white;
    border-radius: 3px;
    padding: 6px 10px;
    font-size: 11px;
    color: var(--fog);
    line-height: 1.7;
    border: 1px solid var(--aged);
  }
  .kp-apply::before {
    content: '💡 ';
  }

  /* 分離線 */
  .detail-divider {
    height: 1px;
    background: var(--aged);
  }

  /* ===== ヒント ===== */
  .hint-strip {
    margin: 8px 16px 6px;
    display: flex;
    gap: 6px;
    overflow-x: auto;
    scrollbar-width: none;
  }
  .hint-strip::-webkit-scrollbar { display: none; }

  .hint-pill {
    flex-shrink: 0;
    background: var(--aged);
    border-radius: 20px;
    padding: 5px 12px;
    font-size: 11px;
    color: var(--ink);
    cursor: pointer;
    transition: background 0.15s;
    border: none;
    font-family: 'Noto Sans JP', sans-serif;
  }
  .hint-pill:hover { background: #d0c7b0; }

  /* ===== チャット ===== */
  .chat-area {
    flex: 1;
    overflow-y: auto;
    padding: 8px 16px;
    display: flex;
    flex-direction: column;
    gap: 10px;
    min-height: 180px;
    max-height: 320px;
  }

  .msg {
    display: flex;
    gap: 10px;
    animation: fadeUp 0.22s ease;
  }
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(6px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  .msg.user { flex-direction: row-reverse; }

  .avatar {
    width: 30px;
    height: 30px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 13px;
    flex-shrink: 0;
    font-family: 'Noto Serif JP', serif;
  }
  .avatar.ai   { background: var(--ink); color: var(--gold); }
  .avatar.user { background: var(--vermillion); color: white; }

  .bubble {
    max-width: 82%;
    padding: 9px 13px;
    font-size: 13px;
    line-height: 1.75;
  }
  .msg.ai .bubble {
    background: white;
    border: 1px solid var(--aged);
    color: var(--ink);
    border-radius: 4px 14px 14px 4px;
  }
  .msg.user .bubble {
    background: var(--ink);
    color: var(--parchment);
    border-radius: 14px 4px 4px 14px;
  }
  .bubble strong { color: var(--vermillion); font-weight: 500; }
  .bubble em { color: var(--gold); font-style: normal; font-family: 'Noto Serif JP', serif; }

  .typing-dots { display: flex; gap: 4px; padding: 4px 0; }
  .typing-dots span {
    width: 6px; height: 6px;
    background: var(--fog);
    border-radius: 50%;
    animation: dot 1.2s infinite;
  }
  .typing-dots span:nth-child(2) { animation-delay: 0.2s; }
  .typing-dots span:nth-child(3) { animation-delay: 0.4s; }
  @keyframes dot {
    0%,60%,100% { transform: scale(1); opacity: 0.5; }
    30% { transform: scale(1.3); opacity: 1; }
  }

  /* ===== 入力 ===== */
  .input-area {
    padding: 10px 16px 12px;
    background: var(--paper);
    border-top: 1px solid var(--aged);
    display: flex;
    gap: 8px;
    align-items: flex-end;
  }

  textarea {
    flex: 1;
    background: white;
    border: 1px solid var(--aged);
    border-radius: 4px;
    padding: 9px 12px;
    font-size: 13px;
    font-family: 'Noto Sans JP', sans-serif;
    color: var(--ink);
    resize: none;
    outline: none;
    min-height: 40px;
    max-height: 90px;
    line-height: 1.5;
    transition: border-color 0.15s;
  }
  textarea:focus { border-color: var(--gold); }
  textarea::placeholder { color: var(--fog); }

  .send-btn {
    background: var(--vermillion);
    color: white;
    border: none;
    border-radius: 4px;
    width: 40px;
    height: 40px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    transition: background 0.15s;
    flex-shrink: 0;
    font-size: 15px;
  }
  .send-btn:hover { background: #a93226; }
  .send-btn:disabled { background: var(--aged); cursor: not-allowed; }

  .scroll-anchor { height: 1px; }
</style>
</head>
<body>

<header>
  <div>
    <div class="header-title">孫子の兵法</div>
    <div class="header-sub">対話式 — スキマ時間学習</div>
  </div>
  <div class="chapter-badge" id="progressLabel">1 / 13 篇</div>
</header>

<div class="progress-bar">
  <div class="progress-fill" id="progressFill" style="width:7.7%"></div>
</div>

<nav class="chapter-nav" id="chapterNav"></nav>

<main>
  <div class="chapter-card" id="chapterCard"></div>
  <div class="hint-strip" id="hintStrip"></div>
  <div class="chat-area" id="chatArea"></div>
  <div class="scroll-anchor" id="scrollAnchor"></div>
  <div class="input-area">
    <textarea id="userInput" placeholder="質問を入力…（例：これをビジネスで使うと？）" rows="1"></textarea>
    <button class="send-btn" id="sendBtn">▶</button>
  </div>
</main>

<script>
const CHAPTERS = [
  {
    id:1, num:"第一篇", name:"始計篇", kanji:"始計",
    quote:"兵は国の大事なり、死生の地、存亡の道、察せざるべからず",
    quoteJP:"戦争は国家の一大事である。国民の生死、国家の存亡がかかる。慎重に考察しなければならない。",
    desc:"戦いを始める前の計画・比較の重要性。五事七計で優劣を見極める。",
    hints:["五事って何？","ビジネスで使うと？","現代の事例は？","一言で要約すると？"],
    keypoints:[
      {
        label:"五事七計 — 戦う前に勝敗を計算せよ",
        original:"主孰有道？将孰有能？天地孰得？法令孰行？兵衆孰強？士卒孰練？賞罰孰明？",
        meaning:"戦う前に「道・天・地・将・法」の五つの要素と七つの比較項目で自軍と敵軍の優劣を冷静に算出する。計算で勝てると分かれば戦い、勝てないなら戦わない。",
        apply:"新規事業を立ち上げる前に市場環境・競合・自社リソース・法規制を徹底調査し、勝算を数値化してから投資判断する。"
      },
      {
        label:"詭道十二則 — 欺くことが戦略の基本",
        original:"兵は詭道なり",
        meaning:"戦争の本質は「だますこと」。能力があっても無能に見せ、動くつもりでも動かないふりをする。敵の判断を常に狂わせ続けることが戦略の核心。",
        apply:"競合が自社の新製品発表に気づかないよう、発表直前まで別分野への投資を見せかける「フェイク戦略」はこの応用。"
      },
      {
        label:"廟算 — 会議室での勝利",
        original:"夫未戦而廟算勝者、得算多也",
        meaning:"実際に戦う前の「作戦会議（廟算）」で多くの勝算を積み上げた側が勝つ。計画の精度が戦場での結果を決定する。",
        apply:"プロジェクト開始前のキックオフで想定リスクを全て洗い出し、対策を用意しておくチームは後半で失速しにくい。"
      }
    ]
  },
  {
    id:2, num:"第二篇", name:"作戦篇", kanji:"作戦",
    quote:"兵は拙速を聞くも、いまだ巧久を見ざるなり",
    quoteJP:"戦いは多少まずくても速いほうがよく、巧みでも長引く戦いは益をもたらさない。",
    desc:"戦争のコストと速度の管理。長期戦を避け、迅速な決着を目指す。",
    hints:["拙速って何を意味する？","なぜ長期戦が危険？","プロジェクトに応用すると？","敵の資源を使う例は？"],
    keypoints:[
      {
        label:"拙速主義 — 完璧より速さを選べ",
        original:"兵は拙速を聞くも、いまだ巧久を見ざるなり",
        meaning:"「完璧に遅い」より「多少荒削りでも速い」方が戦略的に優れる。長引く戦いは資金・士気・物資を消耗し最終的に国力を蝕む。",
        apply:"スタートアップのMVP（最小限の製品）をすぐ市場に出し、フィードバックを得ながら改善するアジャイル開発はこの原理そのもの。"
      },
      {
        label:"兵糧は現地調達 — 敵の資源を奪え",
        original:"食敵一鍾、当吾二十鍾",
        meaning:"敵から奪った食料1単位は、自国から輸送した食料20単位に相当する。補給コストを削減するため、戦地では敵の資源を活用する。",
        apply:"M&Aで競合を買収し、そのブランド・顧客基盤・人材をそのまま活用することで自社開発コストを大幅削減する。"
      },
      {
        label:"長期戦の三つの害悪",
        original:"其用戦也、久則鈍兵挫鋭、攻城則力屈",
        meaning:"①兵器が摩耗し鋭さを失う ②士気が低下する ③国家財政が枯渇する。長引けば長引くほど三重苦が重なり、最終的に勝っても国が疲弊する。",
        apply:"長期化する裁判・交渉・プロジェクトは「勝利」しても組織にダメージを与える。早期和解や妥協点を探すことが賢明な場合がある。"
      }
    ]
  },
  {
    id:3, num:"第三篇", name:"謀攻篇", kanji:"謀攻",
    quote:"百戦百勝は善の善なるものにあらず。戦わずして人の兵を屈するは善の善なるものなり",
    quoteJP:"百回戦って百回勝つことは最善ではない。戦わずして敵を屈服させることこそ最善である。",
    desc:"最善は戦わずして勝つこと。謀略・外交・連合の分断で勝利する。",
    hints:["戦わずして勝つとは？","知彼知己を解説して","経営に使うと？","三つの失敗って何？"],
    keypoints:[
      {
        label:"全勝の策 — 戦わずして勝つ四段階",
        original:"上兵伐謀、其次伐交、其次伐兵、其下攻城",
        meaning:"最上策は「謀（計略で敵を崩す）」、次が「交（外交で孤立させる）」、次が「兵（野戦）」、最下策が「攻城（城攻め）」。消耗が大きい手段ほど下策。",
        apply:"競合を正面から価格競争で叩くのではなく、業界標準・規制・アライアンスを通じて競合が不利になる環境を作ることが上策。"
      },
      {
        label:"知彼知己 — 情報こそ勝利の根拠",
        original:"知彼知己、百戦不殆。不知彼而知己、一勝一負。不知彼不知己、毎戦必殆",
        meaning:"敵も自分も知れば百戦危うからず。片方だけ知れば五分五分。どちらも知らなければ必ず負ける。情報の非対称性が勝敗を決定する。",
        apply:"競合分析と自社SWOT分析を定期的に行い、業界動向・顧客インサイト・自社強弱を常に最新の状態に保つ。"
      },
      {
        label:"君主の三つの失敗 — 現場への過干渉",
        original:"将能而君不御者勝",
        meaning:"①知らないのに軍事行動を命じる ②タイミングを無視して進退を命じる ③権限を奪って将の裁量を奪う。トップが現場を信頼し任せることが組織の強さになる。",
        apply:"マイクロマネジメントする経営者は優秀な現場リーダーの判断力を殺す。戦略は本部が決め、戦術の実行は現場に委ねる委譲が鍵。"
      }
    ]
  },
  {
    id:4, num:"第四篇", name:"軍形篇", kanji:"軍形",
    quote:"勝者はまず勝ちてしかる後に戦いを求め、敗者はまず戦いてしかる後に勝ちを求む",
    quoteJP:"勝者はまず勝てる状況を作ってから戦いを求め、敗者はまず戦ってから勝ちを求めようとする。",
    desc:"守りを固めた上で勝機を待つ。「勝てる態勢」を先に作ること。",
    hints:["守りを固めるとは？","ビジネス戦略に応用すると？","勝てる態勢とは具体的に？","現代の軍事に当てはめると？"],
    keypoints:[
      {
        label:"先勝後戦 — 勝利は戦場ではなく準備段階で決まる",
        original:"勝者はまず勝ちてしかる後に戦いを求む",
        meaning:"勝てる準備が整った時にのみ戦いに臨む。勝機を作り出すのは計画と準備であり、戦場での即興ではない。負けない基盤を作ることが先決。",
        apply:"製品ローンチ前にマーケティング・販売チャネル・サポート体制を全て整えてから発売する。準備が整わないうちに出した製品は市場で失敗する。"
      },
      {
        label:"守りは隠れ、攻めは雷のごとく",
        original:"善守者、蔵於九地之下。善攻者、動於九天之上",
        meaning:"守備上手は自分の弱点を徹底的に隠し、攻撃上手は電撃的に圧倒する。守りの段階では敵に手の内を見せず、攻める時は圧倒的な力で一気に決める。",
        apply:"スタートアップは競合に知られないうちにステルスモードで開発し、準備が整った段階でグランドローンチで一気に市場を取りに行く。"
      },
      {
        label:"勝ちは量から生まれる",
        original:"称生勝、勝生奇、奇生無窮",
        meaning:"資源の量的比較 → 優劣の判断 → 勝機の創出という流れ。資源（人・物・金・情報）を正確に把握し比較することが戦略の出発点になる。",
        apply:"資金調達・採用・技術蓄積など「量」を計測・比較して競合との差を把握し、優位性がある領域に集中投資する。"
      }
    ]
  },
  {
    id:5, num:"第五篇", name:"兵勢篇", kanji:"兵勢",
    quote:"奇正の変は、循環の終わりなきがごとし",
    quoteJP:"正攻法と奇策の組み合わせは無限であり、互いに生み出し合って尽きることがない。",
    desc:"「勢い」を作り出す方法。正攻法（正）と奇策（奇）の組み合わせ。",
    hints:["正と奇って何？","ビジネスで奇策とは？","勢いを組織に作るには？","具体的な戦いの例は？"],
    keypoints:[
      {
        label:"正と奇 — 定石と奇手の無限コンビネーション",
        original:"以正合、以奇勝",
        meaning:"「正」は正面から敵と向き合い拮抗させる定石。「奇」は意表を突く奇策で勝機を作る。正で敵の注意を引きつけ、奇で致命打を与えるのが基本構造。",
        apply:"広告は王道の正攻法（テレビCM等）で認知を広げながら、バイラルマーケティングや限定コラボなど奇策で爆発的な話題を作る二段構え。"
      },
      {
        label:"勢いとは — 個人でなく構造で勝つ",
        original:"善戦者、求之於勢、不責於人",
        meaning:"優れた将は個人の能力に頼らず、「勢い」という流れ・構造を作ることで組織全体を勝利に向かわせる。まるで岩山から転げ落ちる巨石のように止められない力を生む。",
        apply:"個々の営業員の努力に依存するのではなく、マーケティングファネルとCRMシステムで「自動的に売れる仕組み」を構築する。"
      },
      {
        label:"短節 — 一瞬の勝機を逃さない",
        original:"勢険節短",
        meaning:"「勢」は険しく急峻に（一気呵成）、「節（タイミング）」は短く素早く。猛禽が獲物を仕留める瞬発力のように、勝機は短い時間で最大の力を解放する。",
        apply:"フラッシュセール・限定オファーなど「今しかない」緊迫感を作り、購買決断を後回しにさせない施策。"
      }
    ]
  },
  {
    id:6, num:"第六篇", name:"虚実篇", kanji:"虚実",
    quote:"兵の形は水に象る",
    quoteJP:"軍の形は水のようなものだ。水は高い所を避けて低いところに流れる。軍も敵の実を避けて虚を攻める。",
    desc:"敵の実（強み）を避け虚（弱み）を突く。主導権を握り敵をコントロールする。",
    hints:["虚実とは何？","競合に当てはめると？","主導権を握るには？","現代の事例は？"],
    keypoints:[
      {
        label:"虚実の原則 — 弱点を突き強みを避ける",
        original:"避実而撃虚",
        meaning:"「実」は敵の充実した強い部分、「虚」は手薄で弱い部分。強い部分に真正面からぶつかるのは愚策。相手の弱い部分・手薄な箇所を集中的に攻める。",
        apply:"大手が手を出していないニッチな地方市場や特定業種に特化してシェアを獲得し、やがて全体市場へ展開する戦略（ランチェスター戦略）。"
      },
      {
        label:"主動 vs 受動 — 敵を動かす者が勝つ",
        original:"善戦者、致人而不致於人",
        meaning:"主動（自分が主導権を握る）vs 受動（敵の流れに乗らされる）。優れた戦略家は敵を動かす側に立ち、自分が動かされる側に決して回らない。",
        apply:"競合が自社の動きに反応して対策を取るような状況を意図的に作り出すことで、競合の資源と注意を消耗させ続ける。"
      },
      {
        label:"形人而我無形 — 敵を見えるように、自分は見えなく",
        original:"形人而我無形、則我専而敵分",
        meaning:"敵の態勢を明らかにし、自分の態勢を隠せば、自軍は一点集中でき敵は分散して対応せざるを得ない。情報の非対称を利用した集中対分散の原理。",
        apply:"自社の開発ロードマップを非公開にしながら、競合の製品戦略・営業パターンを詳細に把握し先手を打ち続ける。"
      }
    ]
  },
  {
    id:7, num:"第七篇", name:"軍争篇", kanji:"軍争",
    quote:"迂を直となし、患を利となす",
    quoteJP:"遠回りの道を近道に変え、不利を有利に転換する。",
    desc:"有利な位置を争い取る技術。遠回りに見える道が実は近道になる逆説。",
    hints:["迂直の計って何？","ビジネスでの「迂回策」は？","士気の管理法は？","一言で教えて"],
    keypoints:[
      {
        label:"迂直の計 — 遠回りが最速ルート",
        original:"先処戦地而待敵者佚、後処戦地而趨戦者労",
        meaning:"敵が直線で向かう道をあえて迂回し、敵より先に有利な地点に到達する逆説的戦略。直接対決を避けながら有利なポジションを先取りする。",
        apply:"競合が直接狙う主要市場をいったん無視し、隣接する周辺市場や海外展開で力を蓄え、後から本丸市場に参入して優位に立つ。"
      },
      {
        label:"風林火山 — 状況に応じた行動原則",
        original:"其疾如風、其徐如林、侵掠如火、不動如山",
        meaning:"速攻する時は風のように迅速に、構える時は林のように静かに、攻める時は火のように激しく、守る時は山のように動じない。状況ごとに最適な姿勢を選ぶ。",
        apply:"販売攻勢期は全リソースを集中投入（火）、守備期はコスト削減と守りを固め（山）、市場調査期は静かに情報収集（林）と局面で戦略を変える。"
      },
      {
        label:"士気の三段階 — タイミングで士気が変わる",
        original:"朝気鋭、昼気惰、暮気帰",
        meaning:"戦い始めは士気が高く鋭い（朝）、中盤は惰性になる（昼）、長引くと帰りたくなる（暮）。敵の士気が低い「暮」の段階で攻撃するのが理想。",
        apply:"新製品が世に出た直後は競合も動揺し弱体化している。この「競合の士気が低い瞬間」に一気に攻勢をかけるタイミング戦略。"
      }
    ]
  },
  {
    id:8, num:"第八篇", name:"九変篇", kanji:"九変",
    quote:"将に五危あり",
    quoteJP:"将帥には五つの危険な性格がある。それぞれが致命的な弱点となる。",
    desc:"状況に応じて柔軟に戦術を変える。将帥の五つの危険な性格も論じる。",
    hints:["五危って何？","臨機応変の具体例は？","リーダーへの教訓は？","利と害を同時に考えるとは？"],
    keypoints:[
      {
        label:"九変 — 原則よりも状況適応",
        original:"将通於九変之利者、知用兵矣",
        meaning:"地形・状況・命令など、あらゆる場面で杓子定規に原則を適用せず、状況に応じて変化させる能力が将の本質。ルールに縛られることが最大のリスク。",
        apply:"コンプライアンスや社内規定に縛られて市場機会を逃さないよう、例外処理・裁量・スピード判断のルートを組織内に設計しておく。"
      },
      {
        label:"将の五危 — リーダーの致命的な性格欠陥",
        original:"将に五危あり。必死は殺され、必生は虜にされ、忿速は侮られ、廉潔は辱められ、愛民は煩わされ",
        meaning:"①無謀な勇敢さ→死 ②生き残りへの執着→捕虜 ③怒りっぽさ→軽侮 ④清廉潔癖すぎ→屈辱 ⑤過度な部下愛→煩雑な問題。美徳が過剰になると欠陥になる。",
        apply:"完璧主義すぎる管理職はチームをマイクロマネジメントし、スピードを殺す。過度な優しさは「断れないリーダー」を生み組織を混乱させる。"
      },
      {
        label:"利害同考 — メリットとリスクを常にセットで見る",
        original:"智者之慮、必雑於利害",
        meaning:"賢い将は有利な点を考える時に必ず不利な点も考え、不利な点を考える時に必ず有利な点も考える。片面だけを見た判断は必ず誤る。",
        apply:"新規事業の提案書に「期待効果」だけでなく「リスクと対策」を必ずセットで書く文化を組織に根付かせる。"
      }
    ]
  },
  {
    id:9, num:"第九篇", name:"行軍篇", kanji:"行軍",
    quote:"兵は多きをもって善しとなさず、ただ武進せず、力を併せ敵を料りて人を取るのみ",
    quoteJP:"兵の数が多ければよいわけではない。ただ無謀に進まず、敵の力を見極めながら味方を集め、適切な判断をするだけでよい。",
    desc:"地形の読み方、敵情の観察法。様々なサインから敵の状態を読む。",
    hints:["地形の読み方とは？","兆候から敵を読む例は？","組織マネジメントに使えるの？","要点をまとめて"],
    keypoints:[
      {
        label:"地形四原則 — 環境を味方につける布陣",
        original:"処山之軍、必処高、戦隆無登",
        meaning:"山は高いところに陣を張り敵を見下ろす。川は渡ってから岸を離れて陣を張る。沼地は通過するだけで留まらない。平地は背後を固め前方を開ける。地形の利を最大化した配置が基本。",
        apply:"オフィスや会議室のレイアウト・商談の場所・展示会でのブース位置など、「場の有利さ」を意識してポジションを選ぶ。"
      },
      {
        label:"敵の兆候を読む32のサイン",
        original:"敵近而静者、恃其険也。遠而挑戦者、欲人之進也",
        meaning:"近くにいて静かなのは地形の有利を頼んでいる。遠くから挑発するのはこちらを有利でない場所へ誘い出したい。32種の行動パターンから敵の心理・状況を読む観察術。",
        apply:"交渉相手が急かす時は焦りのサイン、沈黙が続く時は意図的な圧力。相手の行動パターンを観察して心理状態を推測し対応を変える。"
      },
      {
        label:"組織管理 — 罰と恩のバランス",
        original:"令素行以教其民、則民服。令不素行以教其民、則民不服",
        meaning:"普段から規律と罰則が徹底されていれば命令は通る。だが恩賞なく罰だけでは使えない。「恩で心をつかみ、罰で規律を維持する」バランスが集団統率の核心。",
        apply:"評価制度で成果を正当に報いつつ、行動規範を明確にして違反を公正に処理する。飴と鞭の公正な運用が組織の信頼を生む。"
      }
    ]
  },
  {
    id:10, num:"第十篇", name:"地形篇", kanji:"地形",
    quote:"夫れ地形は兵の助なり",
    quoteJP:"地形は戦いの補助手段である。敵を判断し、勝利を確実にし、地形の険阻・遠近を計ることは優れた将帥の道である。",
    desc:"六種の地形と六つの敗因。環境を味方につけることの重要性。",
    hints:["六種の地形って何？","六敗を教えて","市場・業界の「地形」とは？","要点だけ教えて"],
    keypoints:[
      {
        label:"六地形 — 六種の戦略的地形",
        original:"地形有通者、有挂者、有支者、有隘者、有険者、有遠者",
        meaning:"①通（双方が行き来できる）②挂（前進しやすく帰りにくい）③支（対立拮抗）④隘（狭い通路）⑤険（断崖・難所）⑥遠（距離が遠い）の六種。それぞれに最適な戦い方がある。",
        apply:"ブルーオーシャン（通）、参入したら撤退困難な市場（挂）、価格競争で拮抗（支）、参入障壁の高いニッチ（隘）など業界構造を地形として分析する。"
      },
      {
        label:"六敗 — 強さに関係なく負ける六つの原因",
        original:"走者、弛者、陥者、崩者、乱者、北者",
        meaning:"①走（兵力が多すぎる敵と正面対決）②弛（士官が弱く兵が強い不均衡）③陥（士官が強く兵が弱い不均衡）④崩（怒りに任せた将の暴走）⑤乱（将が弱く規律なし）⑥北（将が敵を読めず弱兵で強敵に当たる）。",
        apply:"組織崩壊の原因は戦略ではなく「構造の歪み」にある。管理職と現場のスキルギャップ、命令系統の不明瞭さが六敗を現代に再現する。"
      },
      {
        label:"将の独自判断 — 命令より現場を信じよ",
        original:"戦道必勝、主曰無戦、必戦可也",
        meaning:"必ず勝てると確信するなら、君主が「戦うな」と言っても戦ってよい。逆に勝てないなら「戦え」と言われても戦わなくてよい。現場の将の判断が最優先。",
        apply:"経営トップの方針より現場の判断が正しい場合もある。現場に権限を委譲し、適切な判断を下せる将（マネジャー）を育てることが組織の強さになる。"
      }
    ]
  },
  {
    id:11, num:"第十一篇", name:"九地篇", kanji:"九地",
    quote:"善く兵を用うる者は、率然の如し",
    quoteJP:"軍を巧みに用いる者は、常山の蛇・率然のようなものだ。頭を打てば尾が助け、尾を打てば頭が助け、胴を打てば頭と尾が同時に助ける。",
    desc:"九種の戦略的状況と対応法。深く敵地に入るほど兵は決死になる逆説。",
    hints:["九地とは何？","背水の陣の原理を解説","組織を奮い立たせるには？","要点だけ教えて"],
    keypoints:[
      {
        label:"九地 — 九種の戦略的状況と対応",
        original:"散地では戦うな、軽地では留まるな、争地では攻めるな",
        meaning:"①散（自国内）②軽（敵地浅く入った）③争（双方が欲しがる要地）④交（四通八達の地）⑤衢（複数国が接する）⑥重（敵地深く入った）⑦圮（沼・山林）⑧囲（細い道で出口が小）⑨死（生き延びるには戦うしかない）。各状況で対応策が異なる。",
        apply:"市場環境を九地に当てはめる。自社の本拠地（散地）、新規参入（軽地）、競合と激しく争う市場（争地）等、局面ごとに戦略を切り替える。"
      },
      {
        label:"死地に置けば生きる — 背水の陣の原理",
        original:"陥之死地然後生、投之亡地然後存",
        meaning:"兵を逃げられない「死地」に置くと生き残りのために必死になり最強になる。逃げ道を作ることが兵の弱体化につながる逆説。背水の陣はこの原理の実践。",
        apply:"「失敗したら全てを失う」という本気のコミットメント（退路を断つ）が、メンバーの本気度と創意工夫を最大化することがある。"
      },
      {
        label:"率然の組織 — 頭と尾が連動する一体感",
        original:"善く兵を用うる者は、率然の如し",
        meaning:"前線と後方が有機的に連携し、どこが攻撃されても全体で対応できる組織が最強。縦割りでバラバラに動く組織は首と尾が別々に動く死んだ蛇と同じ。",
        apply:"営業・開発・サポートがリアルタイムで情報を共有し、顧客の問題にどの部門でも即座に対応できる横断的な組織設計。"
      }
    ]
  },
  {
    id:12, num:"第十二篇", name:"火攻篇", kanji:"火攻",
    quote:"明主はこれを慮り、良将はこれを修む",
    quoteJP:"賢明な君主はこれを慎重に考慮し、優れた将はこれを厳正に実行する。",
    desc:"火攻めの五種類と使い方。感情に流されず冷静に判断する重要性。",
    hints:["五種の火攻めとは？","感情で動かない教訓とは？","ビジネスで感情的判断を避けるには？","要点だけ教えて"],
    keypoints:[
      {
        label:"五火 — 五種類の火攻め戦術",
        original:"火攻有五：一曰火人、二曰火積、三曰火輜、四曰火庫、五曰火隊",
        meaning:"①火人（敵の兵員を焼く）②火積（食料・補給物資を焼く）③火輜（輸送車を焼く）④火庫（武器庫・倉庫を焼く）⑤火隊（道路・連絡手段を断つ）。補給と通信を断てば敵は自滅する。",
        apply:"競合の「ライフライン」を断つ戦略。主要サプライヤーとの独占契約、優秀な人材の引き抜き、販売チャネルの囲い込み。"
      },
      {
        label:"感情で戦争を始めるな — 怒りは一時的、国は取り戻せない",
        original:"主不可以怒而興師、将不可以慍而致戦",
        meaning:"君主は怒りで開戦してはならず、将帥は腹立ちで戦ってはならない。怒りはいずれ喜びに変わりうるが、国の滅亡や戦死者は取り戻せない。感情的判断が最大のリスク。",
        apply:"競合の挑発・顧客クレーム・メディア批判に感情的に反応して緊急対応策を打つのは最悪手。冷静に数日待って状況を見極めてから判断する。"
      },
      {
        label:"勝ちに乗じよ — 勝利の成果を確実に活かす",
        original:"非利不動、非得不用、非危不戦",
        meaning:"利益がなければ動かない。得るものがなければ兵を使わない。危険でなければ戦わない。勝利の後、その成果を活かさず放置することは資源の無駄遣いになる。",
        apply:"商談を成立させた後、既存顧客へのアップセル・クロスセルで勝利の成果を最大化する。勝ったら次の一手を即座に打つ。"
      }
    ]
  },
  {
    id:13, num:"第十三篇", name:"用間篇", kanji:"用間",
    quote:"先知は鬼神に取ることあたわず、必ず人に取る",
    quoteJP:"事前の情報は、神に祈っても得られない。必ず人間から得るものである。",
    desc:"情報・諜報の重要性。五種のスパイを使い分け、先知（事前情報）で勝つ。",
    hints:["五種の間者って何？","現代の情報戦に当てはめると？","ビジネスインテリジェンスとは？","要点だけ教えて"],
    keypoints:[
      {
        label:"五間 — 五種類の情報収集工作員",
        original:"因間・内間・反間・死間・生間",
        meaning:"①因間（敵国の一般人を使う）②内間（敵の役人を使う）③反間（敵のスパイを二重スパイにする）④死間（偽情報を流す捨て駒）⑤生間（潜入して戻ってくる諜報員）。情報の種類と目的に応じて使い分ける。",
        apply:"①SNSユーザーの口コミ調査 ②競合社員からの情報 ③競合調査会社の活用 ④意図的なリーク情報 ⑤展示会・勉強会での直接情報収集、現代の五間。"
      },
      {
        label:"反間（二重スパイ）を最重視せよ",
        original:"五間之事、主必知之、知之必在於反間、故反間不可不厚也",
        meaning:"五間の中でも反間（敵のスパイを寝返らせる）が最も重要。敵の情報収集の実態・方法・狙いを直接知れるからだ。反間には特別に厚遇すべし。",
        apply:"競合から来た転職者・元競合パートナー・業界コンサルタントは「反間」に相当する。彼らの情報・知見を尊重し活用することが競争優位につながる。"
      },
      {
        label:"先知こそ最大の武器",
        original:"明君賢将、所以動而勝人、成功出於衆者、先知也",
        meaning:"賢明な君主と将帥が動けば勝ち、功績が群を抜く理由はただ一つ「先知（事前情報）」にある。情報こそが全ての戦略の根拠であり、最強の武器になる。",
        apply:"競合の製品ロードマップ・価格改定・組織変更を事前に把握することで、先手を打った戦略立案が可能になる。情報収集への投資は最高のROIを生む。"
      }
    ]
  }
];

let currentChapter = 0;
let isLoading = false;
let conversationHistory = [];
let detailOpen = false;

function init() {
  renderChapterNav();
  renderChapterCard();
  renderHints();
  const c = CHAPTERS[0];
  addMessage('ai', `ようこそ。<strong>孫子の兵法</strong>を対話式で学びましょう。\n\n現在は<em>「${c.name}」</em>（${c.num}）です。\n上の「▼ 詳細を見る」を押すと各篇の要点を深掘りできます。クイック質問か自由入力でAIと対話しながら理解を深めてください。`);
}

function renderChapterNav() {
  const nav = document.getElementById('chapterNav');
  nav.innerHTML = CHAPTERS.map((c, i) => `
    <button class="chapter-tab ${i === currentChapter ? 'active' : ''}" onclick="switchChapter(${i})">${c.kanji}</button>
  `).join('');
}

function renderChapterCard() {
  const c = CHAPTERS[currentChapter];
  document.getElementById('progressLabel').textContent = `${currentChapter + 1} / 13 篇`;
  document.getElementById('progressFill').style.width = `${((currentChapter + 1) / 13) * 100}%`;

  const kpHTML = c.keypoints.map((kp, ki) => `
    <div class="keypoint-item" id="kp-${ki}">
      <div class="keypoint-title" onclick="toggleKP(${ki})">
        <div class="kp-num">${ki + 1}</div>
        <div class="kp-label">${kp.label}</div>
        <div class="kp-arrow">▼</div>
      </div>
      <div class="keypoint-body">
        <div class="keypoint-body-inner">
          <div class="kp-row">
            <div class="kp-row-label">📜 原文</div>
            <div class="kp-original">「${kp.original}」</div>
          </div>
          <div class="kp-row">
            <div class="kp-row-label">💡 意味・解説</div>
            <div class="kp-row-text">${kp.meaning}</div>
          </div>
          <div class="kp-apply">${kp.apply}</div>
        </div>
      </div>
    </div>
  `).join('');

  document.getElementById('chapterCard').innerHTML = `
    <div class="chapter-card-header">
      <div class="chapter-num">${c.num}</div>
      <div class="chapter-name">${c.name}</div>
      <div class="chapter-quote">「${c.quote}」</div>
      <div class="chapter-desc">${c.desc}</div>
      <button class="expand-toggle" id="expandToggle" onclick="toggleDetail()">
        <span>▼</span>&nbsp;詳細を見る（要点 ${c.keypoints.length}項目）
      </button>
    </div>
    <div class="detail-panel" id="detailPanel">
      <div class="detail-inner">
        <div class="detail-section-title">核心要点 — 原文・解説・現代応用</div>
        <div class="keypoint-list">${kpHTML}</div>
      </div>
    </div>
  `;
  detailOpen = false;
}

function toggleDetail() {
  detailOpen = !detailOpen;
  const panel = document.getElementById('detailPanel');
  const toggle = document.getElementById('expandToggle');
  if (detailOpen) {
    panel.classList.add('open');
    toggle.classList.add('open');
    toggle.innerHTML = '<span class="arrow">▼</span>&nbsp;閉じる';
  } else {
    panel.classList.remove('open');
    toggle.classList.remove('open');
    const c = CHAPTERS[currentChapter];
    toggle.innerHTML = `<span class="arrow">▼</span>&nbsp;詳細を見る（要点 ${c.keypoints.length}項目）`;
  }
}

function toggleKP(ki) {
  const el = document.getElementById(`kp-${ki}`);
  el.classList.toggle('open');
}

function renderHints() {
  const c = CHAPTERS[currentChapter];
  document.getElementById('hintStrip').innerHTML = c.hints.map(h => `
    <button class="hint-pill" onclick="sendHint('${h}')">${h}</button>
  `).join('');
}

function switchChapter(idx) {
  currentChapter = idx;
  conversationHistory = [];
  detailOpen = false;
  renderChapterNav();
  renderChapterCard();
  renderHints();
  document.getElementById('chatArea').innerHTML = '';
  const c = CHAPTERS[idx];
  addMessage('ai', `<em>「${c.name}」</em>に切り替えました。\n\n<strong>この篇のテーマ：</strong>${c.desc}\n\n詳細パネルで原文・解説・応用を確認し、気になる点を質問してください！`);
}

function addMessage(role, text) {
  const area = document.getElementById('chatArea');
  const div = document.createElement('div');
  div.className = `msg ${role}`;
  div.innerHTML = `
    <div class="avatar ${role}">${role === 'ai' ? '孫' : '私'}</div>
    <div class="bubble">${text.replace(/\n/g, '<br>')}</div>
  `;
  area.appendChild(div);
  document.getElementById('scrollAnchor').scrollIntoView({ behavior: 'smooth' });
}

function addTyping() {
  const area = document.getElementById('chatArea');
  const div = document.createElement('div');
  div.className = 'msg ai';
  div.id = 'typingIndicator';
  div.innerHTML = `<div class="avatar ai">孫</div><div class="bubble"><div class="typing-dots"><span></span><span></span><span></span></div></div>`;
  area.appendChild(div);
  document.getElementById('scrollAnchor').scrollIntoView({ behavior: 'smooth' });
}

function removeTyping() {
  const el = document.getElementById('typingIndicator');
  if (el) el.remove();
}

async function sendMessage(userText) {
  if (!userText.trim() || isLoading) return;
  isLoading = true;
  document.getElementById('sendBtn').disabled = true;
  document.getElementById('userInput').value = '';

  addMessage('user', userText);

  const c = CHAPTERS[currentChapter];
  const kpContext = c.keypoints.map((kp, i) =>
    `要点${i+1}「${kp.label}」: 原文「${kp.original}」/ 意味: ${kp.meaning} / 応用: ${kp.apply}`
  ).join('\n');

  const systemPrompt = `あなたは孫子の兵法の専門家・解説者です。現在は「${c.name}（${c.num}）」を教えています。

この篇の概要: ${c.desc}
代表的な名言: 「${c.quote}」（${c.quoteJP}）

詳細な要点情報:
${kpContext}

回答ルール:
- 3〜5文で簡潔に（スキマ時間の学習）
- 難しい漢語は噛み砕いて解説
- 必ずビジネス・日常の具体例を1つ添える
- 原文引用には日本語訳も添える
- 親しみやすく深みのある語り口
- 詳細パネルの内容を踏まえてより深い補足を提供する
- プレーンテキストで（HTMLタグ不要）`;

  conversationHistory.push({ role: 'user', content: userText });
  addTyping();

  try {
    const res = await fetch('/api/chat', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({
        model: 'claude-sonnet-4-6',
        max_tokens: 1000,
        system: systemPrompt,
        messages: conversationHistory
      })
    });
    const data = await res.json();
    removeTyping();
    const reply = data.content?.[0]?.text || 'もう一度お試しください。';
    conversationHistory.push({ role: 'assistant', content: reply });
    addMessage('ai', reply);
  } catch (e) {
    removeTyping();
    addMessage('ai', 'エラーが発生しました。もう一度お試しください。');
  }

  isLoading = false;
  document.getElementById('sendBtn').disabled = false;
}

function sendHint(text) {
  document.getElementById('userInput').value = text;
  sendMessage(text);
}

document.getElementById('sendBtn').addEventListener('click', () => {
  sendMessage(document.getElementById('userInput').value);
});

document.getElementById('userInput').addEventListener('keydown', e => {
  if (e.key === 'Enter' && !e.shiftKey) {
    e.preventDefault();
    sendMessage(e.target.value);
  }
});

document.getElementById('userInput').addEventListener('input', function() {
  this.style.height = 'auto';
  this.style.height = Math.min(this.scrollHeight, 90) + 'px';
});

init();
</script>
</body>
</html>
