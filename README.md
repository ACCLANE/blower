# Blower Frontend-Framework

Ein auf SCSS basierendes Frontend-Framework.

## CSS-Variablen-Schema
Werte mit einem `?` dahinter sind optional.

**CSS Custom Properties:** `--{object?}-{function}-{specifics?}`  
**SCSS-Variablen:** `{namespace}.{function}-{specifics?}`

_CSS & SCSS Variablen werden dementsprechend in **kebab-case** geschrieben._

## Namespace Besonderheiten
Eingebundene (`@use`) Projekt Variablendateien nutzen ihren eigenen Namespace, ohne das dieser gesondert via `as` angeben werden muss. Dies führt zu Überscheidungen mit den SASS eigenen Modulen. Daher erhalten alle SASS Module einen komplett eigenen Namespace. Folgendes Schema wird angewandt: `s-funktionsname`.

Ein Beispiel an Hand des Color Modules:
`@use 'sass:color' as s-color;`

## Dateistruktur
Standard-Ordner nach BEMIT (`components`, `objects` etc.)  
Ordner für Mixins, Functions, Variables, Utilites je mit eigener Datei pro Segment und Master-Datei, in der alle zusammenlaufen.

## Repository-Regeln
Vor jedem Commit wird einmal `npm run prod` ausgeführt, damit immer eine lauffähige Version im Repository ist.

## Sass support

| Sass Compiler | Support |
| ------------- | ------- |
| Dart Sass     | ✅      |
| Lib Sass      | ❌      |
| Ruby Sass     | ⚰️      |
