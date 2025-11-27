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

<h2>3. System Cleanup & Optimization</h2>
<ul>
  <li><code>cleanmgr</code></li>
  <li><code>prefetch</code></li>
  <li><code>%temp%</code></li>
  <li><code>temp</code></li>
  <li><code>tree</code></li>
  <li><code>sfc /scannow</code></li>
  <li><code>Dism /Online /Cleanup-Image /RestoreHealth</code></li>
  <li><code>chkdsk C: /f</code></li>
  <li><code>powercfg /batteryreport</code></li>
  <li><code>powercfg /energy</code></li>
</ul>

<h2>4. File System & Directory</h2>
<ul>
  <li><code>dir</code></li>
  <li><code>dir /s</code></li>
  <li><code>cd</code></li>
  <li><code>cd ..</code></li>
  <li><code>copy</code></li>
  <li><code>move</code></li>
  <li><code>del</code></li>
  <li><code>rmdir /S</code></li>
  <li><code>mkdir</code></li>
  <li><code>attrib</code></li>
</ul>

