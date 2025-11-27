<h1>100 Most Used Windows Commands for Developers</h1>

<h2>1. Network & Internet Commands</h2>
<ul>
  <li><code>ipconfig</code></li>
  <li><code>ipconfig /all</code></li>
  <li><code>ipconfig /flushdns</code></li>
  <li><code>ipconfig /release</code></li>
  <li><code>ipconfig /renew</code></li>
  <li><code>ipconfig /displaydns</code></li>
  <li><code>netsh winsock reset</code></li>
  <li><code>netsh int ip reset</code></li>
  <li><code>netsh advfirewall reset</code></li>
  <li><code>netsh advfirewall set allprofiles state off</code></li>
  <li><code>netsh advfirewall set allprofiles state on</code></li>
  <li><code>netsh wlan show profiles</code></li>
  <li><code>netsh wlan show profile name=&lt;wifi&gt; key=clear</code></li>
  <li><code>ping google.com</code></li>
  <li><code>ping 8.8.8.8</code></li>
  <li><code>tracert google.com</code></li>
  <li><code>pathping google.com</code></li>
  <li><code>nslookup google.com</code></li>
  <li><code>getmac</code></li>
  <li><code>arp -a</code></li>
</ul>

<h2>2. Port & Process Commands</h2>
<ul>
  <li><code>netstat -ano</code></li>
  <li><code>netstat -aon | findstr :8080</code></li>
  <li><code>tasklist</code></li>
  <li><code>taskkill /PID &lt;pid&gt; /F</code></li>
  <li><code>taskkill /IM chrome.exe /F</code></li>
  <li><code>wmic process list brief</code></li>
  <li><code>wmic process where "name='java.exe'" get ProcessId</code></li>
</ul>

