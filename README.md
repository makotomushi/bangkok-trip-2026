[index.html](https://github.com/user-attachments/files/28799663/index.html)
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>バンコク・パタヤ 古着買付旅 2026</title>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@300;400;700;900&family=Sarabun:wght@300;600;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --gold:    #C9A84C;
      --red:     #C0392B;
      --teal:    #1A7E7A;
      --cream:   #FAF5E9;
      --ink:     #1C1C1C;
      --muted:   #6B6B6B;
      --border:  #E2D8C0;
      --white:   #FFFFFF;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      background: var(--cream);
      color: var(--ink);
      font-family: 'Noto Sans JP', sans-serif;
      font-size: 15px;
      line-height: 1.8;
    }

    /* ─── HERO ─────────────────────────────── */
    .hero {
      background: var(--ink);
      color: var(--white);
      padding: 60px 24px 50px;
      text-align: center;
      position: relative;
      overflow: hidden;
    }
    .hero::before {
      content: '';
      position: absolute;
      inset: 0;
      background:
        radial-gradient(ellipse 60% 40% at 80% 20%, rgba(201,168,76,0.18) 0%, transparent 70%),
        radial-gradient(ellipse 50% 60% at 20% 80%, rgba(26,126,122,0.15) 0%, transparent 70%);
    }
    .hero-label {
      font-family: 'Sarabun', sans-serif;
      font-size: 11px;
      font-weight: 600;
      letter-spacing: 0.25em;
      color: var(--gold);
      text-transform: uppercase;
      margin-bottom: 18px;
      position: relative;
    }
    .hero h1 {
      font-family: 'Sarabun', sans-serif;
      font-size: clamp(32px, 7vw, 64px);
      font-weight: 800;
      line-height: 1.1;
      letter-spacing: -0.01em;
      position: relative;
    }
    .hero h1 .line-th {
      display: block;
      color: var(--gold);
    }
    .hero h1 .line-jp {
      display: block;
      font-family: 'Noto Sans JP', sans-serif;
      font-weight: 900;
      font-size: clamp(20px, 4vw, 36px);
      color: var(--white);
      margin-top: 8px;
    }
    .hero-meta {
      margin-top: 28px;
      display: flex;
      justify-content: center;
      gap: 24px;
      flex-wrap: wrap;
      position: relative;
    }
    .hero-meta-item {
      text-align: center;
    }
    .hero-meta-item .label {
      font-size: 10px;
      letter-spacing: 0.15em;
      color: rgba(255,255,255,0.5);
      text-transform: uppercase;
    }
    .hero-meta-item .value {
      font-size: 13px;
      font-weight: 700;
      color: var(--white);
      margin-top: 2px;
    }
    .hero-ornament {
      margin-top: 32px;
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 12px;
    }
    .hero-ornament::before,
    .hero-ornament::after {
      content: '';
      flex: 1;
      max-width: 80px;
      height: 1px;
      background: linear-gradient(to right, transparent, var(--gold));
    }
    .hero-ornament::after {
      background: linear-gradient(to left, transparent, var(--gold));
    }
    .hero-ornament span {
      color: var(--gold);
      font-size: 18px;
    }

    /* ─── FLIGHT CARD ───────────────────────── */
    .flight-card {
      max-width: 680px;
      margin: 40px auto 0;
      padding: 0 20px;
    }
    .flight-box {
      background: var(--white);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 24px 28px;
      display: grid;
      grid-template-columns: 1fr auto 1fr;
      align-items: center;
      gap: 16px;
    }
    .flight-end { text-align: left; }
    .flight-end.right { text-align: right; }
    .flight-end .airport {
      font-family: 'Sarabun', sans-serif;
      font-size: 28px;
      font-weight: 800;
      color: var(--ink);
      letter-spacing: -0.02em;
    }
    .flight-end .city {
      font-size: 11px;
      color: var(--muted);
      letter-spacing: 0.08em;
    }
    .flight-end .time {
      font-family: 'Sarabun', sans-serif;
      font-size: 18px;
      font-weight: 600;
      color: var(--teal);
      margin-top: 4px;
    }
    .flight-end .date-str {
      font-size: 11px;
      color: var(--muted);
    }
    .flight-mid {
      text-align: center;
    }
    .flight-mid .airline {
      font-size: 11px;
      color: var(--muted);
      letter-spacing: 0.1em;
    }
    .flight-mid .arrow {
      font-size: 22px;
      color: var(--gold);
      margin: 4px 0;
    }
    .flight-mid .code {
      font-family: 'Sarabun', sans-serif;
      font-size: 13px;
      font-weight: 700;
      color: var(--ink);
      background: var(--cream);
      padding: 2px 8px;
      border-radius: 4px;
      letter-spacing: 0.08em;
    }
    .flight-return {
      background: var(--teal);
      color: var(--white);
      border-color: var(--teal);
      margin-top: 10px;
    }
    .flight-return .flight-end .airport,
    .flight-return .flight-end .time { color: var(--white); }
    .flight-return .flight-end .city,
    .flight-return .flight-end .date-str { color: rgba(255,255,255,0.65); }
    .flight-return .flight-mid .airline { color: rgba(255,255,255,0.65); }
    .flight-return .flight-mid .code {
      background: rgba(255,255,255,0.15);
      color: var(--white);
    }
    .flight-return .flight-mid .arrow { color: var(--gold); }

    /* ─── SECTION HEADER ────────────────────── */
    .section-header {
      max-width: 680px;
      margin: 52px auto 0;
      padding: 0 20px;
    }
    .section-header h2 {
      font-family: 'Sarabun', sans-serif;
      font-size: 11px;
      font-weight: 600;
      letter-spacing: 0.25em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 4px;
    }
    .section-header p {
      font-size: 22px;
      font-weight: 700;
      color: var(--ink);
    }

    /* ─── ITINERARY ─────────────────────────── */
    .days {
      max-width: 680px;
      margin: 24px auto 0;
      padding: 0 20px;
      display: flex;
      flex-direction: column;
      gap: 16px;
    }

    .day-card {
      background: var(--white);
      border: 1px solid var(--border);
      border-radius: 12px;
      overflow: hidden;
    }
    .day-header {
      display: flex;
      align-items: stretch;
      background: var(--ink);
      color: var(--white);
    }
    .day-num {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      background: var(--gold);
      color: var(--ink);
      padding: 14px 18px;
      min-width: 64px;
    }
    .day-num .n {
      font-family: 'Sarabun', sans-serif;
      font-size: 28px;
      font-weight: 800;
      line-height: 1;
    }
    .day-num .label {
      font-size: 9px;
      font-weight: 700;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      margin-top: 2px;
    }
    .day-title-block {
      padding: 14px 20px;
      flex: 1;
    }
    .day-title-block .date {
      font-size: 11px;
      color: rgba(255,255,255,0.55);
      letter-spacing: 0.08em;
    }
    .day-title-block .title {
      font-size: 16px;
      font-weight: 700;
      color: var(--white);
      margin-top: 2px;
    }
    .day-title-block .tag {
      display: inline-block;
      font-size: 10px;
      padding: 2px 8px;
      border-radius: 20px;
      margin-top: 6px;
      font-weight: 600;
      letter-spacing: 0.05em;
    }
    .tag-beach   { background: rgba(26,126,122,0.25); color: #5ECECA; }
    .tag-shop    { background: rgba(201,168,76,0.25);  color: var(--gold); }
    .tag-food    { background: rgba(192,57,43,0.25);   color: #F1948A; }
    .tag-travel  { background: rgba(255,255,255,0.1);  color: rgba(255,255,255,0.6); }

    .day-body {
      padding: 20px 24px;
    }
    .timeline {
      list-style: none;
      position: relative;
    }
    .timeline::before {
      content: '';
      position: absolute;
      left: 6px;
      top: 8px;
      bottom: 8px;
      width: 1px;
      background: var(--border);
    }
    .timeline li {
      padding-left: 24px;
      padding-bottom: 14px;
      position: relative;
    }
    .timeline li:last-child { padding-bottom: 0; }
    .timeline li::before {
      content: '';
      position: absolute;
      left: 2px;
      top: 8px;
      width: 9px;
      height: 9px;
      border-radius: 50%;
      background: var(--border);
      border: 2px solid var(--white);
    }
    .timeline li.highlight::before { background: var(--gold); }
    .timeline li.teal-dot::before  { background: var(--teal); }
    .timeline li.red-dot::before   { background: var(--red); }

    .tl-time {
      font-size: 11px;
      font-weight: 700;
      color: var(--gold);
      letter-spacing: 0.08em;
      font-family: 'Sarabun', sans-serif;
    }
    .tl-text {
      font-size: 14px;
      color: var(--ink);
      line-height: 1.6;
    }
    .tl-note {
      font-size: 12px;
      color: var(--muted);
      margin-top: 2px;
    }

    /* ─── INFO BOX ──────────────────────────── */
    .info-grid {
      max-width: 680px;
      margin: 40px auto 0;
      padding: 0 20px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
    }
    @media (max-width: 520px) { .info-grid { grid-template-columns: 1fr; } }

    .info-box {
      background: var(--white);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 18px 20px;
    }
    .info-box .ib-label {
      font-size: 10px;
      font-weight: 700;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 10px;
    }
    .info-box ul {
      list-style: none;
    }
    .info-box ul li {
      font-size: 13px;
      color: var(--ink);
      padding: 5px 0;
      border-bottom: 1px solid var(--border);
      display: flex;
      gap: 8px;
    }
    .info-box ul li:last-child { border-bottom: none; }
    .info-box ul li .ico { font-size: 14px; flex-shrink: 0; }

    /* ─── FOOTER ─────────────────────────────── */
    footer {
      text-align: center;
      padding: 48px 20px 60px;
      color: var(--muted);
      font-size: 12px;
    }
    footer .ornament {
      font-size: 20px;
      margin-bottom: 10px;
      color: var(--gold);
    }

    /* ─── RESPONSIVE ────────────────────────── */
    @media (max-width: 520px) {
      .flight-box { grid-template-columns: 1fr auto 1fr; gap: 8px; padding: 18px 16px; }
      .flight-end .airport { font-size: 22px; }
      .day-title-block .title { font-size: 14px; }
    }
  </style>
</head>
<body>

<!-- HERO -->
<section class="hero">
  <p class="hero-label">Travel Booklet · July 2026</p>
  <h1>
    <span class="line-th">Bangkok × Pattaya</span>
    <span class="line-jp">古着買付＆南国リゾート旅</span>
  </h1>
  <div class="hero-meta">
    <div class="hero-meta-item">
      <div class="label">メンバー</div>
      <div class="value">まーちゃん・山田さん</div>
    </div>
    <div class="hero-meta-item">
      <div class="label">期間</div>
      <div class="value">7月23日(木) → 7月29日(水)</div>
    </div>
    <div class="hero-meta-item">
      <div class="label">エリア</div>
      <div class="value">パタヤ → バンコク</div>
    </div>
  </div>
  <div class="hero-ornament"><span>✦</span></div>
</section>

<!-- FLIGHTS -->
<div class="flight-card">
  <!-- 往路 -->
  <div class="flight-box">
    <div class="flight-end">
      <div class="airport">KIX</div>
      <div class="city">関西国際空港</div>
      <div class="time">19:45</div>
      <div class="date-str">7月23日(木)</div>
    </div>
    <div class="flight-mid">
      <div class="airline">Peach Aviation</div>
      <div class="arrow">→</div>
      <div class="code">N6SWX6</div>
    </div>
    <div class="flight-end right">
      <div class="airport">BKK</div>
      <div class="city">スワンナプーム空港</div>
      <div class="time">23:55</div>
      <div class="date-str">7月23日(木)</div>
    </div>
  </div>
  <!-- 復路 -->
  <div class="flight-box flight-return">
    <div class="flight-end">
      <div class="airport">BKK</div>
      <div class="city">スワンナプーム空港</div>
      <div class="time">23:59</div>
      <div class="date-str">7月29日(水)</div>
    </div>
    <div class="flight-mid">
      <div class="airline">Thai Airways</div>
      <div class="arrow">→</div>
      <div class="code">TG622</div>
    </div>
    <div class="flight-end right">
      <div class="airport">KIX</div>
      <div class="city">関西国際空港</div>
      <div class="time">07:30</div>
      <div class="date-str">7月30日(木)</div>
    </div>
  </div>
</div>

<!-- ITINERARY HEADER -->
<div class="section-header">
  <h2>Itinerary</h2>
  <p>7日間の旅程</p>
</div>

<!-- DAYS -->
<div class="days">

  <!-- Day 1 -->
  <div class="day-card">
    <div class="day-header">
      <div class="day-num"><span class="n">1</span><span class="label">DAY</span></div>
      <div class="day-title-block">
        <div class="date">7月23日(木)</div>
        <div class="title">深夜フライト → パタヤへ</div>
        <span class="tag tag-travel">移動日</span>
      </div>
    </div>
    <div class="day-body">
      <ul class="timeline">
        <li class="highlight">
          <div class="tl-time">19:45</div>
          <div class="tl-text">関西空港 出発（Peach N6SWX6）</div>
        </li>
        <li class="highlight">
          <div class="tl-time">23:55</div>
          <div class="tl-text">スワンナプーム空港 到着</div>
        </li>
        <li>
          <div class="tl-time">深夜</div>
          <div class="tl-text">空港からタクシーでパタヤへ移動</div>
          <div class="tl-note">所要約2時間。Grab タクシーが割安でおすすめ</div>
        </li>
        <li>
          <div class="tl-text">パタヤ宿泊</div>
        </li>
      </ul>
    </div>
  </div>

  <!-- Day 2 -->
  <div class="day-card">
    <div class="day-header">
      <div class="day-num"><span class="n">2</span><span class="label">DAY</span></div>
      <div class="day-title-block">
        <div class="date">7月24日(金)</div>
        <div class="title">ラン島 海と島遊び</div>
        <span class="tag tag-beach">ビーチ</span>
      </div>
    </div>
    <div class="day-body">
      <ul class="timeline">
        <li class="teal-dot">
          <div class="tl-time">09:00</div>
          <div class="tl-text">ラン島へ渡る（フェリー）</div>
          <div class="tl-note">パタヤビーチ桟橋から約30分</div>
        </li>
        <li>
          <div class="tl-text">バイクを借りて島を一周散策</div>
          <div class="tl-note">レンタル目安 300〜500バーツ/台</div>
        </li>
        <li class="highlight">
          <div class="tl-text">海沿いのカフェでランチ</div>
        </li>
        <li>
          <div class="tl-text">ビーチでのんびり＆マリンアクティビティ</div>
          <div class="tl-note">シュノーケル・バナナボートなど</div>
        </li>
        <li class="teal-dot">
          <div class="tl-time">16:00</div>
          <div class="tl-text">パタヤへ戻る</div>
        </li>
        <li>
          <div class="tl-text">タイマッサージで疲れを癒す</div>
        </li>
        <li class="highlight">
          <div class="tl-text">夕食：ステーキ or シーフード</div>
        </li>
        <li class="red-dot">
          <div class="tl-text">夜：GoGoバーでナイトライフ</div>
        </li>
      </ul>
    </div>
  </div>

  <!-- Day 3 -->
  <div class="day-card">
    <div class="day-header">
      <div class="day-num"><span class="n">3</span><span class="label">DAY</span></div>
      <div class="day-title-block">
        <div class="date">7月25日(土)</div>
        <div class="title">バンコク移動 → チャトチャック古着買付</div>
        <span class="tag tag-shop">買付</span>
      </div>
    </div>
    <div class="day-body">
      <ul class="timeline">
        <li>
          <div class="tl-text">パタヤ → バンコク移動</div>
          <div class="tl-note">バス or Grab で約2〜2.5時間</div>
        </li>
        <li class="highlight">
          <div class="tl-text">午後：チャトチャック市場 古着買付</div>
          <div class="tl-note">土曜はチャトチャック全面オープン！バンスー周辺も回る</div>
        </li>
        <li class="highlight">
          <div class="tl-text">夕食：プーパッポンカレー</div>
          <div class="tl-note">ソンブーン・シーフードなど</div>
        </li>
        <li class="red-dot">
          <div class="tl-text">夜：タニヤでカラオケ</div>
        </li>
        <li>
          <div class="tl-text">Fusion ホテル 宿泊</div>
        </li>
      </ul>
    </div>
  </div>

  <!-- Day 4 -->
  <div class="day-card">
    <div class="day-header">
      <div class="day-num"><span class="n">4</span><span class="label">DAY</span></div>
      <div class="day-title-block">
        <div class="date">7月26日(日)</div>
        <div class="title">カオマンガイ朝食 → マーケット</div>
        <span class="tag tag-food">グルメ</span>
      </div>
    </div>
    <div class="day-body">
      <ul class="timeline">
        <li class="highlight">
          <div class="tl-text">朝食：カオマンガイの名店</div>
          <div class="tl-note">Kaiton Pratunam など</div>
        </li>
        <li>
          <div class="tl-text">チャトチャック（土曜に行けなかった場合）</div>
          <div class="tl-note">※日曜も開場。行けた場合は別のマーケットへ</div>
        </li>
        <li class="teal-dot">
          <div class="tl-text">シーナカリン・ロッファイ・マーケット</div>
          <div class="tl-note">夕方〜夜オープンのヴィンテージ&古着天国</div>
        </li>
        <li>
          <div class="tl-text">サウナ or タイマッサージ</div>
        </li>
      </ul>
    </div>
  </div>

  <!-- Day 5 -->
  <div class="day-card">
    <div class="day-header">
      <div class="day-num"><span class="n">5</span><span class="label">DAY</span></div>
      <div class="day-title-block">
        <div class="date">7月27日(月)</div>
        <div class="title">倉庫買付 ＋ 山田さん帰国</div>
        <span class="tag tag-shop">買付</span>
      </div>
    </div>
    <div class="day-body">
      <ul class="timeline">
        <li class="highlight">
          <div class="tl-text">倉庫への古着買付</div>
        </li>
        <li>
          <div class="tl-text">夕方：タイマッサージ</div>
        </li>
        <li class="highlight">
          <div class="tl-text">夕食：ガパオライス</div>
        </li>
        <li class="red-dot">
          <div class="tl-text">山田さん 帰国</div>
          <div class="tl-note">お疲れさまでした！</div>
        </li>
      </ul>
    </div>
  </div>

  <!-- Day 6 -->
  <div class="day-card">
    <div class="day-header">
      <div class="day-num"><span class="n">6</span><span class="label">DAY</span></div>
      <div class="day-title-block">
        <div class="date">7月28日(火)</div>
        <div class="title">倉庫買付 つづき（まーちゃん solo）</div>
        <span class="tag tag-shop">買付</span>
      </div>
    </div>
    <div class="day-body">
      <ul class="timeline">
        <li class="highlight">
          <div class="tl-text">倉庫への古着買付（ソロ）</div>
        </li>
        <li>
          <div class="tl-text">自由行動・街ぶら</div>
        </li>
      </ul>
    </div>
  </div>

  <!-- Day 7 -->
  <div class="day-card">
    <div class="day-header">
      <div class="day-num"><span class="n">7</span><span class="label">DAY</span></div>
      <div class="day-title-block">
        <div class="date">7月29日(水)</div>
        <div class="title">古着屋巡り → 深夜帰国フライト</div>
        <span class="tag tag-travel">帰国日</span>
      </div>
    </div>
    <div class="day-body">
      <ul class="timeline">
        <li class="highlight">
          <div class="tl-text">バンコク市内の古着屋を巡る</div>
          <div class="tl-note">最後の仕入れチャンス！</div>
        </li>
        <li>
          <div class="tl-text">荷物まとめ・空港へ移動</div>
          <div class="tl-note">スワンナプームへは余裕を持って出発</div>
        </li>
        <li class="teal-dot">
          <div class="tl-time">23:59</div>
          <div class="tl-text">スワンナプーム空港 出発（TG622 タイ航空）</div>
        </li>
        <li class="highlight">
          <div class="tl-time">07:30+1</div>
          <div class="tl-text">関西国際空港 到着</div>
          <div class="tl-note">7月30日(木) 到着</div>
        </li>
      </ul>
    </div>
  </div>

</div>

<!-- INFO GRID -->
<div class="section-header">
  <h2>Essentials</h2>
  <p>持ち物・メモ</p>
</div>

<div class="info-grid">
  <div class="info-box">
    <div class="ib-label">持ち物チェック</div>
    <ul>
      <li><span class="ico">🛂</span> パスポート（有効期限確認）</li>
      <li><span class="ico">💳</span> クレジットカード・現金</li>
      <li><span class="ico">🩴</span> ビーチサンダル・水着</li>
      <li><span class="ico">👕</span> 買付用の大きいバッグ・ダンボール</li>
      <li><span class="ico">💊</span> 常備薬・整腸剤</li>
      <li><span class="ico">🌡️</span> 日焼け止め（SPF50以上）</li>
      <li><span class="ico">🔌</span> 変換プラグ（タイはA・B・Cタイプ）</li>
    </ul>
  </div>
  <div class="info-box">
    <div class="ib-label">現地メモ</div>
    <ul>
      <li><span class="ico">🇹🇭</span> 通貨：タイバーツ（THB）</li>
      <li><span class="ico">📱</span> Grab アプリ必須（移動・フード）</li>
      <li><span class="ico">💧</span> 水道水は飲まない。ペットボトルで</li>
      <li><span class="ico">🌡️</span> 気温 34℃前後。熱中症に注意</li>
      <li><span class="ico">🦟</span> 虫除けスプレー持参</li>
      <li><span class="ico">👗</span> 寺院訪問時は肌を隠す服装を</li>
      <li><span class="ico">🕐</span> 日本との時差：-2時間</li>
    </ul>
  </div>
</div>

<footer>
  <div class="ornament">✦</div>
  <p>Bangkok × Pattaya 古着買付旅 2026</p>
  <p style="margin-top:4px; color:#aaa;">Have a great trip! 🐘</p>
</footer>

</body>
</html>
