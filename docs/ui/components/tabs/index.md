---
title: Tabs Component
outline: deep
---

# Tabs

the Tabs-Component ermoglicht the Organisation from Inhalten in separate, leicht zugangliche Abschnitte. them ist besonders nutzlich, um Platz to sparen and verwandte contents ubersichtlich to gruppieren.

## Installation

the Tabs-Component ist Teil the Casoon UI Library.

```bash
# Installation the gesamten Bibliothek
npm install @casoon/ui-lib
```

## Import

```css
/* Import aller UI-Components */
@import '@casoon/ui-lib/ui.css';

/* or only the Tabs-Component */
@import '@casoon/ui-lib/ui/components/tabs.css';
```

## Basic Usage

```html
<div class="tabs">
  <div class="tabs__list" role="tablist">
    <button class="tabs__tab active" role="tab" aria-selected="true" id="tab-1" aria-controls="panel-1">
      Tab 1
    </button>
    <button class="tabs__tab" role="tab" aria-selected="false" id="tab-2" aria-controls="panel-2">
      Tab 2
    </button>
    <button class="tabs__tab" role="tab" aria-selected="false" id="tab-3" aria-controls="panel-3">
      Tab 3
    </button>
  </div>
  <div class="tabs__panels">
    <div class="tabs__panel active" role="tabpanel" id="panel-1" aria-labelledby="tab-1">
      content for Tab 1
    </div>
    <div class="tabs__panel" role="tabpanel" id="panel-2" aria-labelledby="tab-2" hidden>
      content for Tab 2
    </div>
    <div class="tabs__panel" role="tabpanel" id="panel-3" aria-labelledby="tab-3" hidden>
      content for Tab 3
    </div>
  </div>
</div>
```

<div class="example-wrappers">
  <div style="border: 1px solid #e5e7eb; border-radius: 0.5rem; overflow: hidden; width: 100%; max-width: 600px;">
    <div style="display: flex; border-bottom: 1px solid #e5e7eb;">
      <button style="padding: 0.75rem 1rem; border: none; background: none; font-weight: 500; color: #3b82f6; border-bottom: 2px solid #3b82f6; cursor: pointer;">Tab 1</button>
      <button style="padding: 0.75rem 1rem; border: none; background: none; font-weight: 500; color: #6b7280; cursor: pointer;">Tab 2</button>
      <button style="padding: 0.75rem 1rem; border: none; background: none; font-weight: 500; color: #6b7280; cursor: pointer;">Tab 3</button>
    </div>
    <div style="padding: 1rem;">
      <p>content for Tab 1</p>
      <p>Hier ist a Exampletext for den ersten Tab. these contents become angezeigt, if Tab 1 aktiv ist.</p>
    </div>
  </div>
</div>

## Variants

### Tabs with icons

```html
<div class="tabs">
  <div class="tabs__list" role="tablist">
    <button class="tabs__tab active" role="tab" aria-selected="true" id="tab-1" aria-controls="panel-1">
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"></path>
        <polyline points="9 22 9 12 15 12 15 22"></polyline>
      </svg>
      Home
    </button>
    <button class="tabs__tab" role="tab" aria-selected="false" id="tab-2" aria-controls="panel-2">
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <circle cx="12" cy="12" r="10"></circle>
        <circle cx="12" cy="10" r="3"></circle>
        <path d="M7 20.66l2-3.26"></path>
        <path d="M17 20.66l-2-3.26"></path>
        <path d="M14.5 14.5l-2.5 2"></path>
        <path d="M9.5 14.5l2.5 2"></path>
      </svg>
      Einstellungen
    </button>
    <button class="tabs__tab" role="tab" aria-selected="false" id="tab-3" aria-controls="panel-3">
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"></path>
        <circle cx="12" cy="7" r="4"></circle>
      </svg>
      Profil
    </button>
  </div>
  <div class="tabs__panels">
    <!-- panels hier -->
  </div>
</div>
```

<div class="example-wrappers">
  <div style="border: 1px solid #e5e7eb; border-radius: 0.5rem; overflow: hidden; width: 100%; max-width: 600px;">
    <div style="display: flex; border-bottom: 1px solid #e5e7eb;">
      <button style="padding: 0.75rem 1rem; border: none; background: none; font-weight: 500; color: #3b82f6; border-bottom: 2px solid #3b82f6; cursor: pointer; display: flex; align-items: center; gap: 0.5rem;">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"></path>
          <polyline points="9 22 9 12 15 12 15 22"></polyline>
        </svg>
        Home
      </button>
      <button style="padding: 0.75rem 1rem; border: none; background: none; font-weight: 500; color: #6b7280; cursor: pointer; display: flex; align-items: center; gap: 0.5rem;">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <circle cx="12" cy="12" r="10"></circle>
          <circle cx="12" cy="10" r="3"></circle>
          <path d="M7 20.66l2-3.26"></path>
          <path d="M17 20.66l-2-3.26"></path>
          <path d="M14.5 14.5l-2.5 2"></path>
          <path d="M9.5 14.5l2.5 2"></path>
        </svg>
        Einstellungen
      </button>
      <button style="padding: 0.75rem 1rem; border: none; background: none; font-weight: 500; color: #6b7280; cursor: pointer; display: flex; align-items: center; gap: 0.5rem;">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"></path>
          <circle cx="12" cy="7" r="4"></circle>
        </svg>
        Profil
      </button>
    </div>
    <div style="padding: 1rem;">
      <p>Home-contents</p>
      <p>Willkommen on the Startseite deiner Application.</p>
    </div>
  </div>
</div>

### Vertikale Tabs

```html
<div class="tabs tabs--vertical">
  <div class="tabs__list" role="tablist">
    <button class="tabs__tab active" role="tab" aria-selected="true" id="tab-1" aria-controls="panel-1">
      Tab 1
    </button>
    <button class="tabs__tab" role="tab" aria-selected="false" id="tab-2" aria-controls="panel-2">
      Tab 2
    </button>
    <button class="tabs__tab" role="tab" aria-selected="false" id="tab-3" aria-controls="panel-3">
      Tab 3
    </button>
  </div>
  <div class="tabs__panels">
    <div class="tabs__panel active" role="tabpanel" id="panel-1" aria-labelledby="tab-1">
      content for Tab 1
    </div>
    <div class="tabs__panel" role="tabpanel" id="panel-2" aria-labelledby="tab-2" hidden>
      content for Tab 2
    </div>
    <div class="tabs__panel" role="tabpanel" id="panel-3" aria-labelledby="tab-3" hidden>
      content for Tab 3
    </div>
  </div>
</div>
```

<div class="example-wrappers">
  <div style="border: 1px solid #e5e7eb; border-radius: 0.5rem; overflow: hidden; width: 100%; max-width: 600px; display: flex;">
    <div style="display: flex; flex-direction: column; border-right: 1px solid #e5e7eb; min-width: 150px;">
      <button style="padding: 0.75rem 1rem; border: none; text-align: left; background: #f3f4f6; font-weight: 500; color: #3b82f6; border-left: 3px solid #3b82f6; cursor: pointer;">Tab 1</button>
      <button style="padding: 0.75rem 1rem; border: none; text-align: left; background: none; font-weight: 500; color: #6b7280; cursor: pointer;">Tab 2</button>
      <button style="padding: 0.75rem 1rem; border: none; text-align: left; background: none; font-weight: 500; color: #6b7280; cursor: pointer;">Tab 3</button>
    </div>
    <div style="padding: 1rem; flex: 1;">
      <p>content for Tab 1</p>
      <p>Vertikale Tabs eignen oneself besonders for komplexe Forme or umfangreiche Einstellungen.</p>
    </div>
  </div>
</div>

### Pills-Style

```html
<div class="tabs tabs--pills">
  <div class="tabs__list" role="tablist">
    <button class="tabs__tab active" role="tab" aria-selected="true" id="tab-1" aria-controls="panel-1">
      Tab 1
    </button>
    <button class="tabs__tab" role="tab" aria-selected="false" id="tab-2" aria-controls="panel-2">
      Tab 2
    </button>
    <button class="tabs__tab" role="tab" aria-selected="false" id="tab-3" aria-controls="panel-3">
      Tab 3
    </button>
  </div>
  <div class="tabs__panels">
    <!-- panels hier -->
  </div>
</div>
```

<div class="example-wrappers">
  <div style="border: 1px solid #e5e7eb; border-radius: 0.5rem; overflow: hidden; width: 100%; max-width: 600px;">
    <div style="display: flex; gap: 0.5rem; padding: 0.75rem; background-color: #f9fafb; border-bottom: 1px solid #e5e7eb;">
      <button style="padding: 0.5rem 1rem; border: none; background: #3b82f6; color: white; font-weight: 500; border-radius: 9999px; cursor: pointer;">Tab 1</button>
      <button style="padding: 0.5rem 1rem; border: none; background: #f3f4f6; color: #6b7280; font-weight: 500; border-radius: 9999px; cursor: pointer;">Tab 2</button>
      <button style="padding: 0.5rem 1rem; border: none; background: #f3f4f6; color: #6b7280; font-weight: 500; border-radius: 9999px; cursor: pointer;">Tab 3</button>
    </div>
    <div style="padding: 1rem;">
      <p>content for Tab 1</p>
      <p>Pills-Tabs bieten a modernes design and eignen oneself for Anwendungen with einem leichten, freundlichen Erscheinungsbild.</p>
    </div>
  </div>
</div>

## Usagesbeispiele

### Produkt-Detailseite

```html
<div class="product-details">
  <div class="tabs">
    <div class="tabs__list" role="tablist">
      <button class="tabs__tab active" role="tab" aria-selected="true" id="details-tab" aria-controls="details-panel">
        Details
      </button>
      <button class="tabs__tab" role="tab" aria-selected="false" id="specs-tab" aria-controls="specs-panel">
        Spezifikationen
      </button>
      <button class="tabs__tab" role="tab" aria-selected="false" id="reviews-tab" aria-controls="reviews-panel">
        Bewertungen
      </button>
    </div>
    <div class="tabs__panels">
      <div class="tabs__panel active" role="tabpanel" id="details-panel" aria-labelledby="details-tab">
        <h3>Produktbeschreibung</h3>
        <p>Ausfuhrliche Description des Produkts...</p>
      </div>
      <div class="tabs__panel" role="tabpanel" id="specs-panel" aria-labelledby="specs-tab" hidden>
        <h3>Technische Daten</h3>
        <ul>
          <li>Masse: 10 x 15 x 5 cm</li>
          <li>Gewicht: 250g</li>
          <li>Material: Aluminium</li>
        </ul>
      </div>
      <div class="tabs__panel" role="tabpanel" id="reviews-panel" aria-labelledby="reviews-tab" hidden>
        <h3>Kundenbewertungen</h3>
        <div class="reviews-list">
          <!-- Bewertungen hier -->
        </div>
      </div>
    </div>
  </div>
</div>
```

<div class="example-wrappers">
  <div style="border: 1px solid #e5e7eb; border-radius: 0.5rem; overflow: hidden; width: 100%; max-width: 600px;">
    <div style="display: flex; border-bottom: 1px solid #e5e7eb;">
      <button style="padding: 0.75rem 1rem; border: none; background: none; font-weight: 500; color: #3b82f6; border-bottom: 2px solid #3b82f6; cursor: pointer;">Details</button>
      <button style="padding: 0.75rem 1rem; border: none; background: none; font-weight: 500; color: #6b7280; cursor: pointer;">Spezifikationen</button>
      <button style="padding: 0.75rem 1rem; border: none; background: none; font-weight: 500; color: #6b7280; cursor: pointer;">Bewertungen</button>
    </div>
    <div style="padding: 1rem;">
      <h3 style="margin-top: 0; font-size: 1.25rem; color: #111827;">Produktbeschreibung</h3>
      <p>this hochwertige Produkt wurde for maximale Leistung and Langlebigkeit entwickelt. it verfugt over a ergonomische Form and a modernes design, the oneself nahtlos in jede Umgebung einfugt.</p>
      <p>the intuitive Bedienung and the vielseitigen functions machen it zur idealen Wahl for anspruchsvolle Anwender.</p>
    </div>
  </div>
</div>

### Einstellungen-panel

```html
<div class="settings-panel">
  <h2>Kontoeinstellungen</h2>
  <div class="tabs tabs--vertical">
    <div class="tabs__list" role="tablist">
      <button class="tabs__tab active" role="tab" aria-selected="true" id="profile-tab" aria-controls="profile-panel">
        <svg><!-- Profil-icon --></svg>
        Profil
      </button>
      <button class="tabs__tab" role="tab" aria-selected="false" id="security-tab" aria-controls="security-panel">
        <svg><!-- Sicherheits-icon --></svg>
        Sicherheit
      </button>
      <button class="tabs__tab" role="tab" aria-selected="false" id="notifications-tab" aria-controls="notifications-panel">
        <svg><!-- Benachrichtigungs-icon --></svg>
        notifications
      </button>
      <button class="tabs__tab" role="tab" aria-selected="false" id="billing-tab" aria-controls="billing-panel">
        <svg><!-- Zahlungs-icon --></svg>
        Zahlungen
      </button>
    </div>
    <div class="tabs__panels">
      <div class="tabs__panel active" role="tabpanel" id="profile-panel" aria-labelledby="profile-tab">
        <form class="settings-form">
          <div class="form-group">
            <label for="name">Name</label>
            <input type="text" id="name" value="Max Mustermann">
          </div>
          <div class="form-group">
            <label for="email">E-Mail</label>
            <input type="email" id="email" value="max@example.com">
          </div>
          <button type="submit" class="button button--primary">save</button>
        </form>
      </div>
      <!-- additional panels -->
    </div>
  </div>
</div>
```

<div class="example-wrappers">
  <div style="border: 1px solid #e5e7eb; border-radius: 0.5rem; overflow: hidden; width: 100%; max-width: 700px;">
    <h2 style="margin: 0; padding: 1rem; font-size: 1.5rem; border-bottom: 1px solid #e5e7eb; background-color: #f9fafb;">Kontoeinstellungen</h2>
    <div style="display: flex;">
      <div style="display: flex; flex-direction: column; border-right: 1px solid #e5e7eb; min-width: 200px; background-color: #f9fafb;">
        <button style="padding: 0.75rem 1rem; border: none; text-align: left; background-color: #f3f4f6; font-weight: 500; color: #3b82f6; border-left: 3px solid #3b82f6; cursor: pointer; display: flex; align-items: center; gap: 0.5rem;">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"></path>
            <circle cx="12" cy="7" r="4"></circle>
          </svg>
          Profil
        </button>
        <button style="padding: 0.75rem 1rem; border: none; text-align: left; background: none; font-weight: 500; color: #6b7280; cursor: pointer; display: flex; align-items: center; gap: 0.5rem;">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <rect x="3" y="11" width="18" height="11" rx="2" ry="2"></rect>
            <path d="M7 11V7a5 5 0 0 1 10 0v4"></path>
          </svg>
          Sicherheit
        </button>
        <button style="padding: 0.75rem 1rem; border: none; text-align: left; background: none; font-weight: 500; color: #6b7280; cursor: pointer; display: flex; align-items: center; gap: 0.5rem;">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M18 8A6 6 0 0 0 6 8c0 7-3 9-3 9h18s-3-2-3-9"></path>
            <path d="M13.73 21a2 2 0 0 1-3.46 0"></path>
          </svg>
          notifications
        </button>
        <button style="padding: 0.75rem 1rem; border: none; text-align: left; background: none; font-weight: 500; color: #6b7280; cursor: pointer; display: flex; align-items: center; gap: 0.5rem;">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <rect x="1" y="4" width="22" height="16" rx="2" ry="2"></rect>
            <line x1="1" y1="10" x2="23" y2="10"></line>
          </svg>
          Zahlungen
        </button>
      </div>
      <div style="padding: 1.5rem; flex: 1;">
        <div style="display: flex; flex-direction: column; gap: 1rem;">
          <div>
            <label style="display: block; margin-bottom: 0.5rem; font-weight: 500; color: #374151;">Name</label>
            <input type="text" value="Max Mustermann" style="width: 100%; padding: 0.5rem; border: 1px solid #d1d5db; border-radius: 0.375rem;">
          </div>
          <div>
            <label style="display: block; margin-bottom: 0.5rem; font-weight: 500; color: #374151;">E-Mail</label>
            <input type="email" value="max@example.com" style="width: 100%; padding: 0.5rem; border: 1px solid #d1d5db; border-radius: 0.375rem;">
          </div>
          <div>
            <button style="padding: 0.5rem 1rem; background-color: #3b82f6; color: white; border: none; border-radius: 0.375rem; font-weight: 500; cursor: pointer;">save</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

## Customization

the Tabs-Component kann with CSS Variables angepasst become:

```css
:root {
  --tabs-border: 1px solid var(--color-neutral-200);
  --tabs-border-radius: var(--radius-m);
  --tabs-background: var(--color-white);
  
  --tabs-tab-padding: 0.75rem 1rem;
  --tabs-tab-color: var(--color-neutral-700);
  --tabs-tab-font-weight: 500;
  --tabs-tab-active-color: var(--color-primary-500);
  --tabs-tab-hover-color: var(--color-neutral-900);
  --tabs-tab-hover-bg: var(--color-neutral-50);
  
  --tabs-tab-border-active: 2px solid var(--color-primary-500);
  
  --tabs-panel-padding: 1rem;
  
  /* Pills-Variante */
  --tabs-pills-background: var(--color-neutral-100);
  --tabs-pills-active-bg: var(--color-primary-500);
  --tabs-pills-active-color: var(--color-white);
  --tabs-pills-border-radius: var(--radius-full);
  
  /* Vertikale Tabs */
  --tabs-vertical-width: 200px;
  --tabs-vertical-tab-border-active: 3px solid var(--color-primary-500);
}
```

## Accessibility

- Verwende korrekte ARIA-attributes (`role="tablist"`, `role="tab"`, `role="tabpanel"`)
- Stelle sicher, that Tabs with the Tastatur bedient become can (Pfeiltasten zum Navigieren)
- Behalte den Fokus im aktiven Tab, if between Tabs gewechselt wird
- Verwende `aria-selected="true"` for den aktiven Tab
- Setze `hidden` on inaktive panels, um them from Screenreadern auszuschliessen
- Verwende `aria-controls` and `aria-labelledby` zur Verknupfung from Tabs and panels

## JavaScript-Example

Hier ist a einfaches JavaScript-Example, um the Tabs funktionsfahig to machen:

```javascript
document.addEventListener('DOMContentLoaded', function() {
  const tabLists = document.querySelectorAll('.tabs__list');
  
  tabLists.forEach(tabList => {
    const tabs = tabList.querySelectorAll('.tabs__tab');
    const panels = tabList.closest('.tabs').querySelectorAll('.tabs__panel');
    
    tabs.forEach((tab, index) => {
      tab.addEventListener('click', () => {
        // all Tabs and panels deactivate
        tabs.forEach(t => {
          t.classList.remove('active');
          t.setAttribute('aria-selected', 'false');
        });
        
        panels.forEach(panel => {
          panel.classList.remove('active');
          panel.hidden = true;
        });
        
        // Aktuellen Tab and panel activate
        tab.classList.add('active');
        tab.setAttribute('aria-selected', 'true');
        panels[index].classList.add('active');
        panels[index].hidden = false;
      });
      
      // Tastaturnavigation
      tab.addEventListener('keydown', (e) => {
        let targetTab;
        
        switch (e.key) {
          case 'ArrowRight':
            targetTab = tab.nextElementSibling || tabs[0];
            break;
          case 'ArrowLeft':
            targetTab = tab.previousElementSibling || tabs[tabs.length - 1];
            break;
          default:
            return;
        }
        
        e.preventDefault();
        targetTab.click();
        targetTab.focus();
      });
    });
  });
});
```

## Browser-Kompatibilitat

the Tabs-Component ist with allen modernen Browsern kompatibel.

| Function | Chrome | Firefox | Safari | Edge |
|----------|--------|---------|--------|------|
| Grundlegende Funktionalitat | ✅ | ✅ | ✅ | ✅ |
| flexbox-layout | 29+ | 28+ | 9+ | 16+ |
| CSS Variables | 49+ | 31+ | 9.1+ | 15+ |