![](./blower-logo.svg "Blower Logo")

<img height="auto" src="./blower-logo.svg" width="300" alt="Blower Logo"/>

# Blower Frontend-Framework

A frontend framework based on SCSS modules and CSS variables.

## Stats

![GitHub file size in bytes](https://img.shields.io/github/size/ACCLANE/blower/dist/css/blower.min.css?label=.min.css%20size&style=flat-square) ![GitHub last commit (branch)](https://img.shields.io/github/last-commit/ACCLANE/blower/develop?label=last%20dev%20commit&style=flat-square)

## Requirements

Your project have to use [Dart Sass](https://sass-lang.com/dart-sass) >= 1.35.

### Sass support

| Sass Compiler | Support |
| ------------- | ------- |
| Dart Sass     | ✅      |
| Lib Sass      | ❌      |
| Ruby Sass     | ⚰️      |

## Install Blower

```bash
npm install https://github.com/ACCLANE/blower.git (#commit, #branch or #(release)tag)
```

## Choose what you need

"Blower" is modular and gives you full choice of which modules to include in your project.
There are two configuration levels that can be used independently of each other.

1. The global configuration file `variable/_global-config.scss`. Here you find general settings.
2. Each component, module ect. comes with its own configuration variables, maps or lists. These can be customized with the new `@use` function together `with()`.

### Usage example

```scss
@use '~/blower/components/button' as blower-buttons with (
	$rounded: false, /// all buttons without rounded edges. The remaining components depend on the global configuration.
	$button-types: ( /// only include 3 button types
		'primary',
		'secondary',
		'success',
	),
);
```

## Development instructions

### (S)CSS-Variable-Scheme
Values with a `?` after them are optional.

**CSS Custom Properties:** `--{object?}-{function}-{specifics?}`  
**SCSS-Variablen:** `{namespace}.{function}-{specifics?}`

_CSS & SCSS variables are written accordingly in **kebab-case**._

### Namespace specifics
Included (`@use`) project variable files use their own namespace without having to specify it separately via `as`. This leads to overlaps with the SASS modules. Therefore, all SASS modules receive their own namespace. The following scheme is applied: `s-functionname`.

An example using the color module:
`@use 'sass:color' as s-color;`

### File structure
Standard folder according to BEMIT (`components`, `objects` etc.)
Folders for mixins, functions, variables, utilities, each with its own file for each segment and a master file in which they all run together.

### Repository-Rules
Before each commit, `npm run prod` is executed once so that there is always an executable version in the repository.
