# Minimal Grid

Ein minimalistisches, flexibles CSS-Grid-System basierend auf CSS Grid Layout mit responsiven Breakpoints.

## Features

- 12-Spalten-Grid-System
- CSS Grid basiert (modern und performant)
- Responsive Breakpoints (xs, sm, md, lg, xl, 2xl)
- Container-Klassen
- Offset-Klassen
- Order-Klassen
- Visibility-Helpers
- Vollständig anpassbar über SCSS-Variablen

## Installation

1. Füge die `minimal_grid.scss` Datei zu deinem Projekt hinzu
2. Importiere sie in deine Haupt-SCSS-Datei:

```scss
@import 'minimal_grid';
```

## Konfiguration

Du kannst die folgenden Variablen anpassen, bevor du das Grid importierst:

```scss
$grid-columns: 12;
$gutter: 5vw;
$container-padding: 5vw;
$container-max-width: 2560px;

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

## Nutzungsbeispiel

Hier ist ein einfaches Beispiel für ein responsives Layout:

```html
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minimal Grid Beispiel</title>
    <link rel="stylesheet" href="minimal_grid.css">
    <style>
        /* Einfaches Styling für das Beispiel */
        .box {
            background: #3498db;
            color: white;
            padding: 20px;
            text-align: center;
            border-radius: 4px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Minimal Grid Beispiel</h1>

        <!-- Einfaches 3-Spalten-Layout -->
        <div class="row">
            <div class="xs:col-12 md:col-4">
                <div class="box">Spalte 1</div>
            </div>
            <div class="xs:col-12 md:col-4">
                <div class="box">Spalte 2</div>
            </div>
            <div class="xs:col-12 md:col-4">
                <div class="box">Spalte 3</div>
            </div>
        </div>

        <!-- Asymmetrisches Layout -->
        <div class="row">
            <div class="xs:col-12 lg:col-8">
                <div class="box">Hauptinhalt (8 Spalten)</div>
            </div>
            <div class="xs:col-12 lg:col-4">
                <div class="box">Sidebar (4 Spalten)</div>
            </div>
        </div>

        <!-- Volle Breite -->
        <div class="row">
            <div class="xs:col-full">
                <div class="box">Volle Breite</div>
            </div>
        </div>
    </div>
</body>
</html>
```

### Erklärung

- **`container`**: Zentriert den Inhalt mit einer maximalen Breite
- **`row`**: Erstellt ein Grid mit 12 Spalten
- **`xs:col-12`**: Auf kleinen Bildschirmen (mobil) nimmt das Element 12 Spalten (volle Breite) ein
- **`md:col-4`**: Ab der mittleren Breakpoint (768px) nimmt das Element 4 Spalten ein

## Weitere Funktionen

### Offset

```html
<div class="row">
    <div class="xs:col-6 xs:offset-3">
        <!-- Zentriert mit Offset -->
    </div>
</div>
```

### Order

```html
<div class="row">
    <div class="xs:col-6 lg:order-2">Zuerst auf Mobil, zweites auf Desktop</div>
    <div class="xs:col-6 lg:order-1">Zweites auf Mobil, erstes auf Desktop</div>
</div>
```

### Visibility

```html
<div class="xs:hidden lg:block">
    Nur auf großen Bildschirmen sichtbar
</div>
```

## Breakpoints

| Breakpoint | Größe | Präfix |
|------------|-------|--------|
| Extra Small | 0px | `xs:` |
| Small | 600px | `sm:` |
| Medium | 768px | `md:` |
| Large | 1024px | `lg:` |
| Extra Large | 1280px | `xl:` |
| 2X Large | 1536px | `2xl:` |

## Browser-Unterstützung

Unterstützt alle modernen Browser, die CSS Grid unterstützen:
- Chrome/Edge 57+
- Firefox 52+
- Safari 10.1+

## Lizenz

Frei nutzbar für private und kommerzielle Projekte.
