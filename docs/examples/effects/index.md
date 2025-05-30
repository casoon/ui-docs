---
title: Effects Examples
category: Examples
outline: false
---

# Effects Examples

This page shows practical examples for using the Casoon UI Library Effects in real-world applications.

## Overview

The Effects modules of the Casoon UI Library offer a variety of visual effects and animations that can enhance your user interface. Here you'll find concrete implementation examples that show how these effects can be used in different scenarios.

## 3D Transformations

### Interactive Card with 3D Flip Effect

```html
<div class="card-container transform-3d perspective preserve-3d">
  <div class="card flip-3d">
    <div class="card-front">
      <div class="card-header">
        <h3>Product Information</h3>
      </div>
      <div class="card-body">
        <p>Here are the basic information about the product.</p>
        <button class="button primary">More Details</button>
      </div>
    </div>
    <div class="card-back">
      <div class="card-header accent">
        <h3>Detailed Specifications</h3>
      </div>
      <div class="card-body">
        <ul>
          <li>Technical Details</li>
          <li>Dimensions and Weight</li>
          <li>Materials</li>
        </ul>
        <button class="button">Back</button>
      </div>
    </div>
  </div>
</div>

<style>
  .card-container {
    width: 300px;
    height: 400px;
    margin: 2rem auto;
    cursor: pointer;
  }
  
  .card {
    width: 100%;
    height: 100%;
    position: relative;
    transition: transform 0.8s;
    transform-style: preserve-3d;
  }
  
  .card-container:hover .card {
    transform: rotateY(180deg);
  }
  
  .card-front, .card-back {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
    border-radius: 0.5rem;
    box-shadow: var(--shadow-md);
    overflow: hidden;
  }
  
  .card-back {
    transform: rotateY(180deg);
    background-color: var(--color-background-alt);
  }
  
  .card-header {
    padding: 1rem;
    background-color: var(--color-primary);
    color: white;
  }
  
  .card-header.accent {
    background-color: var(--color-accent);
  }
  
  .card-body {
    padding: 1.5rem;
  }
</style>
```

## Neon Effects

### Interactive Dashboard with Neon Accents

```html
<div class="dashboard theme-night">
  <div class="dashboard-header">
    <h2 class="neon-text-blue">system Status</h2>
    <div class="dashboard-controls">
      <button class="neon-border-blue neon-border-hover">Refresh</button>
      <button class="neon-border-blue neon-border-hover">Settings</button>
    </div>
  </div>
  
  <div class="dashboard-grid">
    <div class="dashboard-card">
      <h3>CPU Usage</h3>
      <div class="metric">
        <div class="metric-value neon-text-blue">42%</div>
        <div class="metric-bar">
          <div class="metric-fill neon-glow-blue" style="width: 42%"></div>
        </div>
      </div>
    </div>
    
    <div class="dashboard-card">
      <h3>Memory</h3>
      <div class="metric">
        <div class="metric-value neon-text-purple">78%</div>
        <div class="metric-bar">
          <div class="metric-fill neon-glow-purple" style="width: 78%"></div>
        </div>
      </div>
    </div>
    
    <div class="dashboard-card">
      <h3>Network</h3>
      <div class="metric">
        <div class="metric-value neon-text-teal">63%</div>
        <div class="metric-bar">
          <div class="metric-fill neon-glow-teal" style="width: 63%"></div>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  .dashboard {
    background-color: #121212;
    border-radius: 0.5rem;
    padding: 1.5rem;
    color: #e0e0e0;
  }
  
  .dashboard-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 2rem;
  }
  
  .dashboard-controls {
    display: flex;
    gap: 1rem;
  }
  
  .dashboard-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 1.5rem;
  }
  
  .dashboard-card {
    background-color: #1e1e1e;
    border-radius: 0.5rem;
    padding: 1.5rem;
  }
  
  .metric {
    margin-top: 1rem;
  }
  
  .metric-value {
    font-size: 2rem;
    font-weight: bold;
    margin-bottom: 0.5rem;
  }
  
  .metric-bar {
    height: 8px;
    background-color: rgba(255, 255, 255, 0.1);
    border-radius: 4px;
    overflow: hidden;
  }
  
  .metric-fill {
    height: 100%;
    border-radius: 4px;
  }
  
  button {
    background-color: transparent;
    color: #e0e0e0;
    border: 1px solid;
    padding: 0.5rem 1rem;
    border-radius: 0.25rem;
    cursor: pointer;
    transition: all 0.2s;
  }
</style>
```

## Loading Animations

### Multi-stage Loading Process with Visual Progress Indicator

```html
<div class="upload-process">
  <h3>Upload Files</h3>
  
  <div class="progress-steps">
    <div class="progress-step completed">
      <div class="step-indicator">
        <div class="spinner-dots"></div>
        <div class="step-check">✓</div>
      </div>
      <div class="step-details">
        <div class="step-name">Select Files</div>
        <div class="step-info">3 files selected</div>
      </div>
    </div>
    
    <div class="progress-step active">
      <div class="step-indicator">
        <div class="spinner-dots"></div>
      </div>
      <div class="step-details">
        <div class="step-name">Compression</div>
        <div class="step-info">Optimizing files...</div>
        <div class="progress">
          <div class="progress-bar progress-bar-animated" style="width: 65%">65%</div>
        </div>
      </div>
    </div>
    
    <div class="progress-step">
      <div class="step-indicator">
        <div class="step-number">3</div>
      </div>
      <div class="step-details">
        <div class="step-name">Upload</div>
        <div class="step-info">Waiting for compression...</div>
      </div>
    </div>
    
    <div class="progress-step">
      <div class="step-indicator">
        <div class="step-number">4</div>
      </div>
      <div class="step-details">
        <div class="step-name">Processing</div>
        <div class="step-info">Waiting for upload...</div>
      </div>
    </div>
  </div>
  
  <div class="upload-actions">
    <button class="button outline">Cancel</button>
    <button class="button primary" disabled>Continue</button>
  </div>
</div>

<style>
  .upload-process {
    max-width: 600px;
    margin: 0 auto;
    padding: 2rem;
    border-radius: 0.5rem;
    background-color: white;
    box-shadow: var(--shadow-md);
  }
  
  .progress-steps {
    margin: 2rem 0;
  }
  
  .progress-step {
    display: flex;
    margin-bottom: 1.5rem;
  }
  
  .step-indicator {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background-color: var(--color-gray-100);
    display: flex;
    align-items: center;
    justify-content: center;
    margin-right: 1rem;
    flex-shrink: 0;
    position: relative;
  }
  
  .progress-step.completed .step-indicator {
    background-color: var(--color-success-100);
    color: var(--color-success);
  }
  
  .progress-step.active .step-indicator {
    background-color: var(--color-primary-100);
    color: var(--color-primary);
  }
  
  .step-check {
    display: none;
  }
  
  .progress-step.completed .spinner-dots {
    display: none;
  }
  
  .progress-step.completed .step-check {
    display: block;
    font-weight: bold;
  }
  
  .step-details {
    flex: 1;
  }
  
  .step-name {
    font-weight: bold;
    margin-bottom: 0.25rem;
  }
  
  .step-info {
    color: var(--color-gray-600);
    font-size: 0.875rem;
    margin-bottom: 0.5rem;
  }
  
  .progress {
    height: 8px;
    background-color: var(--color-gray-100);
    border-radius: 4px;
    overflow: hidden;
    margin-top: 0.5rem;
  }
  
  .progress-bar {
    height: 100%;
    background-color: var(--color-primary);
    border-radius: 4px;
  }
  
  .upload-actions {
    display: flex;
    justify-content: flex-end;
    gap: 1rem;
    margin-top: 1rem;
  }
  
  .button {
    padding: 0.5rem 1rem;
    border-radius: 0.25rem;
    font-weight: 500;
    cursor: pointer;
    border: none;
  }
  
  .button.outline {
    background-color: transparent;
    border: 1px solid var(--color-gray-300);
    color: var(--color-gray-700);
  }
  
  .button.primary {
    background-color: var(--color-primary);
    color: white;
  }
  
  .button[disabled] {
    opacity: 0.6;
    cursor: not-allowed;
  }
</style>
```

## More Examples

Discover more effects in the individual documentation pages:

- [3D Effects](/effects/3d)
- [Gradient Effects](/effects/gradient)
- [Neon Effects](/effects/neon)
- [Patterns & Textures](/effects/patterns)
- [Glass Effects](/effects/glass)
- [Shadow Effects](/effects/shadows)
- [Loading Effects](/effects/state/loading) 