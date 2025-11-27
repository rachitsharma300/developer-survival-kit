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

<h2>5. Dev Environment & Tools</h2>
<ul>
  <li><code>java -version</code></li>
  <li><code>javac -version</code></li>
  <li><code>mvn -v</code></li>
  <li><code>gradle -v</code></li>
  <li><code>node -v</code></li>
  <li><code>npm -v</code></li>
  <li><code>npx create-react-app myapp</code></li>
  <li><code>npm start</code></li>
  <li><code>where java</code></li>
  <li><code>where node</code></li>
</ul>

<h2>6. Network Device Control</h2>
<ul>
  <li><code>netsh interface show interface</code></li>
  <li><code>netsh interface set interface name="Wi-Fi" admin=ENABLE</code></li>
  <li><code>netsh interface set interface name="Wi-Fi" admin=DISABLE</code></li>
  <li><code>netstat -e</code></li>
  <li><code>net statistics workstation</code></li>
</ul>


<h2>7. Firewall Commands</h2>
<ul>
  <li><code>netsh advfirewall show allprofiles</code></li>
  <li><code>netsh advfirewall export firewall.wfw</code></li>
  <li><code>netsh advfirewall import firewall.wfw</code></li>
  <li><code>netsh advfirewall firewall add rule name="Open Port 8080" dir=in action=allow protocol=TCP localport=8080</code></li>
  <li><code>netsh advfirewall firewall delete rule name="Open Port 8080"</code></li>
</ul>

<h2>8. System Info Commands</h2>
<ul>
  <li><code>systeminfo</code></li>
  <li><code>hostname</code></li>
  <li><code>whoami</code></li>
  <li><code>wmic cpu get name</code></li>
  <li><code>wmic memorychip get capacity</code></li>
  <li><code>wmic logicaldisk get size,freespace,caption</code></li>
  <li><code>wmic os get caption</code></li>
  <li><code>taskmgr</code></li>
  <li><code>perfmon</code></li>
  <li><code>msinfo32</code></li>
</ul>


<h2>9. Windows Services</h2>
<ul>
  <li><code>services.msc</code></li>
  <li><code>sc query</code></li>
  <li><code>sc stop &lt;service-name&gt;</code></li>
  <li><code>sc start &lt;service-name&gt;</code></li>
  <li><code>sc delete &lt;service-name&gt;</code></li>
</ul>
