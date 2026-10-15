@import url('https://fonts.googleapis.com/css2?family=DM+Mono:wght@400;500&family=DM+Sans:wght@400;500;600;700&display=swap');

:root {
  color-scheme: light;
  --page: #f5f5f6;
  --surface: #ffffff;
  --surface-soft: #f7f7f8;
  --surface-pressed: #eeeeef;
  --text: #202024;
  --muted: #85858e;
  --border: #e8e8eb;
  --accent: #a51f35;
  --accent-hover: #89182b;
  --accent-soft: #f8e9ec;
  --shadow: 0 14px 45px rgba(30, 30, 38, .055);
}
body[data-theme="slate"] { --page:#eef1f4; --surface:#fff; --surface-soft:#f5f7f9; --text:#202b38; --muted:#7d8996; --border:#e1e6eb; --accent:#344b65; --accent-hover:#26394f; --accent-soft:#e8edf3; }
body[data-theme="forest"] { --page:#f1f4f1; --surface:#fff; --surface-soft:#f6f8f6; --text:#202922; --muted:#7e8b80; --border:#e2e9e2; --accent:#315d43; --accent-hover:#244832; --accent-soft:#e8f1ea; }
body[data-theme="sand"] { --page:#f6f2ec; --surface:#fffdf9; --surface-soft:#faf6f0; --text:#302a24; --muted:#918679; --border:#ece4d9; --accent:#9b5438; --accent-hover:#80432d; --accent-soft:#f5eae3; }
* { box-sizing:border-box; }
body { margin:0; background:var(--page); color:var(--text); font-family:"DM Sans",Arial,sans-serif; min-height:100vh; transition:background .25s,color .25s; }
button,select { font:inherit; }
button { cursor:pointer; }
button:focus-visible,select:focus-visible { outline:3px solid color-mix(in srgb,var(--accent) 35%,transparent); outline-offset:2px; }
.app-shell { max-width:1160px; margin:0 auto; padding:26px 28px 18px; }
.topbar { display:flex; align-items:center; justify-content:space-between; gap:18px; margin-bottom:28px; }
.brand { display:flex; gap:11px; align-items:center; color:inherit; text-decoration:none; }
.brand-mark { width:43px; height:43px; display:grid; place-items:center; border-radius:13px; background:var(--accent); color:#fff; font-weight:700; font-size:22px; letter-spacing:-2px; box-shadow:0 5px 14px color-mix(in srgb,var(--accent) 20%,transparent); }
.brand-mark span { color:#f3c9d0; }
.brand strong { display:block; font-size:17px; letter-spacing:-.5px; }
.brand small { display:block; color:var(--muted); font-size:9px; letter-spacing:1.55px; margin-top:3px; }
.top-actions { display:flex; align-items:center; gap:10px; }
.setting-label,.eyebrow { font-size:10px; letter-spacing:1.55px; color:var(--muted); font-weight:700; margin:0; }
select { background:var(--surface); color:var(--text); border:1px solid var(--border); padding:10px 30px 10px 12px; border-radius:10px; }
.icon-button { display:flex; gap:7px; align-items:center; background:var(--surface); border:1px solid var(--border); border-radius:10px; padding:10px 12px; color:var(--text); font-size:12px; }
.icon-button.on { background:var(--accent-soft); border-color:color-mix(in srgb,var(--accent) 25%,var(--border)); color:var(--accent); }
.workspace { display:grid; grid-template-columns:minmax(0,1.55fr) minmax(280px,.85fr); gap:20px; align-items:stretch; }
.card { background:var(--surface); border:1px solid var(--border); border-radius:20px; box-shadow:var(--shadow); }
.calculator { padding:25px; }
.calc-heading,.history-heading { display:flex; justify-content:space-between; align-items:center; gap:14px; }
h1,h2,p { margin-top:0; }
h1 { font-size:23px; letter-spacing:-.8px; margin:6px 0 0; }
h2 { font-size:19px; letter-spacing:-.55px; margin:6px 0 0; }
.mode-switch { display:flex; background:var(--surface-soft); padding:4px; border-radius:11px; gap:3px; }
.mode-button { border:0; border-radius:8px; padding:9px 12px; color:var(--muted); background:transparent; font-size:12px; font-weight:600; transition:.18s; }
.mode-button.active { background:var(--surface); color:var(--accent); box-shadow:0 1px 4px #0000000b; }
.display { margin:24px 0 17px; min-height:125px; border:1px solid var(--border); background:var(--surface-soft); border-radius:15px; padding:15px 18px; display:flex; flex-direction:column; align-items:flex-end; justify-content:flex-end; overflow:hidden; }
.display-meta { width:100%; display:flex; justify-content:space-between; color:var(--muted); font-size:10px; letter-spacing:1.2px; font-weight:700; margin-bottom:auto; }
#angleMode { color:var(--accent); }
.expression { width:100%; text-align:right; font-family:"DM Mono",monospace; font-size:clamp(22px,3vw,32px); line-height:1.35; overflow-wrap:anywhere; letter-spacing:-1px; }
.result { min-height:22px; color:var(--accent); font-family:"DM Mono",monospace; font-size:15px; margin-top:4px; overflow-wrap:anywhere; }
.scientific-grid { display:grid; grid-template-columns:repeat(4,minmax(0,1fr)); gap:8px; margin-bottom:10px; animation:appear .2s ease-out; }
.hidden { display:none !important; }
.keypad { display:grid; grid-template-columns:repeat(5,minmax(0,1fr)); gap:9px; }
.key { border:1px solid transparent; min-height:53px; border-radius:12px; background:var(--surface-soft); color:var(--text); font-size:17px; font-weight:600; transition:transform .1s,background .16s,border-color .16s,box-shadow .16s; user-select:none; }
.key:hover { background:var(--surface-pressed); border-color:var(--border); }
.key:active { transform:scale(.96); }
.key.operator,.key.utility { background:var(--accent-soft); color:var(--accent); }
.key.operator:hover,.key.utility:hover { filter:brightness(.975); }
.key.function { min-height:40px; border-color:var(--border); background:var(--surface); color:var(--muted); font-size:13px; }
.key.function:hover { color:var(--accent); background:var(--accent-soft); }
.key.equals { background:var(--accent); color:white; box-shadow:0 5px 12px color-mix(in srgb,var(--accent) 20%,transparent); font-size:22px; }
.key.equals:hover { background:var(--accent-hover); }
.key.zero { grid-column:span 2; }
.calc-footer { display:flex; justify-content:space-between; gap:10px; margin-top:18px; padding-top:14px; border-top:1px solid var(--border); color:var(--muted); font-size:10px; }
.status-dot { display:inline-block; width:6px; height:6px; background:#4d9b6a; border-radius:50%; margin-right:5px; vertical-align:1px; }
.history { padding:25px 22px 18px; display:flex; flex-direction:column; min-height:100%; }
.text-button { border:0; background:transparent; color:var(--accent); font-size:12px; font-weight:600; padding:8px 0 8px 8px; }
.text-button:hover { text-decoration:underline; }
.history-intro { color:var(--muted); font-size:12px; line-height:1.5; margin:13px 0 16px; }
.history-list { display:flex; flex-direction:column; gap:9px; }
.history-item { border:1px solid var(--border); background:var(--surface); border-radius:12px; padding:12px 13px; cursor:pointer; transition:background .15s,border-color .15s,transform .15s; text-align:left; color:inherit; width:100%; }
.history-item:hover { background:var(--surface-soft); border-color:color-mix(in srgb,var(--accent) 28%,var(--border)); transform:translateY(-1px); }
.history-expression { color:var(--muted); font-family:"DM Mono",monospace; font-size:11px; overflow-wrap:anywhere; }
.history-result { font-family:"DM Mono",monospace; font-size:17px; font-weight:500; margin-top:6px; overflow-wrap:anywhere; }
.history-time { color:var(--muted); font-size:10px; margin-top:7px; }
.empty-state { flex:1; display:flex; align-items:center; justify-content:center; flex-direction:column; gap:8px; min-height:210px; text-align:center; color:var(--muted); }
.empty-icon { width:40px; height:40px; display:grid; place-items:center; border:1px solid var(--border); border-radius:13px; color:var(--accent); background:var(--accent-soft); font-size:20px; margin-bottom:4px; }
.empty-state strong { color:var(--text); font-size:13px; }
.empty-state span { font-size:11px; max-width:190px; line-height:1.5; }
.history-bottom { border-top:1px solid var(--border); padding-top:14px; margin-top:18px; display:flex; justify-content:space-between; gap:10px; font-size:10px; color:var(--muted); }
.page-footer { text-align:center; padding-top:24px; font-size:9px; letter-spacing:1.7px; color:var(--muted); }
.page-footer span { padding:0 7px; color:var(--accent); }
.toast { position:fixed; bottom:25px; left:50%; transform:translate(-50%,15px); opacity:0; pointer-events:none; background:#242428; color:#fff; padding:11px 16px; border-radius:10px; font-size:12px; box-shadow:0 8px 28px #0002; transition:opacity .2s,transform .2s; z-index:5; }
.toast.show { opacity:1; transform:translate(-50%,0); }
@keyframes appear { from{opacity:0;transform:translateY(-4px)} to{opacity:1;transform:translateY(0)} }
@media (max-width:820px) { .workspace { grid-template-columns:1fr; } .history { min-height:320px; } .history-list { max-height:360px; overflow:auto; } }
@media (max-width:520px) { .app-shell { padding:16px 12px; } .topbar { align-items:flex-start; margin-bottom:18px; } .top-actions { flex-wrap:wrap; justify-content:flex-end; gap:6px; } .setting-label { display:none; } .icon-button span { display:none; } .calculator { padding:16px 12px; border-radius:16px; } .history { padding:20px 16px; } .calc-heading { align-items:flex-start; flex-direction:column; } .mode-switch { width:100%; } .mode-button { flex:1; } .keypad { gap:6px; } .key { min-height:48px; border-radius:10px; } .scientific-grid { gap:6px; } .key.function { min-height:38px; } .calc-footer { font-size:9px; } .brand small { letter-spacing:1px; } }
