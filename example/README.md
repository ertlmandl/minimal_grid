# Minimal Grid - Beispiele

Dieser Ordner enthält vollständige, lauffähige Beispiele für das Minimal Grid System.

## 📁 Übersicht

### 01-basic.html
**Basis-Beispiele für Einsteiger**

Dieses Beispiel zeigt die grundlegenden Funktionen des Grid-Systems:
- ✅ Gleichmäßige Spalten (3 Spalten, 4 Spalten)
- ✅ Asymmetrische Layouts (8/4, 6/6)
- ✅ Volle Breite mit `col-full`
- ✅ Responsive Breakpoints (xs, sm, md, lg)
- ✅ Container-Nutzung

**Ideal für:** Erste Schritte mit dem Grid-System

---

### 02-advanced.html
**Fortgeschrittene Features**

Zeigt erweiterte Funktionen und Techniken:
- 📐 **Offset-Klassen** - Zentrieren und Verschieben von Inhalten
- 🔄 **Order-Klassen** - Reihenfolge auf verschiedenen Bildschirmgrößen ändern
- 👁️ **Visibility-Helpers** - Elemente responsive ein-/ausblenden
- ✨ Kombinierte Features für komplexe Layouts

**Ideal für:** Fortgeschrittene Layouts und responsive Designs

---

### 03-website-layout.html
**Realistisches Website-Layout**

Eine vollständige Landing Page mit:
- 🎨 Header mit Navigation
- 🚀 Hero-Section
- 📦 Feature-Cards in Grid-Layout
- 📊 Statistik-Sektion
- 💰 Pricing-Tabellen
- 📱 Footer mit mehrspaltigem Layout
- 🎯 Responsive Anpassungen für alle Bildschirmgrößen

**Ideal für:** Reale Projekte und als Vorlage

---

## 🚀 Schnellstart

1. **Öffne eine der HTML-Dateien im Browser:**
   ```bash
   # Im Browser öffnen (Linux)
   xdg-open 01-basic.html

   # Im Browser öffnen (macOS)
   open 01-basic.html

   # Im Browser öffnen (Windows)
   start 01-basic.html
   ```

2. **Oder starte einen lokalen Server:**
   ```bash
   # Mit Python 3
   python3 -m http.server 8000

   # Mit Node.js (npx)
   npx serve .

   # Mit PHP
   php -S localhost:8000
   ```

   Dann öffne: `http://localhost:8000/01-basic.html`

---

## 📱 Browser-Ansicht testen

Um die responsive Funktionen zu testen:

1. **Browser Developer Tools öffnen:**
   - Chrome/Edge: `F12` oder `Ctrl+Shift+I` (Windows/Linux) / `Cmd+Option+I` (Mac)
   - Firefox: `F12` oder `Ctrl+Shift+I` (Windows/Linux) / `Cmd+Option+I` (Mac)
   - Safari: `Cmd+Option+I` (Mac)

2. **Device Toolbar aktivieren:**
   - Chrome/Edge: `Ctrl+Shift+M` (Windows/Linux) / `Cmd+Shift+M` (Mac)
   - Firefox: `Ctrl+Shift+M` (Windows/Linux) / `Cmd+Option+M` (Mac)

3. **Verschiedene Bildschirmgrößen testen:**
   - **Mobile:** 375px (iPhone SE)
   - **Tablet:** 768px (iPad)
   - **Desktop:** 1280px, 1920px

---

## 🎯 Breakpoints

Das Grid-System verwendet folgende Breakpoints:

| Name | Größe | Präfix | Verwendung |
|------|-------|--------|------------|
| **xs** | 0px | `xs:` | Mobile (Standard) |
| **sm** | 600px | `sm:` | Large Mobile |
| **md** | 768px | `md:` | Tablet |
| **lg** | 1024px | `lg:` | Desktop |
| **xl** | 1280px | `xl:` | Large Desktop |
| **2xl** | 1536px | `2xl:` | Extra Large |

---

## 💡 Wichtige Konzepte

### Container
```html
<div class="container">
  <!-- Zentrierter Inhalt mit max-width: 2560px -->
</div>

<div class="container fluid">
  <!-- Volle Breite ohne max-width -->
</div>

<!-- Container mit Breakpoint-basierten max-width -->
<div class="container md">max-width: 768px</div>
<div class="container lg">max-width: 1024px</div>
<div class="container xl">max-width: 1280px</div>
<div class="container 2xl">max-width: 1536px</div>
```

### Row (Grid)
```html
<div class="row">
  <!-- Erstellt ein 12-Spalten-Grid -->
</div>
```

### Spalten
```html
<!-- Responsive Spalten -->
<div class="xs:col-12 md:col-6 lg:col-4">
  <!-- Mobil: volle Breite
       Tablet: halbe Breite
       Desktop: 1/3 Breite -->
</div>
```

### Offset (Verschieben)
```html
<!-- Zentriert 6 Spalten -->
<div class="xs:col-6 xs:offset-3">
  <!-- 3 + 6 + 3 = 12 -->
</div>
```

### Order (Reihenfolge)
```html
<div class="xs:col-6 lg:order-2">Box 1</div>
<div class="xs:col-6 lg:order-1">Box 2</div>
<!-- Auf Desktop: Box 2 vor Box 1 -->
```

### Visibility (Sichtbarkeit)
```html
<!-- Versteckt auf Mobil, sichtbar ab Tablet -->
<div class="xs:hidden md:block">
  Nur auf Tablet+
</div>
```

---

## 🛠️ Anpassungen

### CSS bearbeiten

Die kompilierte CSS-Datei liegt in `css/minimal_grid.css`.

Wenn du die Variablen anpassen möchtest (Spalten, Abstände, etc.), bearbeite die `minimal_grid.scss` im Hauptverzeichnis und kompiliere sie neu:

```bash
# Mit Sass
sass ../minimal_grid.scss css/minimal_grid.css

# Mit node-sass
node-sass ../minimal_grid.scss css/minimal_grid.css
```

### Variablen anpassen

Vor dem Import des Grid-Systems:

```scss
// Anpassungen
$grid-columns: 12;
$gutter: 5vw;
$container-padding: 5vw;
$container-max-width: 2560px;

// Breakpoints anpassen
$breakpoints: (
  xs: 0,
  sm: 600px,
  md: 768px,
  lg: 1024px,
  xl: 1280px,
  2xl: 1536px
);

@import 'minimal_grid';
```

---

## 📚 Weitere Ressourcen

- **Hauptdokumentation:** `../README.md`
- **SCSS-Datei:** `../minimal_grid.scss`

---

## ❓ Fragen?

Schaue dir die Beispiele an, experimentiere mit den Klassen und ändere die Browser-Größe, um die responsive Funktionalität zu sehen!

**Viel Erfolg mit Minimal Grid! 🎉**
