<svg width="1200" height="300" viewBox="0 0 1200 300" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- Matrix Rain Gradient -->
    <linearGradient id="matrixGrad" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" style="stop-color:#00FF41;stop-opacity:0.15"/>
      <stop offset="50%" style="stop-color:#00FF41;stop-opacity:0.05"/>
      <stop offset="100%" style="stop-color:#0D1117;stop-opacity:0"/>
    </linearGradient>
    
    <!-- Neon Green Glow -->
    <filter id="neonGlow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="3" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    
    <!-- Electric Blue Glow -->
    <filter id="blueGlow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="4" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    
    <!-- Glitch Filter -->
    <filter id="glitch">
      <feTurbulence type="fractalNoise" baseFrequency="0.15 0.02" numOctaves="1" seed="2" result="noise">
        <animate attributeName="baseFrequency" values="0.15 0.02;0.2 0.03;0.15 0.02" dur="0.3s" repeatCount="indefinite"/>
      </feTurbulence>
      <feDisplacementMap in="SourceGraphic" in2="noise" scale="3" xChannelSelector="R" yChannelSelector="G"/>
    </filter>
    
    <!-- Scanline Pattern -->
    <pattern id="scanlines" width="4" height="4" patternUnits="userSpaceOnUse">
      <rect width="4" height="2" fill="rgba(0,0,0,0.3)"/>
    </pattern>
    
    <!-- Terminal Border -->
    <linearGradient id="borderGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#00FF41;stop-opacity:0.8"/>
      <stop offset="50%" style="stop-color:#00BFFF;stop-opacity:0.4"/>
      <stop offset="100%" style="stop-color:#00FF41;stop-opacity:0.8"/>
    </linearGradient>
    
    <!-- Data Stream Clip -->
    <clipPath id="terminalClip">
      <rect x="0" y="0" width="1200" height="300" rx="8"/>
    </clipPath>
  </defs>
  
  <!-- Background -->
  <rect width="1200" height="300" fill="#0D1117" rx="8"/>
  
  <!-- Matrix Data Stream Background -->
  <g opacity="0.15">
    <text x="50" y="0" fill="#00FF41" font-family="monospace" font-size="12">
      <animate attributeName="y" from="-200" to="350" dur="8s" repeatCount="indefinite"/>
      01101001 01101110 01101010 01100101 01100011 01110100
    </text>
    <text x="200" y="0" fill="#00FF41" font-family="monospace" font-size="10" opacity="0.6">
      <animate attributeName="y" from="-300" to="350" dur="12s" repeatCount="indefinite"/>
      72 6f 6f 74 40 6b 61 6c 69 3a 7e 24 20 73 71 6c 6d 61 70
    </text>
    <text x="450" y="0" fill="#00BFFF" font-family="monospace" font-size="11" opacity="0.4">
      <animate attributeName="y" from="-150" to="350" dur="6s" repeatCount="indefinite"/>
      Nmap scan report for 10.10.14.22 [Host is up]
    </text>
    <text x="700" y="0" fill="#00FF41" font-family="monospace" font-size="9" opacity="0.5">
      <animate attributeName="y" from="-250" to="350" dur="10s" repeatCount="indefinite"/>
      PORT STATE SERVICE VERSION 22/tcp open ssh OpenSSH 8.2p1
    </text>
    <text x="950" y="0" fill="#00BFFF" font-family="monospace" font-size="10" opacity="0.3">
      <animate attributeName="y" from="-180" to="350" dur="7s" repeatCount="indefinite"/>
      sqlmap identified injection point with technique B: boolean-based blind
    </text>
    <text x="100" y="0" fill="#00FF41" font-family="monospace" font-size="8" opacity="0.7">
      <animate attributeName="y" from="-400" to="350" dur="15s" repeatCount="indefinite"/>
      Burp Suite Professional v2024.1 - Proxy listening on 127.0.0.1:8080
    </text>
    <text x="600" y="0" fill="#00FF41" font-family="monospace" font-size="11" opacity="0.4">
      <animate attributeName="y" from="-100" to="350" dur="5s" repeatCount="indefinite"/>
      GET /login.php HTTP/1.1 Host: target.com User-Agent: Mozilla/5.0
    </text>
  </g>
  
  <!-- Scanline Overlay -->
  <rect width="1200" height="300" fill="url(#scanlines)" rx="8" opacity="0.5"/>
  
  <!-- Terminal Window Frame -->
  <rect x="2" y="2" width="1196" height="296" fill="none" stroke="url(#borderGrad)" stroke-width="2" rx="8" opacity="0.6"/>
  
  <!-- Terminal Header Bar -->
  <rect x="0" y="0" width="1200" height="28" fill="#0A0E14" rx="8"/>
  <rect x="0" y="14" width="1200" height="14" fill="#0A0E14"/>
  
  <!-- Window Control Buttons -->
  <circle cx="20" cy="14" r="5" fill="#FF5F56"/>
  <circle cx="38" cy="14" r="5" fill="#FFBD2E"/>
  <circle cx="56" cy="14" r="5" fill="#27C93F"/>
  
  <!-- Terminal Title -->
  <text x="600" y="18" text-anchor="middle" fill="#00FF41" font-family="monospace" font-size="11" opacity="0.7">
    askofu523@ByteSentinel:~/
  </text>
  
  <!-- Prompt Line 1 -->
  <g transform="translate(30, 70)">
    <text fill="#00FF41" font-family="'Courier New', monospace" font-size="14" filter="url(#neonGlow)">
      ┌──(root㉿kali)-[~]
    </text>
    <text fill="#00FF41" font-family="'Courier New', monospace" font-size="14">
      <animate attributeName="opacity" values="1;0;1" dur="0.8s" repeatCount="indefinite"/>
      █
    </text>
  </g>
  
  <!-- Prompt Line 2 with Animated Command -->
  <g transform="translate(30, 100)">
    <text fill="#00FF41" font-family="'Courier New', monospace" font-size="14">
      └─# ./recon.sh --target
    </text>
    <text fill="#00BFFF" font-family="'Courier New', monospace" font-size="14" font-weight="bold">
      <tspan>
        <animate attributeName="opacity" values="1;0.5;1" dur="2s" repeatCount="indefinite"/>
        BYTE_SENTINEL
      </tspan>
    </text>
  </g>
  
  <!-- Nmap Scan Simulation -->
  <g transform="translate(50, 135)" opacity="0.8">
    <text fill="#00FF41" font-family="'Courier New', monospace" font-size="12">
      [<tspan fill="#00BFFF">*</tspan>] Starting Nmap 7.94SVN at 2026-04-15 05:14 UTC
    </text>
    <text fill="#00FF41" font-family="'Courier New', monospace" font-size="12" opacity="0">
      [<tspan fill="#00BFFF">*</tspan>] Nmap scan report for target.local (10.10.14.22)
      <animate attributeName="opacity" values="0;0;1;1" dur="4s" repeatCount="indefinite" keyTimes="0;0.5;0.7;1"/>
    </text>
  </g>
  
  <!-- SQLMap Injection Scroll -->
  <g transform="translate(50, 170)" opacity="0">
    <text fill="#00BFFF" font-family="'Courier New', monospace" font-size="11">
      [INFO] testing connection to the target URL
    </text>
    <text fill="#00FF41" font-family="'Courier New', monospace" font-size="11">
      [<tspan fill="#FF5555">!</tspan>] detected back-end DBMS: MySQL &gt;= 5.0.12
    </text>
    <text fill="#00BFFF" font-family="'Courier New', monospace" font-size="11">
      [<tspan fill="#27C93F">+</tspan>] parameter 'id' appears to be injectable (boolean-based blind)
    </text>
    <animate attributeName="opacity" values="0;0;0;1;1;1;0;0;0" dur="12s" repeatCount="indefinite" keyTimes="0;0.15;0.25;0.35;0.5;0.6;0.7;0.85;1"/>
  </g>
  
  <!-- Burp Suite Activity -->
  <g transform="translate(700, 135)" opacity="0.6">
    <text fill="#00FF41" font-family="'Courier New', monospace" font-size="11">
      Burp Suite Professional v2025.1.2
    </text>
    <text fill="#888888" font-family="'Courier New', monospace" font-size="10">
      ─────────────────────────────────
    </text>
    <text fill="#00BFFF" font-family="'Courier New', monospace" font-size="10">
      Proxy <tspan fill="#27C93F">●</tspan> Running on 127.0.0.1:8080
    </text>
    <text fill="#00FF41" font-family="'Courier New', monospace" font-size="10">
      <tspan fill="#FFBD2E">→</tspan> GET /api/v1/users HTTP/1.1
    </text>
    <text fill="#00FF41" font-family="'Courier New', monospace" font-size="10" opacity="0">
      <tspan fill="#FF5F56">←</tspan> HTTP/1.1 200 OK (JSON)
      <animate attributeName="opacity" values="0;0;1;1;0;0" dur="6s" repeatCount="indefinite"/>
    </text>
  </g>
  
  <!-- Rotating Title Section -->
  <g transform="translate(600, 245)">
    <!-- Title Container -->
    <rect x="-350" y="-22" width="700" height="40" rx="4" fill="#0A0E14" opacity="0.8" stroke="#00FF41" stroke-width="0.5"/>
    
    <!-- Static Prefix -->
    <text x="-330" y="4" fill="#00FF41" font-family="'Courier New', monospace" font-size="16" font-weight="bold">
      $ role:=
    </text>
    
    <!-- Animated Rotating Titles -->
    <g transform="translate(-200, 4)">
      <!-- Title 1: Penetration Tester -->
      <text fill="#00FF41" font-family="'Courier New', monospace" font-size="16" font-weight="bold" filter="url(#neonGlow)" opacity="0">
        "Penetration Tester"
        <animate attributeName="opacity" values="1;1;0;0;0;0" dur="8s" repeatCount="indefinite" keyTimes="0;0.1;0.25;0.25;0.25;1"/>
      </text>
      
      <!-- Title 2: Red Team Operator -->
      <text fill="#FF5555" font-family="'Courier New', monospace" font-size="16" font-weight="bold" opacity="0">
        "Red Team Operator"
        <animate attributeName="opacity" values="0;0;1;1;0;0" dur="8s" repeatCount="indefinite" keyTimes="0;0.25;0.35;0.5;0.5;1"/>
      </text>
      
      <!-- Title 3: Bug Bounty Hunter -->
      <text fill="#FFBD2E" font-family="'Courier New', monospace" font-size="16" font-weight="bold" opacity="0">
        "Bug Bounty Hunter"
        <animate attributeName="opacity" values="0;0;0;0;1;1;0" dur="8s" repeatCount="indefinite" keyTimes="0;0.5;0.5;0.5;0.6;0.75;0.85"/>
      </text>
      
      <!-- Title 4: Web Security Researcher -->
      <text fill="#00BFFF" font-family="'Courier New', monospace" font-size="16" font-weight="bold" opacity="0" filter="url(#blueGlow)">
        "Web Security Researcher"
        <animate attributeName="opacity" values="0;0;0;0;0;0;1;1" dur="8s" repeatCount="indefinite" keyTimes="0;0.75;0.75;0.75;0.75;0.75;0.85;1"/>
      </text>
    </g>
    
    <!-- Blinking Cursor -->
    <text x="250" y="4" fill="#00FF41" font-family="'Courier New', monospace" font-size="18">
      <animate attributeName="opacity" values="1;0;1" dur="0.8s" repeatCount="indefinite"/>
      █
    </text>
  </g>
  
  <!-- HUD Elements - Corner Brackets -->
  <g opacity="0.4">
    <!-- Top Left -->
    <path d="M 15 15 L 15 35" stroke="#00FF41" stroke-width="1.5" fill="none"/>
    <path d="M 15 15 L 35 15" stroke="#00FF41" stroke-width="1.5" fill="none"/>
    
    <!-- Top Right -->
    <path d="M 1185 15 L 1185 35" stroke="#00FF41" stroke-width="1.5" fill="none"/>
    <path d="M 1165 15 L 1185 15" stroke="#00FF41" stroke-width="1.5" fill="none"/>
    
    <!-- Bottom Left -->
    <path d="M 15 285 L 15 265" stroke="#00FF41" stroke-width="1.5" fill="none"/>
    <path d="M 15 285 L 35 285" stroke="#00FF41" stroke-width="1.5" fill="none"/>
    
    <!-- Bottom Right -->
    <path d="M 1185 285 L 1185 265" stroke="#00FF41" stroke-width="1.5" fill="none"/>
    <path d="M 1165 285 L 1185 285" stroke="#00FF41" stroke-width="1.5" fill="none"/>
  </g>
  
  <!-- Status Bar -->
  <g transform="translate(0, 290)" opacity="0.5">
    <rect x="0" y="0" width="1200" height="10" fill="#0A0E14" rx="0 0 8 8"/>
    <text x="10" y="8" fill="#00FF41" font-family="monospace" font-size="8">
      [CONNECTED] <tspan fill="#00BFFF">10.10.14.22:443</tspan> | ENC: AES-256-GCM | <tspan fill="#FF5555">⏻ ACTIVE</tspan>
    </text>
    <text x="1190" y="8" text-anchor="end" fill="#888888" font-family="monospace" font-size="8">
      2026-04-15 05:14:32 UTC
    </text>
  </g>
  
  <!-- Glitch Overlay (occasional distortion) -->
  <rect x="0" y="0" width="1200" height="300" fill="none" opacity="0">
    <animate attributeName="opacity" values="0;0;0;0;0;0;0.3;0;0;0;0;0;0;0;0" dur="5s" repeatCount="indefinite"/>
  </rect>
</svg>
