<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Transit SYNC</title>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.9.0/p5.min.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Nunito:wght@400;600;700;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg:        #2b2b2b;
      --bg-deep:   #222222;
      --orange:    #c8622a;
      --orange-lt: #d4733f;
      --orange-dk: #a84e1e;
      --card:      #f5f4f2;
      --card-line: #e0ddd9;
      --text-dark: #1a1a1a;
      --text-mid:  #555;
      --text-soft: #888;
      --white:     #ffffff;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      background: var(--bg);
      font-family: 'Nunito', sans-serif;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    /* ── TOP BAR ── */
    .topbar {
      background: var(--orange);
      padding: 18px 40px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      box-shadow: 0 4px 20px rgba(0,0,0,0.35);
    }

    .topbar h1 {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 32px;
      color: var(--white);
      letter-spacing: 2px;
    }

    .topbar h1 span { font-weight: 400; opacity: 0.85; }

    .topbar-right {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 13px;
      color: rgba(255,255,255,0.7);
      font-weight: 600;
    }

    .dot-live {
      width: 8px; height: 8px;
      border-radius: 50%;
      background: #fff;
      animation: blink 2s infinite;
    }
    @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0.3} }

    /* ── LAYOUT ── */
    .main {
      flex: 1;
      display: grid;
      grid-template-columns: 360px 1fr;
      gap: 0;
      min-height: 0;
    }

    /* ── LEFT PANEL ── */
    .panel-left {
      background: var(--bg-deep);
      border-right: 1px solid #333;
      padding: 36px 28px;
      display: flex;
      flex-direction: column;
      gap: 28px;
    }

    .section-label {
      font-size: 10px;
      letter-spacing: 3px;
      text-transform: uppercase;
      color: var(--orange-lt);
      font-weight: 800;
      margin-bottom: 10px;
    }

    .input-group { display: flex; flex-direction: column; }

    .input-group label {
      font-size: 11px;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: rgba(255,255,255,0.4);
      font-weight: 700;
      margin-bottom: 8px;
    }

    .input-group input {
      background: #333;
      border: 2px solid #3e3e3e;
      border-radius: 10px;
      padding: 13px 16px;
      font-family: 'Nunito', sans-serif;
      font-size: 16px;
      font-weight: 700;
      color: var(--white);
      outline: none;
      transition: border-color 0.2s, background 0.2s;
    }

    .input-group input::placeholder { color: #555; font-weight: 400; }
    .input-group input:focus {
      border-color: var(--orange);
      background: #3a3a3a;
    }

    .btn-lookup {
      width: 100%;
      padding: 15px;
      background: var(--orange);
      color: var(--white);
      font-family: 'Bebas Neue', sans-serif;
      font-size: 20px;
      letter-spacing: 3px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: background 0.15s, transform 0.1s, box-shadow 0.15s;
      box-shadow: 0 4px 16px rgba(200,98,42,0.3);
    }
    .btn-lookup:hover {
      background: var(--orange-lt);
      box-shadow: 0 6px 22px rgba(200,98,42,0.45);
    }
    .btn-lookup:active { transform: scale(0.98); }
    .btn-lookup:disabled {
      background: #444;
      color: #666;
      cursor: not-allowed;
      box-shadow: none;
    }

    #status {
      font-size: 12px;
      font-weight: 600;
      min-height: 16px;
      text-align: center;
    }
    .s-error   { color: #e07070; }
    .s-loading { color: #888; animation: blink 1s infinite; }
    .s-ok      { color: #7ecb9a; }

    /* ── REMINDER CARD (left panel) ── */
    .reminder-section { flex: 1; }

    .reminder-card {
      background: var(--card);
      border-radius: 14px;
      overflow: hidden;
      box-shadow: 0 6px 24px rgba(0,0,0,0.4);
      display: none;
      animation: slideUp 0.3s ease;
    }

    @keyframes slideUp {
      from { opacity:0; transform:translateY(10px); }
      to   { opacity:1; transform:translateY(0); }
    }

    .reminder-card-header {
      background: var(--card);
      padding: 16px 20px 10px;
      border-bottom: 1px solid var(--card-line);
    }

    .reminder-card-header h3 {
      font-size: 18px;
      font-weight: 800;
      color: var(--text-dark);
    }

    .rc-arrival-time {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 36px;
      color: var(--orange);
      letter-spacing: 1px;
      line-height: 1.1;
      margin-top: 2px;
    }

    .reminder-card-body {
      padding: 14px 20px 18px;
    }

    .reminder-route {
      font-size: 17px;
      font-weight: 800;
      color: var(--text-dark);
      margin-bottom: 4px;
    }

    .reminder-route span { color: var(--orange); }

    .reminder-dest {
      font-size: 14px;
      color: var(--text-mid);
      font-weight: 600;
      margin-bottom: 12px;
    }

    /* ── REMINDER TIME CHIPS ── */
    .reminder-chips-list {
      display: flex;
      flex-direction: column;
      gap: 8px;
      margin-bottom: 10px;
    }

    .reminder-chip {
      display: flex;
      align-items: center;
      justify-content: space-between;
      border: 2px solid var(--text-dark);
      border-radius: 10px;
      padding: 10px 14px;
      background: var(--card);
      animation: slideUp 0.2s ease;
    }

    .reminder-chip-label {
      font-size: 15px;
      font-weight: 800;
      color: var(--text-dark);
    }

    .reminder-chip-actions {
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .chip-edit-btn {
      background: none;
      border: none;
      cursor: pointer;
      font-size: 15px;
      color: var(--text-soft);
      padding: 2px 4px;
      border-radius: 4px;
      transition: color 0.15s;
      line-height: 1;
    }
    .chip-edit-btn:hover { color: var(--orange); }

    .chip-delete-btn {
      background: none;
      border: none;
      cursor: pointer;
      font-size: 14px;
      color: #bbb;
      padding: 2px 4px;
      border-radius: 4px;
      transition: color 0.15s;
      line-height: 1;
    }
    .chip-delete-btn:hover { color: #e07070; }

    .chip-edit-input {
      width: 90px;
      background: none;
      border: none;
      border-bottom: 2px solid var(--orange);
      font-family: 'Nunito', sans-serif;
      font-size: 15px;
      font-weight: 800;
      color: var(--text-dark);
      outline: none;
      padding: 0 2px;
    }

    .add-chip-btn {
      width: 100%;
      padding: 10px 14px;
      background: none;
      border: 2px dashed #ccc;
      border-radius: 10px;
      font-family: 'Nunito', sans-serif;
      font-size: 22px;
      font-weight: 300;
      color: #bbb;
      cursor: pointer;
      transition: border-color 0.15s, color 0.15s;
      margin-bottom: 12px;
    }
    .add-chip-btn:hover { border-color: var(--orange); color: var(--orange); }

    .cancel-reminder-btn {
      width: 100%;
      padding: 12px;
      background: none;
      border: 2px solid var(--orange);
      border-radius: 10px;
      font-family: 'Nunito', sans-serif;
      font-size: 14px;
      font-weight: 800;
      color: var(--orange);
      cursor: pointer;
      letter-spacing: 0.5px;
      transition: background 0.15s, color 0.15s;
    }
    .cancel-reminder-btn:hover { background: var(--orange); color: #fff; }

    .save-reminder-btn {
      width: 100%;
      padding: 12px;
      background: var(--orange);
      border: 2px solid var(--orange);
      border-radius: 10px;
      font-family: 'Nunito', sans-serif;
      font-size: 14px;
      font-weight: 800;
      color: #fff;
      cursor: pointer;
      letter-spacing: 0.5px;
      margin-bottom: 8px;
      transition: background 0.2s, border-color 0.2s, transform 0.1s, box-shadow 0.2s;
      box-shadow: 0 4px 14px rgba(200,98,42,0.3);
    }
    .save-reminder-btn:hover {
      background: var(--orange-lt);
      border-color: var(--orange-lt);
      box-shadow: 0 6px 18px rgba(200,98,42,0.45);
    }
    .save-reminder-btn:active { transform: scale(0.97); }
    .save-reminder-btn.saved {
      background: #4a9e6e;
      border-color: #4a9e6e;
      box-shadow: 0 4px 14px rgba(74,158,110,0.3);
    }

    .save-confirm {
      text-align: center;
      font-size: 12px;
      font-weight: 700;
      color: #4a9e6e;
      margin-bottom: 8px;
      opacity: 0;
      transform: translateY(-4px);
      transition: opacity 0.25s ease, transform 0.25s ease;
      pointer-events: none;
    }
    .save-confirm.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* ── TAB BAR ── */
    .tab-bar {
      display: flex;
      align-items: center;
      gap: 4px;
      margin-bottom: 24px;
      border-bottom: 2px solid #333;
      padding-bottom: 0;
    }

    .tab-btn {
      background: none;
      border: none;
      font-family: 'Bebas Neue', sans-serif;
      font-size: 20px;
      letter-spacing: 2px;
      color: #555;
      cursor: pointer;
      padding: 10px 18px 12px;
      border-bottom: 3px solid transparent;
      margin-bottom: -2px;
      transition: color 0.15s, border-color 0.15s;
      display: flex;
      align-items: center;
      gap: 8px;
      white-space: nowrap;
    }

    .tab-btn:hover { color: #999; }

    .tab-btn.active {
      color: var(--white);
      border-bottom-color: var(--orange);
    }

    .tab-badge {
      background: var(--orange);
      color: #fff;
      font-family: 'Nunito', sans-serif;
      font-size: 11px;
      font-weight: 800;
      border-radius: 10px;
      padding: 1px 7px;
      line-height: 16px;
    }

    /* ── REMINDERS LIST ── */
    .reminders-list {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .reminder-row {
      background: var(--card);
      border-radius: 14px;
      padding: 16px 20px;
      display: grid;
      grid-template-columns: auto 1fr auto;
      align-items: center;
      gap: 16px;
      animation: fadeUp 0.25s ease both;
      box-shadow: 0 2px 12px rgba(0,0,0,0.2);
    }

    .reminder-row-route {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 32px;
      color: var(--orange);
      line-height: 1;
      min-width: 48px;
      text-align: center;
    }

    .reminder-row-info { display: flex; flex-direction: column; gap: 3px; }

    .reminder-row-time {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 20px;
      color: var(--text-dark);
      letter-spacing: 1px;
    }

    .reminder-row-thresholds {
      font-size: 12px;
      font-weight: 600;
      color: var(--text-mid);
    }

    .reminder-row-modes {
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      gap: 4px;
    }

    .mode-pill {
      font-size: 10px;
      font-weight: 800;
      letter-spacing: 1px;
      text-transform: uppercase;
      padding: 3px 8px;
      border-radius: 20px;
      white-space: nowrap;
    }

    .mode-pill.light {
      background: rgba(79,68,224,0.12);
      color: #4f44e0;
    }

    .mode-pill.notif {
      background: rgba(74,158,110,0.12);
      color: #4a9e6e;
    }

    .reminder-row-remove {
      background: none;
      border: none;
      color: #ccc;
      font-size: 16px;
      cursor: pointer;
      padding: 4px;
      border-radius: 6px;
      transition: color 0.15s;
      align-self: flex-start;
    }
    .reminder-row-remove:hover { color: #e07070; }

    /* ── ARRIVALS HEADER (meta only, now inside tab bar) ── */
    #arrivalsMeta {
      margin-left: auto;
      font-size: 12px;
      color: #555;
      font-weight: 600;
      padding-bottom: 12px;
    }

    /* ── RIGHT PANEL ── */
    .panel-right {
      padding: 36px 36px;
      overflow-y: auto;
    }

    .arrivals-header {
      display: flex;
      justify-content: space-between;
      align-items: baseline;
      margin-bottom: 20px;
    }

    .arrivals-title {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 28px;
      color: var(--white);
      letter-spacing: 2px;
    }

    .arrivals-meta {
      font-size: 12px;
      color: #666;
      font-weight: 600;
    }

    .empty-state {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 60%;
      gap: 12px;
      color: #444;
      text-align: center;
    }

    .empty-icon {
      font-size: 52px;
      opacity: 0.3;
    }

    .empty-state p {
      font-size: 14px;
      font-weight: 600;
      color: #555;
    }

    /* ── ARRIVALS GRID ── */
    .arrivals-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
      gap: 14px;
    }

    .arrival-card {
      background: var(--card);
      border-radius: 14px;
      padding: 18px 18px 14px;
      cursor: pointer;
      transition: transform 0.15s, box-shadow 0.15s, outline 0.1s;
      animation: fadeUp 0.25s ease both;
      position: relative;
      overflow: hidden;
    }

    .arrival-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 4px;
      background: var(--orange);
      transform: scaleX(0);
      transform-origin: left;
      transition: transform 0.2s;
    }

    .arrival-card:hover { transform: translateY(-3px); box-shadow: 0 8px 28px rgba(0,0,0,0.4); }
    .arrival-card:hover::before { transform: scaleX(1); }
    .arrival-card.selected { outline: 2px solid var(--orange); box-shadow: 0 0 0 4px rgba(200,98,42,0.2); }
    .arrival-card.selected::before { transform: scaleX(1); }

    .bookmark-icon {
      position: absolute;
      top: 0;
      right: 12px;
      width: 18px;
      height: 26px;
      fill: #14A06A;
      opacity: 0;
      transform: translateY(-6px);
      transition: opacity 0.25s ease, transform 0.25s ease;
      pointer-events: none;
    }

    .arrival-card.bookmarked .bookmark-icon {
      opacity: 1;
      transform: translateY(0);
    }

    @keyframes fadeUp {
      from { opacity:0; transform:translateY(10px); }
      to   { opacity:1; transform:translateY(0); }
    }

    .arrival-time {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 30px;
      color: var(--text-dark);
      letter-spacing: 1px;
      line-height: 1;
      margin-bottom: 6px;
    }

    .arrival-headsign {
      font-size: 12px;
      font-weight: 700;
      color: var(--text-mid);
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      margin-bottom: 10px;
    }

    .arrival-until {
      font-size: 11px;
      font-weight: 800;
      color: var(--orange);
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    /* ── BOTTOM BAR ── */
    .bottombar {
      background: var(--orange);
      padding: 14px 40px;
      display: flex;
      justify-content: flex-end;
      align-items: center;
    }

    /* ── MODE SECTION ── */
    .mode-section {
      margin-bottom: 12px;
    }

    .mode-label {
      font-size: 13px;
      font-weight: 800;
      color: var(--text-dark);
      margin-bottom: 8px;
    }

    .mode-box {
      border: 2px solid var(--text-dark);
      border-radius: 10px;
      overflow: hidden;
    }

    .mode-row {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 11px 14px;
    }

    .mode-divider {
      height: 1px;
      background: var(--card-line);
      margin: 0 14px;
    }

    .mode-check-label {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 14px;
      font-weight: 600;
      color: var(--text-dark);
      cursor: pointer;
      user-select: none;
    }

    .mode-checkbox { display: none; }

    .mode-check-box {
      width: 18px;
      height: 18px;
      border: 2px solid #bbb;
      border-radius: 4px;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
      transition: background 0.15s, border-color 0.15s;
    }

    .mode-checkbox:checked + .mode-check-box {
      background: var(--orange);
      border-color: var(--orange);
    }

    .mode-checkbox:checked + .mode-check-box::after {
      content: '';
      width: 5px;
      height: 9px;
      border: 2px solid #fff;
      border-top: none;
      border-left: none;
      transform: rotate(45deg) translateY(-1px);
      display: block;
    }

    /* Gradient swatches */
    .gradient-options {
      display: flex;
      gap: 8px;
      align-items: center;
    }

    .gradient-swatch {
      background: none;
      border: 2px solid transparent;
      border-radius: 8px;
      padding: 3px;
      cursor: pointer;
      transition: border-color 0.15s, transform 0.1s;
    }

    .gradient-swatch:hover { transform: scale(1.08); }

    .gradient-swatch.active {
      border-color: var(--text-dark);
    }

    .swatch-bar {
      display: block;
      width: 48px;
      height: 14px;
      border-radius: 4px;
    }

    .gear-btn {
      background: none;
      border: none;
      cursor: pointer;
      color: rgba(255,255,255,0.8);
      font-size: 22px;
      padding: 4px;
      transition: color 0.15s, transform 0.3s;
    }
    .gear-btn:hover { color: #fff; transform: rotate(45deg); }

    #p5-container { display: none; }
  </style>
</head>
<body>

  <!-- TOP BAR -->
  <div class="topbar">
    <h1>Transit <span>SYNC</span></h1>
    <div class="topbar-right">
      <div class="dot-live"></div>
      LIVE SCHEDULE
    </div>
  </div>

  <!-- MAIN -->
  <div class="main">

    <!-- LEFT: inputs + reminder -->
    <div class="panel-left">

      <div>
        <div class="section-label">Find Your Bus</div>
        <div style="display:flex;flex-direction:column;gap:14px;">
          <div class="input-group">
            <label>Route Number</label>
            <input id="routeInput" type="text" placeholder="e.g. 22" autocomplete="off"/>
          </div>
          <div class="input-group">
            <label>Stop ID</label>
            <input id="stopInput" type="text" placeholder="e.g. 40850" autocomplete="off"/>
          </div>
          <button class="btn-lookup" id="lookupBtn" onclick="runLookup()" disabled>
            CHECK ARRIVALS
          </button>
          <div id="status"></div>
        </div>
      </div>

      <!-- Reminder card -->
      <div class="reminder-section">
        <div class="section-label">Reminder</div>
        <div class="reminder-card" id="reminderCard">
          <div class="reminder-card-header">
            <h3>Reminder Set</h3>
            <div class="rc-arrival-time" id="rc-arrival-time"></div>
          </div>
          <div class="reminder-card-body">
            <div class="reminder-route" style="margin-bottom:12px;">
              <span id="rc-headsign"></span>
            </div>

            <!-- Reminder time chips -->
            <div class="reminder-chips-list" id="reminderChipsList"></div>

            <!-- Add button -->
            <button class="add-chip-btn" onclick="addReminderChip()">+</button>

            <!-- Mode -->
            <div class="mode-section">
              <div class="mode-label">Mode</div>
              <div class="mode-box">

                <!-- Smart Light row -->
                <div class="mode-row">
                  <label class="mode-check-label">
                    <input type="checkbox" id="modeSmart" class="mode-checkbox"/>
                    <span class="mode-check-box"></span>
                    Smart Light
                  </label>
                  <div class="gradient-options" id="gradientOptions">
                    <button class="gradient-swatch active" id="gradientA" onclick="selectGradient('A')" title="Blue–Pink–Red">
                      <span class="swatch-bar" style="background: linear-gradient(to right, #4f44e0, #e040fb, #f44336);"></span>
                    </button>
                    <button class="gradient-swatch" id="gradientB" onclick="selectGradient('B')" title="Green–Yellow–Red">
                      <span class="swatch-bar" style="background: linear-gradient(to right, #14A06A, #f9c23c, #f44336);"></span>
                    </button>
                  </div>
                </div>

                <div class="mode-divider"></div>

                <!-- Notification row -->
                <div class="mode-row">
                  <label class="mode-check-label">
                    <input type="checkbox" id="modeNotif" class="mode-checkbox"/>
                    <span class="mode-check-box"></span>
                    Notification
                  </label>
                </div>

              </div>
            </div>

            <!-- Save -->
            <button class="save-reminder-btn" id="saveReminderBtn" onclick="saveReminder()">Save</button>
            <div class="save-confirm" id="saveConfirm">✓ Reminder saved!</div>

            <!-- Cancel -->
            <button class="cancel-reminder-btn" onclick="cancelReminder()">Cancel Reminder</button>
          </div>
        </div>
      </div>

    </div>

    <!-- RIGHT: tabbed panel -->
    <div class="panel-right">

      <!-- Tab bar -->
      <div class="tab-bar">
        <button class="tab-btn active" id="tabArrivals" onclick="switchTab('arrivals')">
          Scheduled Arrivals
        </button>
        <button class="tab-btn" id="tabReminders" onclick="switchTab('reminders')">
          Pending Reminders
          <span class="tab-badge" id="reminderBadge" style="display:none;">0</span>
        </button>
        <span class="arrivals-meta" id="arrivalsMeta"></span>
      </div>

      <!-- Arrivals view -->
      <div id="viewArrivals">
        <div class="empty-state" id="emptyState">
          <div class="empty-icon">🚌</div>
          <p>Enter a route and stop ID<br>to see arrival times</p>
        </div>
        <div class="arrivals-grid" id="arrivalsGrid" style="display:none;"></div>
      </div>

      <!-- Pending Reminders view -->
      <div id="viewReminders" style="display:none;">
        <div class="empty-state" id="emptyReminders">
          <div class="empty-icon">🔔</div>
          <p>No reminders saved yet.<br>Select an arrival and hit Save.</p>
        </div>
        <div class="reminders-list" id="remindersList"></div>
      </div>

    </div>

  </div>

  <!-- BOTTOM BAR -->
  <div class="bottombar">
    <button class="gear-btn" title="Settings">⚙</button>
  </div>

  <!-- p5 CSV loader (hidden) -->
  <div id="p5-container"></div>

  <script>
    // ── IFTTT CONFIGURATION ──────────────────────────────────────
    // Fill in your IFTTT Webhooks key and event names below.
    // Find your key at: https://ifttt.com/maker_webhooks → Documentation
    const IFTTT_CONFIG = {
      key:              "dqwOB0DYcXL9DHr0dvqyN6",

      // Smart Light events — these IFTTT applets should trigger
      // your KASA bulb to change color. Pass color as value1.
      lightOnEvent:     "transit_light_on",   // turns bulb on
      lightColorEvent:  "transit_light_color", // value1 = KASA advanced options string
      lightOffEvent:    "transit_light_off",   // turns bulb off

      // KASA light settings sent with every color change
      lightBrightness:        80,   // 0–100
      lightTransitionDuration: 3000, // milliseconds

      // SMS / Notification event — value1 = route headsign,
      // value2 = minutes remaining message
      notifyEvent:      "transit_notify",
    };

    // Color steps for each gradient (first→middle→last, up to 3)
    const GRADIENTS = {
      A: ["#4f44e0", "#e040fb", "#f44336"], // Blue → Pink → Red
      B: ["#14A06A", "#f9c23c", "#f44336"], // Green → Yellow → Red
    };

    // Fires a single IFTTT webhook (plain "Receive a web request" trigger)
    // Values are sent as form-encoded body — IFTTT exposes them as {{Value1}}, {{Value2}}, {{Value3}}
    async function triggerIFTTT(eventName, value1 = "", value2 = "", value3 = "") {
      const url = `https://maker.ifttt.com/trigger/${eventName}/with/key/${IFTTT_CONFIG.key}`;
      const body = new URLSearchParams({ value1, value2, value3 });
      try {
        const res = await fetch(url, {
          method: "POST",
          headers: { "Content-Type": "application/x-www-form-urlencoded" },
          body: body.toString(),
        });
        console.log(`IFTTT [${eventName}] →`, res.status, value1 || "");
      } catch (err) {
        console.error(`IFTTT [${eventName}] failed:`, err);
      }
    }

    const CSV_URL = "http://127.0.0.1:8000/Final%20Project/input_data/stop_times_out_v2.csv";
    let stopTimesData = [];
    let dataLoaded = false;
    let reminderInterval = null;
    let selectedArrival = null;

    // ── p5 instance for CSV loading ──────────────────────────────
    new p5(function(p) {
      p.setup = function() {
        p.noCanvas();
        setStatus("s-loading", "Loading schedule data...");
        p.loadTable(CSV_URL, "csv", "header",
          function(table) {
            for (let r = 0; r < table.getRowCount(); r++) {
              stopTimesData.push({
                // trip_id:       table.getString(r, "trip_id"),
                arrival_time:  table.getString(r, "arrival_time").trim(),
                stop_id:       table.getString(r, "stop_id").trim(),
                stop_headsign: table.getString(r, "stop_headsign").trim()
              });
            }
            dataLoaded = true;
            setStatus("s-ok", `✓ ${stopTimesData.length.toLocaleString()} trips loaded`);
            document.getElementById("lookupBtn").disabled = false;
          },
          function() {
            setStatus("s-error", "✕ Could not load CSV — is your server running?");
          }
        );
      };
      p.draw = function() {};
    }, "p5-container");

    // ── Helpers ──────────────────────────────────────────────────
    function setStatus(cls, msg) {
      const el = document.getElementById("status");
      el.className = cls;
      el.textContent = msg;
    }

    // Parse "HH:MM:SS" → total minutes from midnight
    function timeToMins(t) {
      const parts = t.split(":").map(Number);
      return parts[0] * 60 + parts[1] + (parts[2] || 0) / 60;
    }

    // Convert "HH:MM:SS" (24h, may exceed 23) → "h:MM AM/PM"
    function fmtAmPm(timeStr) {
      const parts = timeStr.split(":").map(Number);
      let hours = parts[0] % 24; // handle GTFS times like 25:00
      const mins = parts[1];
      const ampm = hours < 12 ? "AM" : "PM";
      hours = hours % 12 || 12;
      return `${hours}:${String(mins).padStart(2, "0")} ${ampm}`;
    }

    // Minutes until a scheduled time
    function minsUntil(timeStr) {
      const now = new Date();
      const nowMins = now.getHours() * 60 + now.getMinutes() + now.getSeconds() / 60;
      const diff = Math.round(timeToMins(timeStr) - nowMins);
      return diff;
    }

    function fmtUntil(timeStr) {
      const d = minsUntil(timeStr);
      if (d < 0)  return "Departed";
      if (d === 0) return "Arriving now";
      if (d < 60) return `${d} min`;
      return `${Math.floor(d/60)}h ${d%60}m`;
    }

    // ── Lookup ───────────────────────────────────────────────────
    function runLookup() {
      if (!dataLoaded) { setStatus("s-error", "Data not ready yet."); return; }

      const routeNum = document.getElementById("routeInput").value.trim();
      const stopId   = document.getElementById("stopInput").value.trim();

      if (!routeNum || !stopId) {
        setStatus("s-error", "Please fill in both fields.");
        return;
      }

      const filtered = stopTimesData.filter(row => {
        const headRoute = row.stop_headsign.split(" ")[0];
        return headRoute === routeNum && row.stop_id === stopId;
      });

      if (filtered.length === 0) {
        setStatus("s-error", `No arrivals found for route ${routeNum} at stop ${stopId}.`);
        document.getElementById("arrivalsGrid").style.display = "none";
        document.getElementById("emptyState").style.display = "flex";
        document.getElementById("arrivalsMeta").textContent = "";
        return;
      }

      filtered.sort((a, b) => timeToMins(a.arrival_time) - timeToMins(b.arrival_time));

      setStatus("s-ok", `✓ ${filtered.length} arrival${filtered.length !== 1 ? "s" : ""} found`);
      renderArrivals(filtered, routeNum, stopId);
    }

    function renderArrivals(rows, routeNum, stopId) {
      const grid  = document.getElementById("arrivalsGrid");
      const empty = document.getElementById("emptyState");
      const meta  = document.getElementById("arrivalsMeta");

      meta.textContent = `Route ${routeNum} · Stop ${stopId} · ${rows.length} trips`;
      grid.innerHTML = "";
      empty.style.display = "none";
      grid.style.display = "grid";

      rows.forEach((row, i) => {
        const card = document.createElement("div");
        card.className = "arrival-card";
        card.style.animationDelay = `${i * 25}ms`;
        card.dataset.time     = row.arrival_time;
        card.dataset.headsign = row.stop_headsign;

        card.innerHTML = `
          <svg class="bookmark-icon" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path d="M5 3h14a1 1 0 0 1 1 1v17l-8-4-8 4V4a1 1 0 0 1 1-1z"/>
          </svg>
          <div class="arrival-time">${fmtAmPm(row.arrival_time)}</div>
          <div class="arrival-headsign">${row.stop_headsign}</div>
          <div class="arrival-until">${fmtUntil(row.arrival_time)}</div>
        `;

        card.addEventListener("click", () => selectArrival(card, row));
        grid.appendChild(card);
      });
    }

    // ── Saved reminders store ────────────────────────────────────
    let savedReminders = []; // { id, routeNum, headsign, arrivalTime, chips, smartOn, notifOn, gradChoice }
    let savedReminderIdCounter = 0;

    function switchTab(tab) {
      const isArrivals = tab === 'arrivals';
      document.getElementById("tabArrivals").classList.toggle("active", isArrivals);
      document.getElementById("tabReminders").classList.toggle("active", !isArrivals);
      document.getElementById("viewArrivals").style.display  = isArrivals ? "" : "none";
      document.getElementById("viewReminders").style.display = isArrivals ? "none" : "";
      if (!isArrivals) renderRemindersList();
    }

    function renderRemindersList() {
      const list  = document.getElementById("remindersList");
      const empty = document.getElementById("emptyReminders");
      list.innerHTML = "";

      if (savedReminders.length === 0) {
        empty.style.display = "flex";
        list.style.display  = "none";
        return;
      }

      empty.style.display = "none";
      list.style.display  = "flex";

      savedReminders.forEach((r, idx) => {
        const routeNum    = r.headsign.split(" ")[0];
        const thresholds  = r.chips.map(c => `${c.minutes} min`).join(" · ");
        const modes       = [
          r.smartOn ? `<span class="mode-pill light">💡 Smart Light</span>` : "",
          r.notifOn ? `<span class="mode-pill notif">📱 Notify</span>`      : "",
        ].filter(Boolean).join("");

        const row = document.createElement("div");
        row.className = "reminder-row";
        row.style.animationDelay = `${idx * 40}ms`;
        row.innerHTML = `
          <div class="reminder-row-route">${routeNum}</div>
          <div class="reminder-row-info">
            <div class="reminder-row-time">${fmtAmPm(r.arrivalTime)}</div>
            <div class="reminder-row-thresholds">Alerts at: ${thresholds}</div>
            <div style="display:flex;gap:6px;margin-top:5px;">${modes}</div>
          </div>
          <button class="reminder-row-remove" onclick="removeReminder(${r.id})" title="Remove">✕</button>
        `;
        list.appendChild(row);
      });
    }

    function removeReminder(id) {
      savedReminders = savedReminders.filter(r => r.id !== id);
      updateReminderBadge();
      renderRemindersList();
    }

    function updateReminderBadge() {
      const badge = document.getElementById("reminderBadge");
      if (savedReminders.length > 0) {
        badge.textContent    = savedReminders.length;
        badge.style.display  = "inline";
      } else {
        badge.style.display  = "none";
      }
    }

    // ── Saved reminders store ────────────────────────────────────
    let reminderChips = []; // array of { id, minutes }
    let chipIdCounter = 0;

    function selectArrival(cardEl, row) {
      // Remove bookmark from previously selected card
      document.querySelectorAll(".arrival-card.bookmarked")
        .forEach(c => c.classList.remove("bookmarked"));
      document.querySelectorAll(".arrival-card.selected")
        .forEach(c => c.classList.remove("selected"));
      cardEl.classList.add("selected");
      cardEl.classList.add("bookmarked");
      selectedArrival = row;
      setReminder(row);
    }

    function setReminder(row) {
      document.getElementById("rc-headsign").textContent    = row.stop_headsign;
      document.getElementById("rc-arrival-time").textContent = fmtAmPm(row.arrival_time);

      // Default chip: minutes until bus if not already set
      if (reminderChips.length === 0) {
        const d = minsUntil(row.arrival_time);
        const defaultMins = d > 0 ? Math.max(1, d - 5) : 15;
        reminderChips = [{ id: ++chipIdCounter, minutes: defaultMins }];
      }

      renderChips();
      document.getElementById("reminderCard").style.display = "block";
    }

    function renderChips() {
      const list = document.getElementById("reminderChipsList");
      list.innerHTML = "";
      reminderChips.forEach(chip => {
        const div = document.createElement("div");
        div.className = "reminder-chip";
        div.id = `chip-${chip.id}`;
        div.innerHTML = `
          <span class="reminder-chip-label" id="chip-label-${chip.id}">${chip.minutes} Minutes</span>
          <div class="reminder-chip-actions">
            <button class="chip-edit-btn" onclick="editChip(${chip.id})" title="Edit">✏️</button>
            <button class="chip-delete-btn" onclick="deleteChip(${chip.id})" title="Remove">✕</button>
          </div>
        `;
        list.appendChild(div);
      });
      // Hide + button when at max capacity
      const addBtn = document.querySelector(".add-chip-btn");
      if (addBtn) addBtn.style.display = reminderChips.length >= 3 ? "none" : "";
    }

    function editChip(id) {
      const chip = reminderChips.find(c => c.id === id);
      if (!chip) return;
      const labelEl = document.getElementById(`chip-label-${id}`);
      // Swap label for inline input
      labelEl.outerHTML = `
        <input class="chip-edit-input" id="chip-input-${id}"
          type="number" min="1" max="999"
          value="${chip.minutes}"
          onblur="saveChip(${id})"
          onkeydown="if(event.key==='Enter') saveChip(${id})"
        />
      `;
      document.getElementById(`chip-input-${id}`).focus();
      // Swap edit btn to save btn
      const editBtn = document.querySelector(`#chip-${id} .chip-edit-btn`);
      if (editBtn) {
        editBtn.textContent = "✓";
        editBtn.onclick = () => saveChip(id);
      }
    }

    function saveChip(id) {
      const input = document.getElementById(`chip-input-${id}`);
      if (!input) return;
      const val = parseInt(input.value, 10);
      if (!isNaN(val) && val > 0) {
        const chip = reminderChips.find(c => c.id === id);
        if (chip) chip.minutes = val;
      }
      renderChips();
    }

    function deleteChip(id) {
      reminderChips = reminderChips.filter(c => c.id !== id);
      renderChips();
    }

    function addReminderChip() {
      if (reminderChips.length >= 3) return; // max 3 reminders
      reminderChips.push({ id: ++chipIdCounter, minutes: 10 });
      renderChips();
      editChip(chipIdCounter);
    }

    // Holds all active setTimeout IDs so we can cancel them
    let scheduledTimers = [];

    function saveReminder() {
      if (!selectedArrival) return;

      const btn        = document.getElementById("saveReminderBtn");
      const confirmEl  = document.getElementById("saveConfirm");
      const smartOn    = document.getElementById("modeSmart").checked;
      const notifOn    = document.getElementById("modeNotif").checked;
      const gradChoice = document.getElementById("gradientA").classList.contains("active") ? "A" : "B";
      const colors     = GRADIENTS[gradChoice];
      const headsign   = selectedArrival.stop_headsign;

      // Clear any previously scheduled timers
      scheduledTimers.forEach(t => clearTimeout(t));
      scheduledTimers = [];

      // Sort chips descending (largest minutes first = furthest from bus)
      // then cap at 3
      const sortedChips = [...reminderChips]
        .sort((a, b) => b.minutes - a.minutes)
        .slice(0, 3);

      if (sortedChips.length === 0) {
        confirmEl.textContent = "⚠ Add at least one reminder time.";
        confirmEl.classList.add("visible");
        setTimeout(() => confirmEl.classList.remove("visible"), 3000);
        return;
      }

      const nowMins    = (() => {
        const n = new Date();
        return n.getHours() * 60 + n.getMinutes() + n.getSeconds() / 60;
      })();
      const busMins    = timeToMins(selectedArrival.arrival_time);

      // If Smart Light is on, fire the "turn on" webhook immediately
      if (smartOn) {
        triggerIFTTT(IFTTT_CONFIG.lightOnEvent, headsign);
      }

      // Schedule one action per chip threshold
      sortedChips.forEach((chip, index) => {
        // When should this fire? (bus arrival time minus chip.minutes)
        const fireMins   = busMins - chip.minutes;
        const delayMs    = Math.max(0, (fireMins - nowMins) * 60 * 1000);
        const color      = colors[Math.min(index, colors.length - 1)];
        const minsLabel  = chip.minutes;

        const tid = setTimeout(() => {
          if (smartOn) {
            const colorStr = `color: ${color}; brightness: ${IFTTT_CONFIG.lightBrightness}; transition_duration: ${IFTTT_CONFIG.lightTransitionDuration}`;
            triggerIFTTT(IFTTT_CONFIG.lightColorEvent, colorStr, `${minsLabel} min`, headsign);
          }
          if (notifOn) {
            triggerIFTTT(IFTTT_CONFIG.notifyEvent, headsign, `Your bus arrives in ${minsLabel} minutes!`);
          }
          console.log(`⏰ Reminder fired: ${minsLabel} min before bus — color ${color}`);
        }, delayMs);

        scheduledTimers.push(tid);
      });

      // Schedule light-off 5 minutes after the last (smallest) chip threshold
      if (smartOn) {
        const lastChip   = sortedChips[sortedChips.length - 1]; // smallest minutes
        const fireMins   = busMins - lastChip.minutes;
        const offDelayMs = Math.max(0, (fireMins - nowMins + 5) * 60 * 1000);
        const offTid     = setTimeout(() => {
          triggerIFTTT(IFTTT_CONFIG.lightOffEvent, headsign);
          console.log("💡 Smart light off");
        }, offDelayMs);
        scheduledTimers.push(offTid);
      }

      // UI feedback
      btn.classList.add("saved");
      btn.textContent = "✓ Saved";
      const modeList = [smartOn && "Smart Light", notifOn && "Notification"].filter(Boolean).join(" + ");
      confirmEl.textContent = `✓ ${sortedChips.length} reminder${sortedChips.length > 1 ? "s" : ""} scheduled${modeList ? " · " + modeList : ""}`;
      confirmEl.classList.add("visible");

      // Add to saved reminders list
      savedReminders.push({
        id:          ++savedReminderIdCounter,
        headsign:    selectedArrival.stop_headsign,
        arrivalTime: selectedArrival.arrival_time,
        chips:       sortedChips,
        smartOn,
        notifOn,
        gradChoice,
      });
      updateReminderBadge();

      setTimeout(() => {
        btn.classList.remove("saved");
        btn.textContent = "Save";
        confirmEl.classList.remove("visible");
      }, 4000);
    }

    function cancelReminder() {
      // Cancel all scheduled IFTTT timers
      scheduledTimers.forEach(t => clearTimeout(t));
      scheduledTimers = [];

      const btn     = document.getElementById("saveReminderBtn");
      const confirm = document.getElementById("saveConfirm");
      btn.classList.remove("saved");
      btn.textContent = "Save";
      confirm.classList.remove("visible");
      if (reminderInterval) clearInterval(reminderInterval);
      reminderInterval = null;
      selectedArrival = null;
      reminderChips = [];
      chipIdCounter = 0;
      document.getElementById("reminderCard").style.display = "none";
      document.querySelectorAll(".arrival-card.selected")
        .forEach(c => c.classList.remove("selected"));
      document.querySelectorAll(".arrival-card.bookmarked")
        .forEach(c => c.classList.remove("bookmarked"));
    }

    function selectGradient(choice) {
      document.getElementById("gradientA").classList.toggle("active", choice === "A");
      document.getElementById("gradientB").classList.toggle("active", choice === "B");
    }

    // Enter key support
    ["routeInput","stopInput"].forEach(id => {
      document.getElementById(id).addEventListener("keydown", e => {
        if (e.key === "Enter") runLookup();
      });
    });
  </script>
</body>
</html>
