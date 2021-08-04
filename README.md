![GitHub file size in bytes](https://img.shields.io/github/size/ACCLANE/blower/dist/css/blower.min.css?label=.min.css%20size&style=flat-square) ![GitHub last commit (branch)](https://img.shields.io/github/last-commit/ACCLANE/blower/develop?label=last%20dev%20commit&style=flat-square)

# Blower Frontend-Framework

A frontend framework based on SCSS and CSS Variables.

## (S)CSS-Variable-Scheme
Values with a `?` after them are optional.

**CSS Custom Properties:** `--{object?}-{function}-{specifics?}`  
**SCSS-Variablen:** `{namespace}.{function}-{specifics?}`

_CSS & SCSS variables are written accordingly in **kebab-case**._

## Namespace specifics
Included (`@use`) project variable files use their own namespace without having to specify it separately via `as`. This leads to overlaps with the SASS modules. Therefore, all SASS modules receive their own namespace. The following scheme is applied: `s-functionname`.

An example using the color module:
`@use 'sass:color' as s-color;`

## File structure
Standard folder according to BEMIT (`components`, `objects` etc.)
Folders for mixins, functions, variables, utilities, each with its own file for each segment and a master file in which they all run together.

## Repository-Rules
Before each commit, `npm run prod` is executed once so that there is always an executable version in the repository.

## Sass support

| Sass Compiler | Support |
| ------------- | ------- |
| Dart Sass     | ✅      |
| Lib Sass      | ❌      |
| Ruby Sass     | ⚰️      |
