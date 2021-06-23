# Blower Frontend-Framework

Ein auf SCSS basierendes Frontend-Framework.

## CSS-Variablen-Schema
Werte mit einem `?` dahinter sind optional.

**CSS Custom Properties:** `--{object?}-{function}-{specifics?}`  
**SCSS-Variablen:** `{namespace}.{function}-{specifics?}`

_CSS & SCSS Variablen werden dementsprechend in **kebab-case** geschrieben._

## Dateistruktur
Standard-Ordner nach BEMIT (`components`, `objects` etc.)  
Ordner für Mixins, Functions, Variables, Utilites je mit eigener Datei pro Segment und Master-Datei, in der alle zusammenlaufen.

## Repository-Regeln
Vor jedem Commit wird einmal `npm run prod` ausgeführt, damit immer eine lauffähige Version im Repository ist.
