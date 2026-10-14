# Halloween-<!DOCTYPE html>
<html lang="zh-Hant-TW">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>🎃 萬聖探奇・閱界思行 | 跨領域四節課主題學習平台</title>
  <!-- Google Fonts: Outfit, Plus Jakarta Sans, Noto Sans TC -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@400;500;700;900&family=Outfit:wght@500;700;900&family=Plus+Jakarta+Sans:wght@500;700;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg-dark: #0a0a14;
      --bg-card: rgba(23, 17, 39, 0.75);
      --bg-card-hover: rgba(35, 26, 60, 0.85);
      --border-color: rgba(255, 117, 24, 0.25);
      --border-glow: rgba(255, 117, 24, 0.5);
      --primary-orange: #ff7518;
      --accent-purple: #9d4edd;
      --accent-green: #39ff14;
      --accent-cyan: #00f0ff;
      --accent-gold: #ffb703;
      --text-light: #f8fafc;
      --text-muted: #94a3b8;
      --radius-sm: 8px;
      --radius-md: 14px;
      --radius-lg: 22px;
      --shadow-glow: 0 8px 32px 0 rgba(255, 117, 24, 0.18);
      --font-display: 'Outfit', 'Noto Sans TC', sans-serif;
      --font-body: 'Plus Jakarta Sans', 'Noto Sans TC', sans-serif;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      -webkit-font-smoothing: antialiased;
    }

    body {
      background-color: var(--bg-dark);
      background-image: 
        radial-gradient(circle at 10% 20%, rgba(157, 78, 221, 0.15) 0%, transparent 40%),
        radial-gradient(circle at 90% 80%, rgba(255, 117, 24, 0.12) 0%, transparent 40%),
        radial-gradient(circle at 50% 50%, rgba(0, 240, 255, 0.05) 0%, transparent 60%);
      background-attachment: fixed;
      color: var(--text-light);
      font-family: var(--font-body);
      line-height: 1.6;
      min-height: 100vh;
      overflow-x: hidden;
    }

    /* 頂部導覽列 */
    header.main-header {
      position: sticky;
      top: 0;
      z-index: 1000;
      background: rgba(10, 10, 20, 0.88);
      backdrop-filter: blur(16px);
      border-bottom: 1px solid rgba(255, 255, 255, 0.08);
      padding: 0.75rem 1.5rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 1rem;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 0.75rem;
      text-decoration: none;
      color: var(--text-light);
    }

    .brand-icon {
      font-size: 2rem;
      filter: drop-shadow(0 0 10px rgba(255, 117, 24, 0.7));
      animation: float-pulse 3s ease-in-out infinite alternate;
    }

    @keyframes float-pulse {
      0% { transform: translateY(0) scale(1); }
      100% { transform: translateY(-3px) scale(1.08); }
    }

    .brand-text h1 {
      font-family: var(--font-display);
      font-size: 1.25rem;
      font-weight: 900;
      letter-spacing: -0.02em;
      background: linear-gradient(135deg, #ff7518 0%, #ffb703 50%, #f72585 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .brand-text p {
      font-size: 0.75rem;
      color: var(--text-muted);
    }

    /* 頂部控制按鈕區 */
    .header-actions {
      display: flex;
      align-items: center;
      gap: 0.6rem;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      padding: 0.5rem 1rem;
      border-radius: var(--radius-sm);
      font-size: 0.85rem;
      font-weight: 700;
      cursor: pointer;
      transition: all 0.25s ease;
      border: 1px solid transparent;
      outline: none;
      text-decoration: none;
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--primary-orange) 0%, #e85d04 100%);
      color: #fff;
      box-shadow: 0 4px 14px rgba(255, 117, 24, 0.35);
    }
    .btn-primary:hover {
      box-shadow: 0 6px 20px rgba(255, 117, 24, 0.55);
      transform: translateY(-1px);
    }

    .btn-outline {
      background: rgba(255, 255, 255, 0.05);
      border-color: rgba(255, 255, 255, 0.15);
      color: var(--text-light);
    }
    .btn-outline:hover {
      background: rgba(255, 255, 255, 0.12);
      border-color: var(--accent-purple);
    }

    .btn-mode-toggle {
      background: rgba(157, 78, 221, 0.2);
      border-color: var(--accent-purple);
      color: #e0aaff;
    }
    .btn-mode-toggle:hover {
      background: rgba(157, 78, 221, 0.35);
    }

    /* 導覽分頁條 */
    .nav-tabs-wrapper {
      max-width: 1280px;
      margin: 1rem auto 0;
      padding: 0 1rem;
    }

    .nav-tabs {
      display: flex;
      gap: 0.5rem;
      overflow-x: auto;
      padding-bottom: 0.5rem;
      scrollbar-width: thin;
    }

    .nav-tab-btn {
      flex: 1;
      min-width: 180px;
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid rgba(255, 255, 255, 0.08);
      color: var(--text-muted);
      padding: 0.85rem 1rem;
      border-radius: var(--radius-md);
      font-size: 0.88rem;
      font-weight: 700;
      cursor: pointer;
      display: flex;
      flex-direction: column;
      gap: 0.2rem;
      align-items: flex-start;
      transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);
    }

    .nav-tab-btn span.badge {
      font-size: 0.7rem;
      padding: 0.15rem 0.5rem;
      border-radius: 20px;
      background: rgba(255, 255, 255, 0.08);
      color: var(--text-light);
    }

    .nav-tab-btn:hover {
      background: rgba(255, 117, 24, 0.08);
      border-color: rgba(255, 117, 24, 0.3);
      color: var(--text-light);
    }

    .nav-tab-btn.active {
      background: linear-gradient(135deg, rgba(255, 117, 24, 0.2) 0%, rgba(157, 78, 221, 0.15) 100%);
      border-color: var(--primary-orange);
      color: #fff;
      box-shadow: 0 4px 20px rgba(255, 117, 24, 0.2);
    }

    .nav-tab-btn.active span.badge {
      background: var(--primary-orange);
      color: #000;
      font-weight: 800;
    }

    /* 主要容器 */
    main.container {
      max-width: 1280px;
      margin: 1.5rem auto 4rem;
      padding: 0 1rem;
    }

    /* 模組卡片樣式 */
    .module-card {
      background: var(--bg-card);
      backdrop-filter: blur(20px);
      border: 1px solid var(--border-color);
      border-radius: var(--radius-lg);
      padding: 2rem;
      margin-bottom: 2rem;
      box-shadow: var(--shadow-glow);
      position: relative;
      overflow: hidden;
    }

    .module-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 1rem;
      margin-bottom: 1.75rem;
      border-bottom: 1px solid rgba(255, 255, 255, 0.08);
      padding-bottom: 1.25rem;
    }

    .module-title-area h2 {
      font-family: var(--font-display);
      font-size: 1.6rem;
      font-weight: 900;
      display: flex;
      align-items: center;
      gap: 0.6rem;
      color: #fff;
    }

    .module-title-area p {
      color: var(--text-muted);
      font-size: 0.95rem;
      margin-top: 0.3rem;
    }

    .status-pill {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      padding: 0.35rem 0.85rem;
      border-radius: 30px;
      font-size: 0.78rem;
      font-weight: 700;
      background: rgba(57, 255, 20, 0.12);
      border: 1px solid rgba(57, 255, 20, 0.35);
      color: #84ff6b;
      white-space: nowrap;
    }

    /* 任務區塊 */
    .task-section {
      background: rgba(10, 10, 20, 0.6);
      border: 1px solid rgba(255, 255, 255, 0.06);
      border-radius: var(--radius-md);
      padding: 1.5rem;
      margin-bottom: 1.5rem;
      transition: border-color 0.25s ease;
    }

    .task-section:hover {
      border-color: rgba(255, 117, 24, 0.35);
    }

    .task-tag {
      display: inline-block;
      font-size: 0.75rem;
      font-weight: 800;
      text-transform: uppercase;
      padding: 0.25rem 0.65rem;
      border-radius: 6px;
      margin-bottom: 0.75rem;
      letter-spacing: 0.04em;
    }

    .tag-orange { background: rgba(255, 117, 24, 0.2); color: #ffa94d; border: 1px solid rgba(255, 117, 24, 0.4); }
    .tag-purple { background: rgba(157, 78, 221, 0.2); color: #d8b4fe; border: 1px solid rgba(157, 78, 221, 0.4); }
    .tag-cyan { background: rgba(0, 240, 255, 0.15); color: #67e8f9; border: 1px solid rgba(0, 240, 255, 0.4); }
    .tag-green { background: rgba(57, 255, 20, 0.15); color: #86efac; border: 1px solid rgba(57, 255, 20, 0.4); }

    .task-title {
      font-size: 1.25rem;
      font-weight: 800;
      margin-bottom: 0.75rem;
      color: #fff;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    /* 互動填空與反思輸入框 */
    .fill-in-container {
      background: rgba(255, 255, 255, 0.03);
      border-left: 4px solid var(--primary-orange);
      padding: 1.25rem;
      border-radius: 0 var(--radius-sm) var(--radius-sm) 0;
      margin-top: 1rem;
      font-size: 1.05rem;
      line-height: 1.8;
    }

    .inline-blank {
      display: inline-block;
      min-width: 110px;
      background: rgba(255, 117, 24, 0.15);
      border-bottom: 2px dashed var(--primary-orange);
      color: #fff;
      padding: 0.2rem 0.5rem;
      font-weight: 700;
      border-radius: 4px;
      cursor: pointer;
      text-align: center;
      transition: all 0.2s ease;
    }
    .inline-blank:hover {
      background: rgba(255, 117, 24, 0.3);
      border-bottom-style: solid;
    }
    .inline-blank.revealed {
      background: rgba(57, 255, 20, 0.2);
      border-bottom-color: var(--accent-green);
      color: #84ff6b;
    }

    /* 對照表格設計 */
    .comparison-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1.25rem;
      margin-top: 1rem;
    }

    @media (max-width: 768px) {
      .comparison-grid {
        grid-template-columns: 1fr;
      }
    }

    .comp-card {
      background: rgba(20, 15, 35, 0.85);
      border-radius: var(--radius-md);
      padding: 1.5rem;
      border: 1px solid rgba(255, 255, 255, 0.08);
      position: relative;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }
    .comp-card:hover {
      transform: translateY(-3px);
      box-shadow: 0 8px 24px rgba(0, 0, 0, 0.4);
    }
    .comp-card.western { border-top: 4px solid var(--primary-orange); }
    .comp-card.eastern { border-top: 4px solid var(--accent-gold); }

    .comp-card h4 {
      font-size: 1.15rem;
      font-weight: 800;
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .comp-item {
      margin-bottom: 0.85rem;
      padding-bottom: 0.85rem;
      border-bottom: 1px dashed rgba(255, 255, 255, 0.08);
    }
    .comp-item:last-child {
      border-bottom: none;
      margin-bottom: 0;
      padding-bottom: 0;
    }
    .comp-label {
      font-size: 0.78rem;
      color: var(--text-muted);
      text-transform: uppercase;
      letter-spacing: 0.05em;
      margin-bottom: 0.2rem;
    }
    .comp-value {
      font-size: 0.95rem;
      color: #fff;
      font-weight: 600;
    }

    /* OPAC 檢索模擬器 */
    .opac-box {
      display: flex;
      gap: 0.75rem;
      margin-bottom: 1.25rem;
      flex-wrap: wrap;
    }
    .opac-input {
      flex: 1;
      min-width: 250px;
      background: rgba(0, 0, 0, 0.4);
      border: 1px solid rgba(255, 255, 255, 0.15);
      color: #fff;
      padding: 0.75rem 1rem;
      border-radius: var(--radius-sm);
      font-size: 0.95rem;
    }
    .opac-input:focus {
      outline: none;
      border-color: var(--primary-orange);
      box-shadow: 0 0 10px rgba(255, 117, 24, 0.3);
    }
    .quick-tags {
      display: flex;
      gap: 0.5rem;
      flex-wrap: wrap;
      margin-bottom: 1rem;
      align-items: center;
    }
    .quick-btn {
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255, 255, 255, 0.1);
      color: var(--text-muted);
      padding: 0.3rem 0.7rem;
      border-radius: 20px;
      font-size: 0.78rem;
      cursor: pointer;
      transition: all 0.2s;
    }
    .quick-btn:hover {
      background: rgba(255, 117, 24, 0.2);
      color: #fff;
      border-color: var(--primary-orange);
    }

    .books-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 1rem;
      margin-top: 1rem;
    }
    .book-card {
      background: rgba(15, 12, 28, 0.85);
      border: 1px solid rgba(255, 255, 255, 0.08);
      border-radius: var(--radius-md);
      padding: 1.25rem;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      transition: all 0.25s;
    }
    .book-card:hover {
      border-color: var(--accent-cyan);
      box-shadow: 0 6px 20px rgba(0, 240, 255, 0.15);
      transform: translateY(-2px);
    }
    .book-title {
      font-size: 1.05rem;
      font-weight: 800;
      color: #fff;
      margin-bottom: 0.4rem;
    }
    .book-meta {
      font-size: 0.8rem;
      color: var(--text-muted);
      margin-bottom: 0.6rem;
    }
    .call-number-badge {
      display: inline-block;
      background: rgba(0, 240, 255, 0.12);
      border: 1px solid rgba(0, 240, 255, 0.35);
      color: var(--accent-cyan);
      padding: 0.2rem 0.5rem;
      border-radius: 4px;
      font-family: monospace;
      font-weight: bold;
      font-size: 0.85rem;
      margin-top: 0.4rem;
    }

    /* 三站輪換學習卡 */
    .station-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1.25rem;
      margin-top: 1rem;
    }
    @media (max-width: 900px) {
      .station-grid { grid-template-columns: 1fr; }
    }
    .station-card {
      background: rgba(22, 17, 38, 0.9);
      border: 1px solid rgba(255, 255, 255, 0.08);
      border-radius: var(--radius-md);
      padding: 1.5rem;
      position: relative;
    }
    .station-badge {
      position: absolute;
      top: 1rem;
      right: 1rem;
      background: var(--accent-purple);
      color: #fff;
      font-size: 0.72rem;
      font-weight: 800;
      padding: 0.2rem 0.6rem;
      border-radius: 20px;
    }

    /* 單字點擊發音卡片 */
    .vocab-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(130px, 1fr));
      gap: 0.75rem;
      margin-top: 1rem;
    }
    .vocab-card {
      background: rgba(255, 255, 255, 0.04);
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: var(--radius-sm);
      padding: 0.85rem 0.5rem;
      text-align: center;
      cursor: pointer;
      transition: all 0.2s;
    }
    .vocab-card:hover {
      background: rgba(255, 117, 24, 0.2);
      border-color: var(--primary-orange);
      transform: scale(1.05);
    }
    .vocab-icon { font-size: 1.8rem; margin-bottom: 0.3rem; }
    .vocab-word { font-weight: 800; font-size: 0.95rem; color: #fff; }
    .vocab-zh { font-size: 0.75rem; color: var(--text-muted); }

    /* AI 互動對話模擬器 */
    .ai-chat-box {
      background: #0d0b1a;
      border: 1px solid rgba(157, 78, 221, 0.3);
      border-radius: var(--radius-md);
      padding: 1rem;
      margin-top: 1rem;
    }
    .ai-chat-messages {
      height: 180px;
      overflow-y: auto;
      display: flex;
      flex-direction: column;
      gap: 0.6rem;
      margin-bottom: 0.75rem;
      padding-right: 0.4rem;
    }
    .chat-bubble {
      max-width: 80%;
      padding: 0.6rem 0.9rem;
      border-radius: 12px;
      font-size: 0.88rem;
    }
    .bubble-ai {
      background: rgba(157, 78, 221, 0.25);
      border: 1px solid rgba(157, 78, 221, 0.4);
      color: #f1e4ff;
      align-self: flex-start;
    }
    .bubble-user {
      background: rgba(255, 117, 24, 0.25);
      border: 1px solid rgba(255, 117, 24, 0.4);
      color: #fff;
      align-self: flex-end;
    }
    .chat-input-row {
      display: flex;
      gap: 0.5rem;
    }

    /* Kahoot! 互動挑戰器 */
    .kahoot-box {
      background: linear-gradient(145deg, #181335 0%, #0d0a21 100%);
      border: 2px solid var(--accent-purple);
      border-radius: var(--radius-md);
      padding: 1.5rem;
      margin-top: 1rem;
    }
    .kahoot-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 1rem;
    }
    .kahoot-q-text {
      font-size: 1.15rem;
      font-weight: 800;
      color: #fff;
      margin-bottom: 1.25rem;
      min-height: 48px;
    }
    .kahoot-answers {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 0.75rem;
    }
    @media (max-width: 600px) {
      .kahoot-answers { grid-template-columns: 1fr; }
    }
    .kahoot-btn {
      padding: 1rem;
      border-radius: 8px;
      border: none;
      font-weight: 800;
      font-size: 0.95rem;
      color: #fff;
      cursor: pointer;
      text-align: left;
      display: flex;
      align-items: center;
      gap: 0.6rem;
      transition: transform 0.15s, opacity 0.2s;
    }
    .kahoot-btn:hover { transform: scale(1.02); opacity: 0.9; }
    .k-red { background: #e21b3c; }
    .k-blue { background: #1368ce; }
    .k-yellow { background: #d89e00; }
    .k-green { background: #26890c; }

    /* SRL 星星評分元件 */
    .star-rating {
      display: inline-flex;
      gap: 0.35rem;
      cursor: pointer;
      font-size: 1.5rem;
      color: #4b5563;
    }
    .star-rating .star.active {
      color: var(--accent-gold);
      text-shadow: 0 0 10px rgba(255, 183, 3, 0.6);
    }

    /* 學生筆記書寫 textarea */
    .student-textarea {
      width: 100%;
      min-height: 90px;
      background: rgba(0, 0, 0, 0.35);
      border: 1px solid rgba(255, 255, 255, 0.15);
      border-radius: var(--radius-sm);
      color: #fff;
      padding: 0.75rem;
      font-size: 0.92rem;
      font-family: inherit;
      resize: vertical;
      margin-top: 0.5rem;
    }
    .student-textarea:focus {
      outline: none;
      border-color: var(--primary-orange);
      box-shadow: 0 0 8px rgba(255, 117, 24, 0.3);
    }

    /* 列印特定樣式 */
    @media print {
      body {
        background: #fff !important;
        color: #000 !important;
      }
      header.main-header, .nav-tabs-wrapper, .btn-mode-toggle, .quick-tags, .opac-box, .ai-chat-box {
        display: none !important;
      }
      .module-card {
        background: #fff !important;
        border: 1px solid #ccc !important;
        box-shadow: none !important;
        color: #000 !important;
        page-break-inside: avoid;
        margin-bottom: 1.5cm;
      }
      .task-title, .module-title-area h2, .comp-card h4, .comp-value {
        color: #000 !important;
      }
      .comp-card {
        background: #f8fafc !important;
        border: 1px solid #ddd !important;
      }
    }
  </style>
</head>
<body>

  <!-- 頂部導覽列 -->
  <header class="main-header">
    <a href="#" class="brand">
      <div class="brand-icon">🎃</div>
      <div class="brand-text">
        <h1>萬聖探奇・閱界思行</h1>
        <p>國中跨領域四節課主題學習平台 (OPAC / 文化探秘 / AI美語 / 食安手作)</p>
      </div>
    </a>
    <div class="header-actions">
      <button class="btn btn-mode-toggle" id="modeToggleBtn" onclick="toggleTeacherStudentMode()">
        <span>👩‍🏫 教師教案模式</span>
      </button>
      <button class="btn btn-outline" onclick="window.print()">
        <span>🖨️ 列印導學單</span>
      </button>
      <button class="btn btn-primary" onclick="exportStudentData()">
        <span>💾 儲存學習歷程</span>
      </button>
    </div>
  </header>

  <!-- 課程分頁選單 -->
  <div class="nav-tabs-wrapper">
    <nav class="nav-tabs" id="lessonTabs">
      <button class="nav-tab-btn active" onclick="switchLessonTab(0)">
        <span class="badge">Lesson 1</span>
        <strong>第一節：OPAC 檢索與應用</strong>
      </button>
      <button class="nav-tab-btn" onclick="switchLessonTab(1)">
        <span class="badge">Lesson 2</span>
        <strong>第二節：東西方文化探秘</strong>
      </button>
      <button class="nav-tab-btn" onclick="switchLessonTab(2)">
        <span class="badge">Lesson 3</span>
        <strong>第三節：美語歌謠與 AI 互動</strong>
      </button>
      <button class="nav-tab-btn" onclick="switchLessonTab(3)">
        <span class="badge">Lesson 4</span>
        <strong>第四節：創意手作與食安反思</strong>
      </button>
    </nav>
  </div>

  <!-- 主要內容區 -->
  <main class="container">

    <!-- ==================== 第一節課：OPAC 搜尋和應用 ==================== -->
    <section class="module-card lesson-pane" id="lesson-pane-0">
      <div class="module-header">
        <div class="module-title-area">
          <h2>🔍 第一節：神「搜」鬼沒——圖書館 OPAC 檢索與民俗主題應用</h2>
          <p>掌握線上公用目錄檢索（OPAC）、布林關鍵字技巧、索書號（分類號＋著者號）解碼並定位實體館藏。</p>
        </div>
        <div class="status-pill">⏱️ 45 分鐘實作</div>
      </div>

      <!-- 任務一：OPAC 模擬器 -->
      <div class="task-section">
        <span class="task-tag tag-cyan">核心實作演練</span>
        <h3 class="task-title">🎯 任務：萬聖與民俗主題【圖書館尋寶獵人】</h3>
        <p style="color: var(--text-muted); font-size: 0.9rem; margin-bottom: 1rem;">
          在下方 OPAC 檢索框輸入關鍵字（例如：「萬聖節」、「薩溫節」、「中元節」、「食安」），即時查詢本校圖書館藏，並記錄索書號與架位。
        </p>

        <div class="quick-tags">
          <span style="font-size: 0.8rem; color: var(--text-muted);">熱門推薦關鍵字：</span>
          <button class="quick-btn" onclick="triggerSearch('萬聖節')">🎃 萬聖節</button>
          <button class="quick-btn" onclick="triggerSearch('薩溫節')">🔥 薩溫節</button>
          <button class="quick-btn" onclick="triggerSearch('中元節')">🏮 中元節</button>
          <button class="quick-btn" onclick="triggerSearch('食安')">🍬 健康食安</button>
          <button class="quick-btn" onclick="triggerSearch('神話')">⚡ 世界神話</button>
        </div>

        <div class="opac-box">
          <input type="text" class="opac-input" id="opacKeyword" placeholder="請輸入書名、作者、關鍵字或索書號..." oninput="handleOpacSearch()">
          <button class="btn btn-primary" onclick="handleOpacSearch()">🔍 檢索館藏</button>
        </div>

        <div class="books-grid" id="opacResults">
          <!-- 動態載入圖書結果 -->
        </div>

        <div class="fill-in-container" style="margin-top: 1.5rem;">
          <strong>📝 學生 OPAC 實作查核登記表：</strong>
          <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 0.75rem; margin-top: 0.5rem;">
            <input type="text" class="opac-input" id="student_book_name" placeholder="我找到的書名...">
            <input type="text" class="opac-input" id="student_call_number" placeholder="索書號 (例: 538.5 / 712)...">
          </div>
          <input type="text" class="opac-input" id="student_book_shelf" style="margin-top: 0.5rem;" placeholder="實體書架位置 (例: 1F 跨文化專區 SOC-02-B)...">
        </div>
      </div>

      <!-- 索書號解碼小教學 -->
      <div class="task-section">
        <span class="task-tag tag-purple">圖書資訊素養</span>
        <h3 class="task-title">💡 索書號（Call Number）大解密</h3>
        <p style="font-size: 0.95rem; line-height: 1.7;">
          索書號就像圖書的身分證字號！由「<strong>分類號</strong>」（代表知識類別，如 538 歲時風俗、200 宗教神話）與「<strong>著者號</strong>」（代表作者代碼）組成。看到 <code>538.5 / 712</code>，就能直奔圖書館 500 類民俗架區迅速找到它！
        </p>
      </div>
    </section>

    <!-- ==================== 第二節課：萬聖節起源與東西方文化探秘 ==================== -->
    <section class="module-card lesson-pane" id="lesson-pane-1" style="display: none;">
      <div class="module-header">
        <div class="module-title-area">
          <h2>🎃 第二節：萬聖節起源與東西方文化探秘（配合簡報一）</h2>
          <p>理解萬聖節歷史起源、文化符號涵義，並深入比較東西方鬼節文化之信仰背景與習慣。</p>
        </div>
        <div class="status-pill">⏱️ 45 分鐘探究</div>
      </div>

      <!-- 任務一：課前線上看與思考 -->
      <div class="task-section">
        <span class="task-tag tag-orange">任務一</span>
        <h3 class="task-title">🎬【課前線上看與思考】薩溫節與南瓜燈由來</h3>
        
        <div class="fill-in-container">
          <p style="margin-bottom: 0.75rem;">
            💡 <strong>觀點填空（點擊虛線挖空看正解）：</strong><br>
            萬聖節最早源自古凱爾特人的
            <span class="inline-blank" onclick="toggleBlank(this, '薩溫節（Samhain）')">［？點擊揭曉］</span>，
            象徵
            <span class="inline-blank" onclick="toggleBlank(this, '夏天的結束')">［？點擊揭曉］</span>
            與
            <span class="inline-blank" onclick="toggleBlank(this, '新年的開始')">［？點擊揭曉］</span>。
          </p>
          <p>
            🎃 <strong>傳說解析（點擊虛線挖空看正解）：</strong><br>
            『吝嗇傑克』（Stingy Jack）因為生前戲弄魔鬼，死後提著燈籠在黑夜漫遊。他最初是用
            <span class="inline-blank" onclick="toggleBlank(this, '蕪菁（大頭菜）')">［？點擊揭曉］</span>
            雕刻燈籠，傳到美國後才改用盛產的
            <span class="inline-blank" onclick="toggleBlank(this, '南瓜')">［？點擊揭曉］</span>。
          </p>
        </div>
      </div>

      <!-- 任務二：東西方鬼節文化比一比 -->
      <div class="task-section">
        <span class="task-tag tag-purple">任務二</span>
        <h3 class="task-title">⚖️【東西方鬼節文化比一比】（小組導學對照表）</h3>
        <p style="color: var(--text-muted); font-size: 0.9rem;">
          透過信仰背景、節慶儀式與飲食文化，體會西洋萬聖夜的面具驅鬼與台灣中元節的孝道博愛：
        </p>

        <div class="comparison-grid">
          <!-- 西洋萬聖夜 -->
          <div class="comp-card western">
            <h4>🎃 西洋萬聖夜（Halloween）</h4>
            <div class="comp-item">
              <div class="comp-label">節慶日期</div>
              <div class="comp-value">10 月 31 日（萬聖節前夜）</div>
            </div>
            <div class="comp-item">
              <div class="comp-label">核心信仰與心理</div>
              <div class="comp-value">面具驅鬼與敬畏亡靈（直面未知恐懼，轉化為幽默慶典）</div>
            </div>
            <div class="comp-item">
              <div class="comp-label">代表活動與儀式</div>
              <div class="comp-value">Trick or Treat 挨家要糖 / 變裝化妝舞會 / 雕刻南瓜燈</div>
            </div>
            <div class="comp-item">
              <div class="comp-label">代表飲食與象徵物</div>
              <div class="comp-value">南瓜派、太妃糖蘋果、萬聖綜合糖果</div>
            </div>
          </div>

          <!-- 台灣中元節 -->
          <div class="comp-card eastern">
            <h4>🏮 台灣中元節（Zhongyuan Festival）</h4>
            <div class="comp-item">
              <div class="comp-label">節慶日期</div>
              <div class="comp-value">傳統農曆七月十五日（農曆七月民俗月）</div>
            </div>
            <div class="comp-item">
              <div class="comp-label">核心信仰與心理</div>
              <div class="comp-value">目蓮救母與孝道普渡（慎終追遠敬祖、慈悲布施無主孤魂好兄弟）</div>
            </div>
            <div class="comp-item">
              <div class="comp-label">代表活動與儀式</div>
              <div class="comp-value">中元普渡設宴 / 頭城與恆春搶孤濟貧 / 水燈引路</div>
            </div>
            <div class="comp-item">
              <div class="comp-label">代表飲食與象徵物</div>
              <div class="comp-value">三牲素果、零食金紙、水煮空心菜湯（象徵無心留難）</div>
            </div>
          </div>
        </div>
      </div>

      <!-- 任務三：個人文化省思與 Kahoot! 線上挑戰 -->
      <div class="task-section">
        <span class="task-tag tag-green">任務三</span>
        <h3 class="task-title">✍️【個人文化省思與 Kahoot! 線上挑戰】</h3>
        
        <p style="font-size: 0.95rem; margin-bottom: 0.5rem;">
          <strong>個人反思寫作</strong>：寫下你在文化比一比中，覺得東西方鬼節「最有趣」或「最值得尊重」的一項傳統反思（字數至少 50 字）：
        </p>
        <textarea class="student-textarea" id="student_reflection_l2" placeholder="例如：我覺得台灣中元節準備空心菜湯招待好兄弟但『無心挽留』的習俗非常有禮貌且富有慈悲心..."></textarea>

        <!-- 內建 Kahoot! 互動挑戰 -->
        <div class="kahoot-box">
          <div class="kahoot-header">
            <span style="font-weight: 800; font-size: 1.1rem; color: #ffb703;">🎮 Kahoot! 即時互動快問快答</span>
            <span id="kahootScore" style="font-size: 0.9rem; color: #84ff6b; font-weight: bold;">得分：0 分</span>
          </div>
          <div class="kahoot-q-text" id="kahootQuestion">
            Q1: 萬聖節（Halloween）的起源最早可以追溯到古凱爾特人的哪一個傳統節日？
          </div>
          <div class="kahoot-answers" id="kahootAnswers">
            <button class="kahoot-btn k-red" onclick="checkKahoot(0)">▲ 復活節 (Easter)</button>
            <button class="kahoot-btn k-blue" onclick="checkKahoot(1)">◆ 薩溫節 (Samhain)</button>
            <button class="kahoot-btn k-yellow" onclick="checkKahoot(2)">● 聖誕節 (Christmas)</button>
            <button class="kahoot-btn k-green" onclick="checkKahoot(3)">■ 篝火節 (Bonfire Night)</button>
          </div>
          <div id="kahootExplanation" style="margin-top: 1rem; font-size: 0.9rem; color: #cbd5e1; display: none;"></div>
        </div>
      </div>
    </section>

    <!-- ==================== 第三節課：萬聖節美語、節慶歌謠與 AI 互動口語 ==================== -->
    <section class="module-card lesson-pane" id="lesson-pane-2" style="display: none;">
      <div class="module-header">
        <div class="module-title-area">
          <h2>👻 第三節：萬聖節美語、節慶歌謠與 AI 互動口語（配合簡報二）</h2>
          <p>掌握核心英文單字、情境句型辨析，並於三站輪換學習中運用因材網「e度」AI 進行英語口語練習。</p>
        </div>
        <div class="status-pill">⏱️ 45 分鐘沉浸</div>
      </div>

      <!-- 任務一：核心美語單字與用語辨析 -->
      <div class="task-section">
        <span class="task-tag tag-purple">任務一</span>
        <h3 class="task-title">🗣️【核心美語單字與用語辨析】</h3>
        
        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; margin-bottom: 1.25rem;">
          <div style="background: rgba(255, 117, 24, 0.1); border: 1px solid var(--primary-orange); border-radius: 8px; padding: 1rem;">
            <h4 style="color: #ffaa5a; margin-bottom: 0.3rem;">🎉 Happy Halloween!</h4>
            <p style="font-size: 0.88rem; color: var(--text-light);">用於整體的<strong>節慶祝福與見面問候</strong>（如卡片祝福、朋友打招呼）。</p>
          </div>
          <div style="background: rgba(157, 78, 221, 0.1); border: 1px solid var(--accent-purple); border-radius: 8px; padding: 1rem;">
            <h4 style="color: #e0aaff; margin-bottom: 0.3rem;">🍬 Trick or Treat!</h4>
            <p style="font-size: 0.88rem; color: var(--text-light);">專用於萬聖夜孩童敲門<strong>討糖果與角色扮演互動</strong>的專屬口號。</p>
          </div>
        </div>

        <p style="font-size: 0.9rem; color: var(--text-muted); margin-bottom: 0.5rem;">點擊下方圖卡可立即聆聽美式標準發音 🔊：</p>
        <div class="vocab-grid">
          <div class="vocab-card" onclick="speakWord('Witch')">
            <div class="vocab-icon">🧙‍♀️</div>
            <div class="vocab-word">Witch</div>
            <div class="vocab-zh">女巫</div>
          </div>
          <div class="vocab-card" onclick="speakWord('Ghost')">
            <div class="vocab-icon">👻</div>
            <div class="vocab-word">Ghost</div>
            <div class="vocab-zh">幽靈</div>
          </div>
          <div class="vocab-card" onclick="speakWord('Vampire')">
            <div class="vocab-icon">🧛‍♂️</div>
            <div class="vocab-word">Vampire</div>
            <div class="vocab-zh">吸血鬼</div>
          </div>
          <div class="vocab-card" onclick="speakWord('Mummy')">
            <div class="vocab-icon">🧟</div>
            <div class="vocab-word">Mummy</div>
            <div class="vocab-zh">木乃伊</div>
          </div>
          <div class="vocab-card" onclick="speakWord('Skeleton')">
            <div class="vocab-icon">💀</div>
            <div class="vocab-word">Skeleton</div>
            <div class="vocab-zh">骷髏</div>
          </div>
          <div class="vocab-card" onclick="speakWord('Jack-o-lantern')">
            <div class="vocab-icon">🎃</div>
            <div class="vocab-word">Jack-o'-lantern</div>
            <div class="vocab-zh">南瓜燈</div>
          </div>
          <div class="vocab-card" onclick="speakWord('Haunted house')">
            <div class="vocab-icon">🏚️</div>
            <div class="vocab-word">Haunted house</div>
            <div class="vocab-zh">鬼屋</div>
          </div>
        </div>
      </div>

      <!-- 任務二：三站輪換學習闖關卡 -->
      <div class="task-section">
        <span class="task-tag tag-cyan">任務二</span>
        <h3 class="task-title">🏃‍♂️【個人輪換三站學習闖關卡】</h3>
        <p style="color: var(--text-muted); font-size: 0.9rem;">全班分組輪流於三站體驗，完成各站任務並記錄：</p>

        <div class="station-grid">
          <!-- 站別 A -->
          <div class="station-card">
            <span class="station-badge">站別 A</span>
            <h4 style="margin-bottom: 0.5rem; color: #67e8f9;">🎵 數位歌謠站</h4>
            <p style="font-size: 0.85rem; color: var(--text-muted); margin-bottom: 0.75rem;">
              聆聽《Five Little Pumpkins》或《The Skeleton Dance》，寫出 2 個歌曲中聽到的身體部位或數字單字：
            </p>
            <input type="text" class="opac-input" id="song_word_1" placeholder="單字 1 (例: head / two)..." style="margin-bottom: 0.4rem;">
            <input type="text" class="opac-input" id="song_word_2" placeholder="單字 2 (例: knee / five)...">
          </div>

          <!-- 站別 B -->
          <div class="station-card">
            <span class="station-badge">站別 B</span>
            <h4 style="margin-bottom: 0.5rem; color: #ffa94d;">🎭 情境口語站</h4>
            <p style="font-size: 0.85rem; color: var(--text-muted); margin-bottom: 0.75rem;">
              與同儕練習變裝問答句型，並請夥伴檢核核章：<br>
              <code>A: What are you dressed up as?</code><br>
              <code>B: I'm dressed up as a witch.</code>
            </p>
            <input type="text" class="opac-input" id="peer_name_1" placeholder="夥伴 1 簽名..." style="margin-bottom: 0.4rem;">
            <input type="text" class="opac-input" id="peer_name_2" placeholder="夥伴 2 簽名...">
          </div>

          <!-- 站別 C -->
          <div class="station-card">
            <span class="station-badge">站別 C</span>
            <h4 style="margin-bottom: 0.5rem; color: #c084fc;">🤖 因材網「e度」AI 站</h4>
            <p style="font-size: 0.85rem; color: var(--text-muted); margin-bottom: 0.5rem;">
              與 AI 學習夥伴進行 1:1 英文對話，記錄自己向 AI 提出的英文問題：
            </p>
            
            <div class="ai-chat-box">
              <div class="ai-chat-messages" id="aiChatMessages">
                <div class="chat-bubble bubble-ai">
                  Hi there! Happy Halloween! 🎃 What costume do you like best?
                </div>
              </div>
              <div class="chat-input-row">
                <input type="text" class="opac-input" id="aiChatInput" placeholder="輸入英文與 e度 對話..." onkeypress="if(event.key==='Enter') sendAiMessage()">
                <button class="btn btn-primary" onclick="sendAiMessage()">送出</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ==================== 第四節課：創意手作、健康食安與數位成果發表 ==================== -->
    <section class="module-card lesson-pane" id="lesson-pane-3" style="display: none;">
      <div class="module-header">
        <div class="module-title-area">
          <h2>🎨 第四節：創意手作、健康食安與數位成果發表</h2>
          <p>體驗節慶手作、建立食安與控糖觀念，並透過 Canva 海報與 SRL 自主學習反思完成成果展示。</p>
        </div>
        <div class="status-pill">⏱️ 45 分鐘發表</div>
      </div>

      <!-- 任務一：聰明挑糖與食安標示大解密 -->
      <div class="task-section">
        <span class="task-tag tag-green">任務一</span>
        <h3 class="task-title">🔍【聰明挑糖與食安標示大解密】（健康飲食素養）</h3>
        <p style="font-size: 0.95rem; line-height: 1.7; margin-bottom: 1rem;">
          討糖也要顧健康！根據台灣《食品安全衛生管理法》第 22 條，合格市售包裝糖果必須具備<strong>四大法定標示</strong>：
        </p>

        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 1rem;">
          <div style="background: rgba(255, 255, 255, 0.04); border-left: 3px solid #39ff14; padding: 1rem; border-radius: 6px;">
            <strong style="color: #86efac;">① 品名與內容物</strong>
            <p style="font-size: 0.85rem; color: var(--text-muted); margin-top: 0.3rem;">包含主原料與所有食品添加物名稱（如人工色素、甜味劑）。</p>
          </div>
          <div style="background: rgba(255, 255, 255, 0.04); border-left: 3px solid #39ff14; padding: 1rem; border-radius: 6px;">
            <strong style="color: #86efac;">② 製造商 / 進口商資訊</strong>
            <p style="font-size: 0.85rem; color: var(--text-muted); margin-top: 0.3rem;">完整公司名稱、電話與地址，出問題時有明確責任窗口。</p>
          </div>
          <div style="background: rgba(255, 255, 255, 0.04); border-left: 3px solid #39ff14; padding: 1rem; border-radius: 6px;">
            <strong style="color: #86efac;">③ 有效日期與保存條件</strong>
            <p style="font-size: 0.85rem; color: var(--text-muted); margin-top: 0.3rem;">標記製造日與有效期限，避免誤食受潮發霉變質的糖果。</p>
          </div>
          <div style="background: rgba(255, 255, 255, 0.04); border-left: 3px solid #39ff14; padding: 1rem; border-radius: 6px;">
            <strong style="color: #86efac;">④ 營養標示與過敏原警語</strong>
            <p style="font-size: 0.85rem; color: var(--text-muted); margin-top: 0.3rem;">標明總糖量與熱量，並註記花生、堅果或牛奶過敏原警語。</p>
          </div>
        </div>
      </div>

      <!-- 任務二：創意手作與 Canva 海報設計構想 -->
      <div class="task-section">
        <span class="task-tag tag-orange">任務二</span>
        <h3 class="task-title">🖌️【創意手作與 Canva 數位海報設計構想】</h3>
        
        <p style="font-size: 0.95rem; margin-bottom: 0.75rem;">請勾選你的個人創作項目：</p>
        <div style="display: flex; gap: 1.5rem; flex-wrap: wrap; margin-bottom: 1rem;">
          <label style="display: flex; align-items: center; gap: 0.4rem; cursor: pointer;">
            <input type="radio" name="craft_type" value="paper_pumpkin" checked> 🎃 紙盤南瓜燈
          </label>
          <label style="display: flex; align-items: center; gap: 0.4rem; cursor: pointer;">
            <input type="radio" name="craft_type" value="candy_box"> 🍬 環保萬聖糖果盒
          </label>
          <label style="display: flex; align-items: center; gap: 0.4rem; cursor: pointer;">
            <input type="radio" name="craft_type" value="canva_poster"> 🎨 Canva 健康點心標示海報
          </label>
        </div>

        <p style="font-size: 0.9rem; color: var(--text-muted);">設計色彩搭配與亮點構想：</p>
        <textarea class="student-textarea" id="craft_concept" placeholder="例如：主色採用午夜黑配螢光橘，並在 Canva 海報右上角設計花生過敏原小標章提醒同學..."></textarea>
      </div>

      <!-- 任務三：同儕互評與 SRL 自主學習反思 -->
      <div class="task-section">
        <span class="task-tag tag-purple">任務三</span>
        <h3 class="task-title">🌟【數位成果發表同儕互評與 SRL 自主學習反思】</h3>
        
        <!-- 同儕互評 -->
        <div style="background: rgba(255, 255, 255, 0.03); padding: 1rem; border-radius: var(--radius-sm); margin-bottom: 1.5rem;">
          <strong style="color: #e0aaff;">🤝 同儕互評（Peer Review）：</strong>
          <div style="margin-top: 0.5rem; display: flex; flex-direction: column; gap: 0.5rem;">
            <input type="text" class="opac-input" id="peer_review_target" placeholder="被評論同學座號與姓名...">
            <input type="text" class="opac-input" id="peer_review_praise" placeholder="🌟 一句欣賞讚賞 (Praise)...">
            <input type="text" class="opac-input" id="peer_review_suggestion" placeholder="💡 一項改進建議 (Suggestion)...">
          </div>
        </div>

        <!-- SRL 自主學習星級量表 -->
        <div>
          <strong style="color: #ffb703;">📊 SRL（Self-Regulated Learning）自主學習星級評分 (1~5★)：</strong>
          
          <div style="margin-top: 0.75rem; display: flex; flex-direction: column; gap: 0.75rem;">
            <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap;">
              <span>🎯 目標設定與進度監控能力：</span>
              <div class="star-rating" data-target="srl_goal">
                <span class="star active" onclick="setRating('srl_goal', 1)">★</span>
                <span class="star active" onclick="setRating('srl_goal', 2)">★</span>
                <span class="star active" onclick="setRating('srl_goal', 3)">★</span>
                <span class="star active" onclick="setRating('srl_goal', 4)">★</span>
                <span class="star" onclick="setRating('srl_goal', 5)">★</span>
              </div>
            </div>

            <div style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap;">
              <span>💻 數位工具運用能力（OPAC / Canva / 因材網 e度 / Kahoot!）：</span>
              <div class="star-rating" data-target="srl_tools">
                <span class="star active" onclick="setRating('srl_tools', 1)">★</span>
                <span class="star active" onclick="setRating('srl_tools', 2)">★</span>
                <span class="star active" onclick="setRating('srl_tools', 3)">★</span>
                <span class="star active" onclick="setRating('srl_tools', 4)">★</span>
                <span class="star active" onclick="setRating('srl_tools', 5)">★</span>
              </div>
            </div>
          </div>

          <div style="margin-top: 1rem;">
            <strong>📝 四節課總收穫省思：</strong>
            <textarea class="student-textarea" id="student_total_reflection" placeholder="總結你在這四節課跨領域探索（檢索、文化、美語、健康）中最深刻的學習收穫..."></textarea>
          </div>
        </div>
      </div>
    </section>

  </main>

  <script>
    // 內建館藏資料 (模擬 OPAC 資料庫)
    const libraryBooks = [
      {
        id: "BK-024",
        title: "西方節慶與世界神話：從萬聖節薩溫之火到諸神黃昏",
        author: "艾瑪·華生 (Emma Watson) / 林雅詩 譯",
        callNumber: "538.5 / 712",
        shelf: "1F 跨文化專區 架號 SOC-02-B",
        tags: ["萬聖節", "西方節慶", "薩溫節", "神話傳說"]
      },
      {
        id: "BK-025",
        title: "台灣民俗大解密：中元普渡、搶孤與人情博愛",
        author: "黃文博 教授",
        callNumber: "538.2 / 419",
        shelf: "1F 本土文化專區 架號 TW-01-C",
        tags: ["中元節", "普渡", "搶孤", "台灣民俗"]
      },
      {
        id: "BK-026",
        title: "青少年健康食安指南：看懂食品標示與糖分陷阱",
        author: "陳思維 營養師",
        callNumber: "411.3 / 883",
        shelf: "2F 健康生活專區 架號 SCI-03-A",
        tags: ["食安", "營養標示", "健康飲食", "生活科技"]
      },
      {
        id: "BK-001",
        title: "Python 程式設計超入門：從零開始寫出實用程式",
        author: "張偉明",
        callNumber: "312.4 / 844-2",
        shelf: "2F 資訊科技區 架號 IT-03-B",
        tags: ["Python", "資訊科技", "程式設計"]
      },
      {
        id: "BK-022",
        title: "原子習慣 (青少年版)：細微改變帶來巨大成就",
        author: "詹姆斯·克利爾",
        callNumber: "176.5 / 128",
        shelf: "2F 心理勵志區 架號 GUI-03-A",
        tags: ["自主學習", "習慣管理"]
      }
    ];

    // 切換分頁
    function switchLessonTab(tabIndex) {
      const tabs = document.querySelectorAll('.nav-tab-btn');
      const panes = document.querySelectorAll('.lesson-pane');
      tabs.forEach((tab, idx) => {
        if (idx === tabIndex) {
          tab.classList.add('active');
          panes[idx].style.display = 'block';
        } else {
          tab.classList.remove('active');
          panes[idx].style.display = 'none';
        }
      });
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    // 教師/學生模式切換
    let isTeacherMode = false;
    function toggleTeacherStudentMode() {
      isTeacherMode = !isTeacherMode;
      const btn = document.getElementById('modeToggleBtn');
      if (isTeacherMode) {
        btn.innerHTML = '<span>🎓 學生互動模式</span>';
        document.querySelectorAll('.inline-blank').forEach(el => el.classList.add('revealed'));
        alert("已切換為【教師教案模式】：填空正解已預先顯現，便於教學引導！");
      } else {
        btn.innerHTML = '<span>👩‍🏫 教師教案模式</span>';
        document.querySelectorAll('.inline-blank').forEach(el => el.classList.remove('revealed'));
        alert("已切換為【學生互動模式】：可讓學生自行填答與探索！");
      }
    }

    // OPAC 檢索邏輯
    function triggerSearch(keyword) {
      document.getElementById('opacKeyword').value = keyword;
      handleOpacSearch();
    }

    function handleOpacSearch() {
      const q = document.getElementById('opacKeyword').value.trim().toLowerCase();
      const container = document.getElementById('opacResults');
      
      const filtered = libraryBooks.filter(book => {
        if (!q) return true;
        const text = `${book.title} ${book.author} ${book.callNumber} ${book.tags.join(' ')}`.toLowerCase();
        return text.includes(q);
      });

      if (filtered.length === 0) {
        container.innerHTML = '<div style="color: var(--text-muted); padding: 1rem;">查無館藏，請嘗試其他關鍵字（如：萬聖節、中元節、食安）</div>';
        return;
      }

      container.innerHTML = filtered.map(b => `
        <div class="book-card">
          <div>
            <div class="book-title">${b.title}</div>
            <div class="book-meta">作者：${b.author}</div>
            <div style="display: flex; gap: 0.3rem; flex-wrap: wrap;">
              ${b.tags.map(t => `<span style="font-size: 0.7rem; background: rgba(255,255,255,0.06); padding: 2px 6px; border-radius: 4px;">#${t}</span>`).join('')}
            </div>
          </div>
          <div>
            <div class="call-number-badge">索書號：${b.callNumber}</div>
            <div style="font-size: 0.8rem; color: var(--text-muted); margin-top: 0.3rem;">📍 架位：${b.shelf}</div>
            <button class="btn btn-outline" style="font-size: 0.75rem; padding: 0.3rem 0.6rem; margin-top: 0.5rem;" onclick="selectBookForWorksheet('${b.title}', '${b.callNumber}', '${b.shelf}')">📌 帶入學習單</button>
          </div>
        </div>
      `).join('');
    }

    function selectBookForWorksheet(title, callNum, shelf) {
      document.getElementById('student_book_name').value = title;
      document.getElementById('student_call_number').value = callNum;
      document.getElementById('student_book_shelf').value = shelf;
      alert(`已將《${title}》的索書號與架位帶入下方實作登記表！`);
    }

    // 觀點填空點擊揭曉
    function toggleBlank(element, answer) {
      if (element.classList.contains('revealed')) {
        element.classList.remove('revealed');
        element.innerText = '［？點擊揭曉］';
      } else {
        element.classList.add('revealed');
        element.innerText = answer;
      }
    }

    // Web Speech API 發音
    function speakWord(word) {
      if ('speechSynthesis' in window) {
        const utter = new SpeechSynthesisUtterance(word);
        utter.lang = 'en-US';
        utter.rate = 0.85;
        window.speechSynthesis.speak(utter);
      } else {
        alert("您的瀏覽器暫不支援語音合成發音。");
      }
    }

    // AI 對話模擬
    function sendAiMessage() {
      const input = document.getElementById('aiChatInput');
      const val = input.value.trim();
      if (!val) return;

      const chatBox = document.getElementById('aiChatMessages');
      
      // 使用者發送
      const userBubble = document.createElement('div');
      userBubble.className = 'chat-bubble bubble-user';
      userBubble.innerText = val;
      chatBox.appendChild(userBubble);
      input.value = '';

      // AI 回應
      setTimeout(() => {
        const aiBubble = document.createElement('div');
        aiBubble.className = 'chat-bubble bubble-ai';
        
        const replies = [
          "Awesome! I love witches and jack-o'-lanterns! Did you know carved pumpkins were originally turnips in Ireland? 🎃",
          "That sounds so cool! Don't forget to say 'Trick or Treat!' with a loud, confident voice! 👻",
          "Great English sentence! Remember to check food safety labels before enjoying your Halloween candy! 🍬",
          "Splendid costume idea! Would you like to ask me anything else about Halloween or Samhain?"
        ];
        aiBubble.innerText = replies[Math.floor(Math.random() * replies.length)];
        chatBox.appendChild(aiBubble);
        chatBox.scrollTop = chatBox.scrollHeight;
      }, 600);
    }

    // Kahoot 題目模擬器
    const kahootQuestions = [
      {
        q: "Q1: 萬聖節（Halloween）的起源最早可以追溯到古凱爾特人的哪一個傳統節日？",
        options: ["▲ 復活節 (Easter)", "◆ 薩溫節 (Samhain)", "● 聖誕節 (Christmas)", "■ 篝火節 (Bonfire Night)"],
        correct: 1,
        exp: "正確！古凱爾特人的薩溫節象徵夏天的結束與新年的開端。"
      },
      {
        q: "Q2: 在愛爾蘭民間傳說中，『吝嗇傑克』最初是用哪一種蔬菜來雕刻他的燈籠？",
        options: ["▲ 蕪菁（大頭菜）", "◆ 巨大南瓜", "● 馬鈴薯", "■ 甜菜根"],
        correct: 0,
        exp: "正確！最初是用蕪菁（大頭菜），傳到盛產南瓜的美國後才演變為南瓜燈。"
      },
      {
        q: "Q3: 台灣中元普渡祭品中常見『水煮空心菜湯』，在民俗文化上有何寓意？",
        options: ["▲ 夏天降火解暑", "◆ 象徵主家無心留難好兄弟", "● 祈求大豐收", "■ 空心菜最便宜"],
        correct: 1,
        exp: "正確！『空心』象徵主家好客但無心強留，陰陽各安其位、以禮相待。"
      }
    ];
    let curKIndex = 0;
    let kahootScore = 0;

    function checkKahoot(selectedIdx) {
      const qObj = kahootQuestions[curKIndex];
      const expDiv = document.getElementById('kahootExplanation');
      expDiv.style.display = 'block';

      if (selectedIdx === qObj.correct) {
        kahootScore += 100;
        expDiv.innerHTML = `<span style="color:#84ff6b; font-weight:bold;">🎉 答對了！+100分</span><br>${qObj.exp}`;
      } else {
        expDiv.innerHTML = `<span style="color:#ff6b6b; font-weight:bold;">❌ 答錯囉！</span><br>${qObj.exp}`;
      }
      document.getElementById('kahootScore').innerText = `得分：${kahootScore} 分`;

      // 換下一題或結束
      setTimeout(() => {
        curKIndex++;
        if (curKIndex < kahootQuestions.length) {
          loadKahootQuestion();
        } else {
          document.getElementById('kahootQuestion').innerText = `🏆 挑戰結束！您的最終得分是：${kahootScore} 分！`;
          document.getElementById('kahootAnswers').innerHTML = '<button class="btn btn-primary" onclick="resetKahoot()">🔄 重新挑戰</button>';
          expDiv.style.display = 'none';
        }
      }, 1800);
    }

    function loadKahootQuestion() {
      const qObj = kahootQuestions[curKIndex];
      document.getElementById('kahootQuestion').innerText = qObj.q;
      const btnColors = ['k-red', 'k-blue', 'k-yellow', 'k-green'];
      document.getElementById('kahootAnswers').innerHTML = qObj.options.map((opt, i) => `
        <button class="kahoot-btn ${btnColors[i]}" onclick="checkKahoot(${i})">${opt}</button>
      `).join('');
      document.getElementById('kahootExplanation').style.display = 'none';
    }

    function resetKahoot() {
      curKIndex = 0;
      kahootScore = 0;
      document.getElementById('kahootScore').innerText = `得分：0 分`;
      loadKahootQuestion();
    }

    // SRL 星星評分點擊
    function setRating(targetKey, score) {
      const container = document.querySelector(`.star-rating[data-target="${targetKey}"]`);
      if (!container) return;
      const stars = container.querySelectorAll('.star');
      stars.forEach((s, idx) => {
        if (idx < score) s.classList.add('active');
        else s.classList.remove('active');
      });
      localStorage.setItem(`rating_${targetKey}`, score);
    }

    // 儲存與匯出學生學習歷程
    function exportStudentData() {
      const studentData = {
        timestamp: new Date().toISOString(),
        opacBook: document.getElementById('student_book_name').value,
        opacCallNumber: document.getElementById('student_call_number').value,
        reflectionL2: document.getElementById('student_reflection_l2').value,
        songWords: [document.getElementById('song_word_1').value, document.getElementById('song_word_2').value],
        craftConcept: document.getElementById('craft_concept').value,
        totalReflection: document.getElementById('student_total_reflection').value
      };

      const blob = new Blob([JSON.stringify(studentData, null, 2)], { type: "application/json" });
      const url = URL.createObjectURL(blob);
      const a = document.createElement("a");
      a.href = url;
      a.download = `halloween_learning_portfolio_${new Date().toISOString().slice(0,10)}.json`;
      a.click();
      URL.revokeObjectURL(url);
      alert("✅ 學習歷程檔案已成功匯出至下載資料夾！");
    }

    // 初始化頁面
    window.addEventListener('DOMContentLoaded', () => {
      handleOpacSearch();
    });
  </script>
</body>
</html>
[halloween.html](https://github.com/user-attachments/files/33415537/halloween.html)
