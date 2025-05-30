---
title: Neos Effects
category: Effects
---

# Neos-effects

the Neos-effects the Casoon UI Library bieten a Sammlung moderner, futuristischer Gestaltungselemente im Neon-Cyberpunk-Style, the Ihrer Benutzeroberflache a einzigartiges, futuristisches Aussehen verleihen.

## Uberblick

the Neos-effects combine leuchtende Colors, scharfe Kontraste and dynamische elements, um a futuristische Asthetik to schaffen. them eignen oneself hervorragend for moderne Web-Apps, Spieleoberflachen and Projekte with Cyberpunk- or Sci-Fi-Thematik.

## Installation

import them the Neos-effects-modules over CSS:

```css
@import '@casoon/ui-lib/effects/neos.css';
```

## Verfugbare classes

### Grundlegende Neos-elements

| Class | Description |
|--------|-------------|
| `.neos` | Grundlegende Neos-Stilisierung with leuchtenden Kanten |
| `.neos-text` | Text with Neos-Stilisierung |
| `.neos-border` | element with leuchtender Neos-Umrandung |
| `.neos-box` | box with Neos-Stilisierung |
| `.neos-card` | Card with Neos-Stilisierung |
| `.neos-button` | button with Neos-Stilisierung |

### Neos-Colors

| Class | Description |
|--------|-------------|
| `.neos-cyan` | Cyan-farbene Neos-Stilisierung |
| `.neos-magenta` | Magenta-farbene Neos-Stilisierung |
| `.neos-yellow` | Gelbe Neos-Stilisierung |
| `.neos-green` | Grune Neos-Stilisierung |
| `.neos-blue` | Blaue Neos-Stilisierung |
| `.neos-purple` | Violette Neos-Stilisierung |
| `.neos-red` | Rote Neos-Stilisierung |
| `.neos-orange` | Orange Neos-Stilisierung |
| `.neos-multi` | Mehrfarbige Neos-Stilisierung |

### Neos-effects

| Class | Description |
|--------|-------------|
| `.neos-glow` | Verstarkter Leuchteffekt |
| `.neos-pulse` | Pulsierender Leuchteffekt |
| `.neos-flicker` | Flackernder Leuchteffekt |
| `.neos-shadow` | Neos-Schatteneffekt |
| `.neos-scanline` | Scanline-effect for Retro-CRT-Look |
| `.neos-glitch` | Glitch-effect for digitale Storungen |
| `.neos-circuit` | Schaltkreis-pattern-effect |
| `.neos-grid` | Neos-Rasterhintergrund |
| `.neos-hologram` | Hologramm-ahnlicher effect |

### Neos-layouts

| Class | Description |
|--------|-------------|
| `.neos-containers` | containers with Neos-Stilisierung |
| `.neos-panel` | panel with Neos-Stilisierung |
| `.neos-terminal` | Terminal-ahnliches element |
| `.neos-dashboard` | Dashboard with Neos-Stilisierung |
| `.neos-hud` | Head-up-Display-Style |

## Examples

### Neos-button

```html
<button class="neos-button neos-cyan">
  <span class="neos-button-text">Neos button</span>
</button>

<style>
  .neos-button {
    padding: 0.8em 2em;
    border: 2px solid var(--neos-cyan-color);
    background-color: transparent;
    color: var(--neos-cyan-color);
    font-family: 'Rajdhani', sans-serif;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 1px;
    position: relative;
    overflow: hidden;
    transition: all 0.3s;
    box-shadow: 0 0 10px 0 var(--neos-cyan-glow);
  }
  
  .neos-button:before {
    content: "";
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(
      90deg,
      transparent,
      rgba(var(--neos-cyan-rgb), 0.4),
      transparent
    );
    transition: all 0.5s;
  }
  
  .neos-button:hover:before {
    left: 100%;
  }
  
  .neos-button:hover {
    background-color: rgba(var(--neos-cyan-rgb), 0.1);
    box-shadow: 0 0 20px 5px var(--neos-cyan-glow);
  }
</style>
```

### Neos-Card

```html
<div class="neos-card neos-purple">
  <div class="neos-card-header">
    <h3 class="neos-text">Neos Card</h3>
  </div>
  <div class="neos-card-body">
    <p>this content wird im futuristischen Neos-Style dargestellt.</p>
  </div>
  <div class="neos-card-footer">
    <button class="neos-button neos-purple">more erfahren</button>
  </div>
</div>

<style>
  .neos-card {
    background-color: rgba(10, 10, 15, 0.8);
    border: 1px solid var(--neos-purple-color);
    border-radius: 4px;
    box-shadow: 0 0 15px 0 var(--neos-purple-glow);
    padding: 0;
    overflow: hidden;
    max-width: 350px;
  }
  
  .neos-card-header {
    background-color: rgba(var(--neos-purple-rgb), 0.1);
    padding: 1rem;
    border-bottom: 1px solid var(--neos-purple-color);
  }
  
  .neos-card-body {
    padding: 1.5rem;
    color: #e0e0e0;
  }
  
  .neos-card-footer {
    padding: 1rem;
    border-top: 1px solid var(--neos-purple-color);
    text-align: right;
  }
</style>
```

### Neos-Terminal

```html
<div class="neos-terminal neos-green">
  <div class="neos-terminal-header">
    <div class="neos-terminal-controls">
      <span class="neos-terminal-control"></span>
      <span class="neos-terminal-control"></span>
      <span class="neos-terminal-control"></span>
    </div>
    <div class="neos-terminal-title">Terminal</div>
  </div>
  <div class="neos-terminal-body">
    <div class="neos-terminal-line">$ system_init</div>
    <div class="neos-terminal-line">Initialisiere system...</div>
    <div class="neos-terminal-line">Zugriff on Netzwerk hergestellt</div>
    <div class="neos-terminal-line">Status: Online</div>
    <div class="neos-terminal-line neos-terminal-cursor">$</div>
  </div>
</div>

<style>
  .neos-terminal {
    background-color: rgba(0, 0, 0, 0.9);
    border: 1px solid var(--neos-green-color);
    border-radius: 6px;
    box-shadow: 0 0 20px 0 var(--neos-green-glow);
    font-family: 'Source Code Pro', monospace;
    max-width: 600px;
    overflow: hidden;
  }
  
  .neos-terminal-header {
    background-color: rgba(var(--neos-green-rgb), 0.1);
    padding: 0.5rem 1rem;
    border-bottom: 1px solid var(--neos-green-color);
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .neos-terminal-controls {
    display: flex;
    gap: 8px;
  }
  
  .neos-terminal-control {
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background-color: #555;
  }
  
  .neos-terminal-control:first-child {
    background-color: #ff5f57;
  }
  
  .neos-terminal-control:nth-child(2) {
    background-color: #ffbd2e;
  }
  
  .neos-terminal-control:nth-child(3) {
    background-color: #28ca41;
  }
  
  .neos-terminal-title {
    color: var(--neos-green-color);
    font-size: 0.8rem;
  }
  
  .neos-terminal-body {
    padding: 1rem;
    color: var(--neos-green-color);
    min-height: 200px;
  }
  
  .neos-terminal-line {
    line-height: 1.5;
    margin-bottom: 0.5rem;
  }
  
  .neos-terminal-cursor:after {
    content: "■";
    animation: cursor-blink 1s infinite;
  }
  
  @keyframes cursor-blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
  }
</style>
```

### Neos-Dashboard

```html
<div class="neos-dashboard">
  <div class="neos-dashboard-header">
    <h2 class="neos-text neos-blue">Neos Dashboard</h2>
    <div class="neos-dashboard-controls">
      <button class="neos-button neos-blue neos-small">Refresh</button>
      <button class="neos-button neos-blue neos-small">Settings</button>
    </div>
  </div>
  
  <div class="neos-dashboard-grid">
    <div class="neos-panel neos-cyan">
      <div class="neos-panel-header">
        <h3 class="neos-text">system Status</h3>
      </div>
      <div class="neos-panel-body">
        <div class="neos-stat">
          <div class="neos-stat-label">CPU</div>
          <div class="neos-progress">
            <div class="neos-progress-bar" style="width: 65%"></div>
          </div>
          <div class="neos-stat-value">65%</div>
        </div>
        
        <div class="neos-stat">
          <div class="neos-stat-label">Memory</div>
          <div class="neos-progress">
            <div class="neos-progress-bar" style="width: 42%"></div>
          </div>
          <div class="neos-stat-value">42%</div>
        </div>
        
        <div class="neos-stat">
          <div class="neos-stat-label">Network</div>
          <div class="neos-progress">
            <div class="neos-progress-bar" style="width: 89%"></div>
          </div>
          <div class="neos-stat-value">89%</div>
        </div>
      </div>
    </div>
    
    <div class="neos-panel neos-magenta">
      <div class="neos-panel-header">
        <h3 class="neos-text">Aktivitat</h3>
      </div>
      <div class="neos-panel-body">
        <div class="neos-activity-log">
          <div class="neos-activity-item">
            <span class="neos-activity-time">10:42</span>
            <span class="neos-activity-text">system-Update abgeschlossen</span>
          </div>
          <div class="neos-activity-item">
            <span class="neos-activity-time">10:31</span>
            <span class="neos-activity-text">Neue Verbindung hergestellt</span>
          </div>
          <div class="neos-activity-item">
            <span class="neos-activity-time">10:15</span>
            <span class="neos-activity-text">Daten synchronisiert</span>
          </div>
        </div>
      </div>
    </div>
    
    <div class="neos-panel neos-yellow">
      <div class="neos-panel-header">
        <h3 class="neos-text">notifications</h3>
      </div>
      <div class="neos-panel-body">
        <div class="neos-notification">
          <div class="neos-notification-icon">!</div>
          <div class="neos-notification-content">
            <div class="neos-notification-title">system-warning</div>
            <div class="neos-notification-message">Speichernutzung over 80%</div>
          </div>
        </div>
        
        <div class="neos-notification">
          <div class="neos-notification-icon">i</div>
          <div class="neos-notification-content">
            <div class="neos-notification-title">info</div>
            <div class="neos-notification-message">5 neue Updates verfugbar</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  .neos-dashboard {
    background-color: rgba(10, 10, 20, 0.9);
    border: 1px solid var(--neos-blue-color);
    border-radius: 8px;
    box-shadow: 0 0 30px 0 var(--neos-blue-glow);
    overflow: hidden;
    padding: 1rem;
  }
  
  .neos-dashboard-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 1.5rem;
  }
  
  .neos-dashboard-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 1.5rem;
  }
  
  .neos-panel {
    background-color: rgba(0, 0, 0, 0.7);
    border: 1px solid;
    border-radius: 4px;
    overflow: hidden;
  }
  
  .neos-panel-header {
    padding: 0.8rem;
    border-bottom: 1px solid;
  }
  
  .neos-panel-body {
    padding: 1rem;
  }
  
  .neos-stat {
    display: flex;
    align-items: center;
    margin-bottom: 1rem;
    color: #e0e0e0;
  }
  
  .neos-stat-label {
    width: 80px;
  }
  
  .neos-progress {
    flex: 1;
    height: 6px;
    background-color: rgba(255, 255, 255, 0.1);
    border-radius: 3px;
    overflow: hidden;
  }
  
  .neos-progress-bar {
    height: 100%;
    background-color: currentColor;
  }
  
  .neos-stat-value {
    width: 50px;
    text-align: right;
  }
  
  .neos-activity-log {
    color: #e0e0e0;
  }
  
  .neos-activity-item {
    padding: 0.5rem 0;
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  }
  
  .neos-activity-time {
    font-weight: bold;
    margin-right: 0.5rem;
    color: var(--neos-magenta-color);
  }
  
  .neos-notification {
    display: flex;
    padding: 0.8rem;
    background-color: rgba(255, 255, 255, 0.05);
    border-radius: 4px;
    margin-bottom: 0.8rem;
    color: #e0e0e0;
  }
  
  .neos-notification-icon {
    width: 24px;
    height: 24px;
    border-radius: 50%;
    background-color: var(--neos-yellow-color);
    color: black;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    margin-right: 0.8rem;
  }
  
  .neos-notification-title {
    font-weight: bold;
    margin-bottom: 0.3rem;
  }
</style>
```

## Customization

the Neos-effects can over CSS Variables angepasst become:

```css
:root {
  /* Basisfarben */
  --neos-cyan-color: #00ffff;
  --neos-cyan-rgb: 0, 255, 255;
  --neos-cyan-glow: rgba(0, 255, 255, 0.6);
  
  --neos-magenta-color: #ff00ff;
  --neos-magenta-rgb: 255, 0, 255;
  --neos-magenta-glow: rgba(255, 0, 255, 0.6);
  
  --neos-yellow-color: #ffff00;
  --neos-yellow-rgb: 255, 255, 0;
  --neos-yellow-glow: rgba(255, 255, 0, 0.6);
  
  --neos-green-color: #00ff00;
  --neos-green-rgb: 0, 255, 0;
  --neos-green-glow: rgba(0, 255, 0, 0.6);
  
  --neos-blue-color: #0088ff;
  --neos-blue-rgb: 0, 136, 255;
  --neos-blue-glow: rgba(0, 136, 255, 0.6);
  
  --neos-purple-color: #9900ff;
  --neos-purple-rgb: 153, 0, 255;
  --neos-purple-glow: rgba(153, 0, 255, 0.6);
  
  --neos-red-color: #ff0055;
  --neos-red-rgb: 255, 0, 85;
  --neos-red-glow: rgba(255, 0, 85, 0.6);
  
  --neos-orange-color: #ff6600;
  --neos-orange-rgb: 255, 102, 0;
  --neos-orange-glow: rgba(255, 102, 0, 0.6);
  
  /* effect-parameter */
  --neos-glow-intensity: 0.7;
  --neos-pulse-speed: 2s;
  --neos-flicker-speed: 0.1s;
  --neos-scanline-size: 2px;
  --neos-scanline-speed: 3s;
  --neos-grid-size: 30px;
  
  /* Textschatten */
  --neos-text-shadow: 0 0 5px currentColor, 0 0 10px currentColor, 0 0 15px currentColor;
  
  /* background */
  --neos-bg-color: rgba(10, 10, 20, 0.95);
}
```

## Accessibility

at the Usage from Neos-Effekten should folgende Accessibilitysaspekte berucksichtigt become:

1. **Kontrast**: Stellen them despite leuchtender effects einen ausreichenden Kontrast sicher
2. **Flackernde effects**: Vermeiden them ubermassig flackernde effects for Menschen with Empfindlichkeiten
3. **Alternative Styles**: Bieten them a not-Neos version for Nutzer, the reduzierte Bewegung bevorzugen

```css
/* Alternative Styles for reduzierte Bewegung */
@media (prefers-reduced-motion: reduce) {
  .neos-pulse, 
  .neos-flicker, 
  .neos-scanline, 
  .neos-glitch {
    animation: none !important;
  }
  
  .neos-button:before {
    display: none;
  }
}

/* Verbesserter Kontrast for bessere Lesbarkeit */
.neos-text {
  font-weight: bold;
  text-shadow: 0 0 1px rgba(0, 0, 0, 0.5);
}
```

## Browser-Kompatibilitat

the Neos-effects become from allen modernen Browsern unterstutzt. for altere Browser become alternative Stiloptionen angeboten. 