<div align="center">

<svg width="1200" height="300" viewBox="0 0 1200 300" xmlns="http://www.w3.org/2000/svg">

  <defs>
    <linearGradient id="matrixGrad" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" style="stop-color:#00FF41;stop-opacity:0.15"/>
      <stop offset="50%" style="stop-color:#00FF41;stop-opacity:0.05"/>
      <stop offset="100%" style="stop-color:#0D1117;stop-opacity:0"/>
    </linearGradient>

    <filter id="neonGlow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="3" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <filter id="blueGlow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="4" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <pattern id="scanlines" width="4" height="4" patternUnits="userSpaceOnUse">
      <rect width="4" height="2" fill="rgba(0,0,0,0.3)"/>
    </pattern>

    <linearGradient id="borderGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#00FF41;stop-opacity:0.8"/>
      <stop offset="50%" style="stop-color:#00BFFF;stop-opacity:0.4"/>
      <stop offset="100%" style="stop-color:#00FF41;stop-opacity:0.8"/>
    </linearGradient>

  </defs>

  <!-- Background -->
  <rect width="1200" height="300" fill="#0D1117" rx="8"/>

  <!-- Scanlines -->
  <rect width="1200" height="300" fill="url(#scanlines)" opacity="0.4"/>

  <!-- Border -->
  <rect x="2" y="2" width="1196" height="296" fill="none"
        stroke="url(#borderGrad)" stroke-width="2" rx="8"/>

  <!-- Terminal Header -->
  <text x="600" y="40" text-anchor="middle"
        fill="#00FF41" font-family="monospace" font-size="20">
    askofu523@ByteSentinel:~ penetration testing lab
  </text>

  <!-- Main Title -->
  <text x="600" y="160" text-anchor="middle"
        fill="#00FF41" font-family="monospace" font-size="28"
        filter="url(#neonGlow)">
    Penetration Tester | Red Team | Bug Bounty Hunter
  </text>

  <!-- Subtitle -->
  <text x="600" y="200" text-anchor="middle"
        fill="#00BFFF" font-family="monospace" font-size="16">
    Web Security • Burp Suite • OWASP • OSINT • Exploitation
  </text>

  <!-- Blinking Cursor -->
  <text x="860" y="200" fill="#00FF41" font-size="18">
    █
    <animate attributeName="opacity" values="1;0;1" dur="0.8s" repeatCount="indefinite"/>
  </text>

</svg>

</div>
