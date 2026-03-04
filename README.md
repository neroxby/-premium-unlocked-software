# -premium-unlocked-software
Runs silently in background and Connects to attacker’s server.
# xWorm V6 –
This is a single HTML file that creates a dark, green neon cyber dashboard — like a control panel you might see in a hacker movie or cybersecurity tool demo.
**Important note at the start:**  
This is **100% visual and local only**.  
It runs completely inside your web browser.  
It does **not** harm your computer.  
## What You See When You Open It
1. **Dark black background** with soft green glowing circles (like matrix rain style)
   - Status box on the right: starts as "OFFLINE" (red background)  
3. **Left sidebar** (narrow column)  
   - "CONTROL" section with big buttons:  
     - Connect  
     - Keylogger  
     - Screen Capture
     - Ransomware (red danger button)  
   - "PLUGINS • V6.4" section showing plugin names like Stealer.dll, RemoteShell.dll, etc.
4. **Main area (right side)**  
   - Big black log box that shows messages with timestamps and colors (green = normal, yellow = warning, red = error)  
   - one statistic cards:  
     - "Targets Online" → starts at 0 
## How to Use It
1. Create a new file on your computer called `index.html`  
2. Copy the full code (from the repo or previous messages) and paste it into that file  
3. Save it  
4. Double-click the file — it opens in your browser automatically  
5. (Best experience: open in Firefox or LibreWolf)
No installation. No internet needed after you save the file.
## Step-by-Step: What Happens When You Click Things
### 1. Click "Connect"
- Log shows: "[time] Connecting to C2..." (green)  
- Waits about 1–2 seconds  
- Status changes from "OFFLINE" (red) → "ONLINE" (green box)  
- one numbers jump up randomly:  
  - Targets Online → e.g. 3 to 10  
### 2. Click any action button (Keylogger, Screen Capture, Ransomware)
- First check: if status is still "OFFLINE" → log says "No active connection" in red → stops  
- If "ONLINE":  
  - Log shows yellow warning: "Executing [name] module..."  
  - Waits 1–2 seconds  
  - Then shows success message in green:  
    - Normal buttons → "[name] completed"  
    - system Extract → special message like "extraction → 2 profiles located" (random number)  
    - Ransomware → "Ransomware module activated" in red (scary look)  

**How code does this:** One function called `execute(action)` checks status, adds log lines with colors, uses another timer, and has if-statements for special messages.
### 3. Automatic messages when page loads
- After \~0.6 seconds: green log "Loading plugin set: Stealer • RemoteShell .
- After \~1.2 seconds: yellow log "Persistence layer initialized"  
**How:** Two small timers at the bottom of the script run as soon as the page opens.
### 4. The log box
- Every message gets added at the bottom  
- Automatically scrolls down so you always see the newest line  
- Different colors help read fast: green=info, yellow=warning, red=error  
**How:** Helper function `addLog(txt, type)` creates a new line `<div>`, adds color class, puts it in log, then forces scroll to bottom.
## Plugins List
- Stealer.dll  
- RemoteShell.dll  
- FileManager.dll  
- RDP.dll  
- Recovery.dll  
- Chromium.dll  
- SystemCheck.dll  
- WindowsUpdate.dll  
In real XWorm (from security blogs like Trellix, TheHackerNews, Picus Security):  
- It has **35+ plugins** loaded from memory  
- Examples: RemoteDesktop.dll (remote control), Stealer.dll (steal passwords/Wi-Fi), FileManager.dll (browse files), ransomware plugin (encrypt files with AES)  
- Plugins make it modular — attacker can add/remove features remotely  
## Why Make This?
- Practice cyber aesthetic design (dark mode, neon, logs, status)  
- Show how real malware panels **might** look (without any danger)  
- Good for portfolios, CTF writeups.
- **Change colors**  
  Look for `:root {` at top of `<style>`  
  Example: `--accent: #00ff41;` → change to `#ff00ff` for purple  
- **Add more buttons**  
  In sidebar `<div class="panel">`, copy-paste a `<button>` line:  
  ```html
  contact with me on telegram
  https://t.me/H16kM4w
