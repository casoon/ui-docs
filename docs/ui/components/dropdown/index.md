---
title: Dropdown Component
outline: deep
---


# Dropdown

the Dropdown-component ermoglicht the Anzeige einer versteckten list from Optionen, the at Aktivierung sichtbar wird. these component ist ideal for Navigationsmenus, Filteroptionen and others interaktive elements.

## Installation

the Dropdown-component ist Teil the Casoon UI Library.

```bash
# Installation the gesamten Bibliothek
npm install @casoon/ui-lib
```

## Import

```css
/* Import aller UI-Components */
@import '@casoon/ui-lib/ui.css';

/* or only the Dropdown-component */
@import '@casoon/ui-lib/ui/components/dropdown.css';
```

## Basic Usage

```html
<div class="dropdown">
  <button class="dropdown__trigger button">
    Dropdown offnen
    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <polyline points="6 9 12 15 18 9"></polyline>
    </svg>
  </button>
  <div class="dropdown__menu">
    <a href="#" class="dropdown__item">Option 1</a>
    <a href="#" class="dropdown__item">Option 2</a>
    <a href="#" class="dropdown__item">Option 3</a>
  </div>
</div>
```

<div class="example-wrappers">
  <div style="position: relative; display: inline-block;">
    <button style="display: flex; align-items: center; gap: 0.5rem; padding: 0.5rem 1rem; background-color: #3b82f6; color: white; border: none; border-radius: 0.375rem; cursor: pointer; font-weight: 500;">
      Dropdown offnen
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <polyline points="6 9 12 15 18 9"></polyline>
      </svg>
    </button>
    <div style="position: absolute; top: 100%; left: 0; margin-top: 0.5rem; min-width: 10rem; background-color: white; border: 1px solid #e5e7eb; border-radius: 0.375rem; box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1); z-index: 10;">
      <a href="#" style="display: block; padding: 0.5rem 1rem; color: #374151; text-decoration: none; hover:background-color: #f3f4f6;">Option 1</a>
      <a href="#" style="display: block; padding: 0.5rem 1rem; color: #374151; text-decoration: none; hover:background-color: #f3f4f6;">Option 2</a>
      <a href="#" style="display: block; padding: 0.5rem 1rem; color: #374151; text-decoration: none; hover:background-color: #f3f4f6;">Option 3</a>
    </div>
  </div>
</div>

## Variants

### with Trennlinien

```html
<div class="dropdown">
  <button class="dropdown__trigger button">Aktionen</button>
  <div class="dropdown__menu">
    <a href="#" class="dropdown__item">Bearbeiten</a>
    <a href="#" class="dropdown__item">Duplizieren</a>
    <div class="dropdown__divider"></div>
    <a href="#" class="dropdown__item dropdown__item--danger">delete</a>
  </div>
</div>
```

<div class="example-wrappers">
  <div style="position: relative; display: inline-block;">
    <button style="display: flex; align-items: center; gap: 0.5rem; padding: 0.5rem 1rem; background-color: #3b82f6; color: white; border: none; border-radius: 0.375rem; cursor: pointer; font-weight: 500;">
      Aktionen
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <polyline points="6 9 12 15 18 9"></polyline>
      </svg>
    </button>
    <div style="position: absolute; top: 100%; left: 0; margin-top: 0.5rem; min-width: 10rem; background-color: white; border: 1px solid #e5e7eb; border-radius: 0.375rem; box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1); z-index: 10;">
      <a href="#" style="display: block; padding: 0.5rem 1rem; color: #374151; text-decoration: none; hover:background-color: #f3f4f6;">Bearbeiten</a>
      <a href="#" style="display: block; padding: 0.5rem 1rem; color: #374151; text-decoration: none; hover:background-color: #f3f4f6;">Duplizieren</a>
      <div style="height: 1px; background-color: #e5e7eb; margin: 0.25rem 0;"></div>
      <a href="#" style="display: block; padding: 0.5rem 1rem; color: #ef4444; text-decoration: none; hover:background-color: #f3f4f6;">delete</a>
    </div>
  </div>
</div>

### With icons

```html
<div class="dropdown">
  <button class="dropdown__trigger button">Menu</button>
  <div class="dropdown__menu">
    <a href="#" class="dropdown__item">
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <path d="M11 4H4a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"></path>
        <path d="M18.5 2.5a2.121 2.121 0 0 1 3 3L12 15l-4 1 1-4 9.5-9.5z"></path>
      </svg>
      Bearbeiten
    </a>
    <a href="#" class="dropdown__item">
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect>
        <path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path>
      </svg>
      Kopieren
    </a>
    <a href="#" class="dropdown__item">
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"></path>
        <polyline points="17 8 12 3 7 8"></polyline>
        <line x1="12" y1="3" x2="12" y2="15"></line>
      </svg>
      Herunterladen
    </a>
  </div>
</div>
```

<div class="example-wrappers">
  <div style="position: relative; display: inline-block;">
    <button style="display: flex; align-items: center; gap: 0.5rem; padding: 0.5rem 1rem; background-color: #3b82f6; color: white; border: none; border-radius: 0.375rem; cursor: pointer; font-weight: 500;">
      Menu
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <polyline points="6 9 12 15 18 9"></polyline>
      </svg>
    </button>
    <div style="position: absolute; top: 100%; left: 0; margin-top: 0.5rem; min-width: 10rem; background-color: white; border: 1px solid #e5e7eb; border-radius: 0.375rem; box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1); z-index: 10;">
      <a href="#" style="display: flex; align-items: center; gap: 0.5rem; padding: 0.5rem 1rem; color: #374151; text-decoration: none; hover:background-color: #f3f4f6;">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M11 4H4a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"></path>
          <path d="M18.5 2.5a2.121 2.121 0 0 1 3 3L12 15l-4 1 1-4 9.5-9.5z"></path>
        </svg>
        Bearbeiten
      </a>
      <a href="#" style="display: flex; align-items: center; gap: 0.5rem; padding: 0.5rem 1rem; color: #374151; text-decoration: none; hover:background-color: #f3f4f6;">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect>
          <path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path>
        </svg>
        Kopieren
      </a>
      <a href="#" style="display: flex; align-items: center; gap: 0.5rem; padding: 0.5rem 1rem; color: #374151; text-decoration: none; hover:background-color: #f3f4f6;">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"></path>
          <polyline points="17 8 12 3 7 8"></polyline>
          <line x1="12" y1="3" x2="12" y2="15"></line>
        </svg>
        Herunterladen
      </a>
    </div>
  </div>
</div>

## Usagesbeispiele

### Navigationsmenu

```html
<nav class="navbar">
  <div class="navbar__brand">Meine Website</div>
  <div class="navbar__menu">
    <a href="#" class="navbar__link">Home</a>
    <a href="#" class="navbar__link">over us</a>
    <div class="dropdown">
      <button class="dropdown__trigger navbar__link">
        Produkte
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <polyline points="6 9 12 15 18 9"></polyline>
        </svg>
      </button>
      <div class="dropdown__menu">
        <a href="#" class="dropdown__item">category 1</a>
        <a href="#" class="dropdown__item">category 2</a>
        <a href="#" class="dropdown__item">category 3</a>
      </div>
    </div>
    <a href="#" class="navbar__link">Kontakt</a>
  </div>
</nav>
```

<div class="example-wrappers">
  <div style="display: flex; align-items: center; justify-content: space-between; padding: 1rem; background-color: #f9fafb; border-radius: 0.5rem; width: 100%; max-width: 700px; border: 1px solid #e5e7eb;">
    <div style="font-weight: 600; font-size: 1.25rem; color: #111827;">Meine Website</div>
    <div style="display: flex; gap: 1.5rem; align-items: center;">
      <a href="#" style="color: #374151; text-decoration: none; font-weight: 500;">Home</a>
      <a href="#" style="color: #374151; text-decoration: none; font-weight: 500;">over us</a>
      <div style="position: relative;">
        <button style="display: flex; align-items: center; gap: 0.5rem; background: none; border: none; color: #374151; font-weight: 500; cursor: pointer; padding: 0;">
          Produkte
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <polyline points="6 9 12 15 18 9"></polyline>
          </svg>
        </button>
        <div style="position: absolute; top: 100%; left: 0; margin-top: 0.5rem; min-width: 10rem; background-color: white; border: 1px solid #e5e7eb; border-radius: 0.375rem; box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1); z-index: 10;">
          <a href="#" style="display: block; padding: 0.5rem 1rem; color: #374151; text-decoration: none; hover:background-color: #f3f4f6;">category 1</a>
          <a href="#" style="display: block; padding: 0.5rem 1rem; color: #374151; text-decoration: none; hover:background-color: #f3f4f6;">category 2</a>
          <a href="#" style="display: block; padding: 0.5rem 1rem; color: #374151; text-decoration: none; hover:background-color: #f3f4f6;">category 3</a>
        </div>
      </div>
      <a href="#" style="color: #374151; text-decoration: none; font-weight: 500;">Kontakt</a>
    </div>
  </div>
</div>

### Aktionsmenu

```html
<div class="card">
  <div class="card__header">
    <h3 class="card__title">Projekt: Website-Redesign</h3>
    <div class="dropdown">
      <button class="dropdown__trigger button button--icon">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <circle cx="12" cy="12" r="1"></circle>
          <circle cx="12" cy="5" r="1"></circle>
          <circle cx="12" cy="19" r="1"></circle>
        </svg>
      </button>
      <div class="dropdown__menu dropdown__menu--right">
        <a href="#" class="dropdown__item">Details anzeigen</a>
        <a href="#" class="dropdown__item">Bearbeiten</a>
        <a href="#" class="dropdown__item">Archivieren</a>
        <div class="dropdown__divider"></div>
        <a href="#" class="dropdown__item dropdown__item--danger">delete</a>
      </div>
    </div>
  </div>
  <div class="card__body">
    Redesign the Unternehmenswebsite with neuer Markenidentitat and verbesserten functions.
  </div>
</div>
```

<div class="example-wrappers">
  <div style="border: 1px solid #e5e7eb; border-radius: 0.5rem; width: 100%; max-width: 400px; overflow: hidden;">
    <div style="display: flex; justify-content: space-between; align-items: center; padding: 1rem; border-bottom: 1px solid #e5e7eb; background-color: #f9fafb;">
      <h3 style="margin: 0; font-size: 1rem; color: #111827;">Projekt: Website-Redesign</h3>
      <div style="position: relative;">
        <button style="display: flex; align-items: center; justify-content: center; width: 2rem; height: 2rem; background: none; border: none; border-radius: 9999px; cursor: pointer; color: #6b7280; hover:background-color: #f3f4f6;">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <circle cx="12" cy="12" r="1"></circle>
            <circle cx="12" cy="5" r="1"></circle>
            <circle cx="12" cy="19" r="1"></circle>
          </svg>
        </button>
        <div style="position: absolute; top: 100%; right: 0; margin-top: 0.5rem; min-width: 10rem; background-color: white; border: 1px solid #e5e7eb; border-radius: 0.375rem; box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1); z-index: 10;">
          <a href="#" style="display: block; padding: 0.5rem 1rem; color: #374151; text-decoration: none; hover:background-color: #f3f4f6;">Details anzeigen</a>
          <a href="#" style="display: block; padding: 0.5rem 1rem; color: #374151; text-decoration: none; hover:background-color: #f3f4f6;">Bearbeiten</a>
          <a href="#" style="display: block; padding: 0.5rem 1rem; color: #374151; text-decoration: none; hover:background-color: #f3f4f6;">Archivieren</a>
          <div style="height: 1px; background-color: #e5e7eb; margin: 0.25rem 0;"></div>
          <a href="#" style="display: block; padding: 0.5rem 1rem; color: #ef4444; text-decoration: none; hover:background-color: #f3f4f6;">delete</a>
        </div>
      </div>
    </div>
    <div style="padding: 1rem;">
      Redesign the Unternehmenswebsite with neuer Markenidentitat and verbesserten functions.
    </div>
  </div>
</div>

## Anpassung

the Dropdown-component kann with CSS Variables angepasst become:

```css
:root {
  --dropdown-min-width: 10rem;
  --dropdown-bg: var(--color-white);
  --dropdown-border: 1px solid var(--color-neutral-200);
  --dropdown-border-radius: var(--radius-m);
  --dropdown-shadow: var(--shadow-lg);
  --dropdown-z-index: 50;
  
  --dropdown-item-padding: 0.5rem 1rem;
  --dropdown-item-color: var(--color-neutral-700);
  --dropdown-item-hover-bg: var(--color-neutral-100);
  --dropdown-item-hover-color: var(--color-neutral-900);
  
  --dropdown-divider-color: var(--color-neutral-200);
  --dropdown-divider-margin: 0.25rem 0;
  
  --dropdown-item-danger-color: var(--color-error-600);
  --dropdown-item-danger-hover-bg: var(--color-error-50);
  --dropdown-item-danger-hover-color: var(--color-error-700);
}
```

## JavaScript-Example

Hier ist a einfaches JavaScript-Example, um the Dropdown-Funktionalitat to implement:

```javascript
document.addEventListener('DOMContentLoaded', function() {
  // all Dropdown-Trigger finden
  const triggers = document.querySelectorAll('.dropdown__trigger');
  
  triggers.forEach(trigger => {
    trigger.addEventListener('click', function(e) {
      e.preventDefault();
      e.stopPropagation();
      
      const dropdown = this.closest('.dropdown');
      const menu = dropdown.querySelector('.dropdown__menu');
      
      // Umschalten des aktiven Zustands
      dropdown.classList.toggle('active');
      
      // close at Klick ausserhalb
      document.addEventListener('click', function closeDropdown(e) {
        if (!dropdown.contains(e.target)) {
          dropdown.classList.remove('active');
          document.removeEventListener('click', closeDropdown);
        }
      });
    });
  });
  
  // Tastaturunterstutzung for Dropdown-Items
  const items = document.querySelectorAll('.dropdown__item');
  
  items.forEach(item => {
    item.addEventListener('keydown', function(e) {
      if (e.key === 'ArrowDown' || e.key === 'ArrowUp') {
        e.preventDefault();
        
        const currentIndex = Array.from(items).indexOf(this);
        let targetIndex;
        
        if (e.key === 'ArrowDown') {
          targetIndex = (currentIndex + 1) % items.length;
        } else {
          targetIndex = (currentIndex - 1 + items.length) % items.length;
        }
        
        items[targetIndex].focus();
      }
    });
  });
});
```

## Accessibility

- Verwende `aria-expanded="true/false"` on dem Trigger-element
- Setze `aria-haspopup="true"` on dem Trigger-element
- Fuge `aria-labelledby` zum Dropdown-Menu hinzu, the on the ID des Triggers verweist
- Stelle sicher, that Dropdown-Menus with the Tastatur bedienbar sind
- Verwende `role="menu"` for the Menu and `role="menuitem"` for the Menupunkte
- Ermogliche the close des Menus with the ESC-Taste
- Achte on ausreichenden Kontrast between Text and background

## Browser-Kompatibilitat

the Dropdown-component ist with allen modernen Browsern kompatibel.

| function | Chrome | Firefox | Safari | Edge |
|----------|--------|---------|--------|------|
| Grundlegende Funktionalitat | ✅ | ✅ | ✅ | ✅ |
| Positionierung | ✅ | ✅ | ✅ | ✅ |
| CSS Variables | 49+ | 31+ | 9.1+ | 15+ |