# Plume CSS - a tiny framework for css artisans

## Introduction

The goal of this library is to get a base that include a grid system, some helpers and the maximum of compatibilities with old scool browsers.

## Quick start

* Include from jsDelivr CDN
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/0kyn/plume-css/dist/css/plume.min.css">
```

## Development
* Clone the repository
```sh
git clone https://github.com/0kyn/plume-css.git my-project 
```

```sh
cd my-project 
```

* Watching for changes
```sh
npm run dev 
```

## Production

Build assets for production  
```sh
npm run prod 
```

## Docs
Plume CSS is mobile first, breakpoints are defined as Bootstrap ones :
```css
/* Small devices (landscape phones, 576px and up) */
@media (min-width: 576px) { ... }

/* Medium devices (tablets, 768px and up) */
@media (min-width: 768px) { ... }

/* Large devices (desktops, 992px and up) */
@media (min-width: 992px) { ... }

/* Extra large devices (large desktops, 1200px and up) */
@media (min-width: 1200px) { ... }
```

### Grid system (12 columns) works in the same way

```html
<div class="plume-grid">
  <div class="row">
    <div class="col-6">50%</div>
    <div class="col-6">50%</div>
  </div>

  <div class="row">
    <div class="col-3">25%</div>
    <!-- 75% -->
    <div class="col-9">
      <div class="row">
        <div class="col-6">50% of 75%</div>
        <div class="col-6">50% of 75%</div>
      </div>
    </div>
  </div>

  <div class="row">
    <div class="col-12 col-xl-4">mobile->100% - laptop(>1200px)->25%</div>
    <div class="col-12 col-xl-4">mobile->100% - laptop(>1200px)->25%</div>
    <div class="col-12 col-xl-4">mobile->100% - laptop(>1200px)->25%</div>
  </div>
</div>
```
> This grid system is based on `float` that makes it compatible with old browsers.

### Helpers
- center a single column in a row
```html
<div class="row">
  <div class="col-4 col-center">~33.3% centered column</div>
</div>
```

- hide a column at a specific breakpoint
```html
<div class="row">
  <div class="col-12 hide-xl">column hidden on laptop(>1200px)</div>
</div>
```

- show a column only for a specific breakpoint
```html
<div class="row">
  <div class="col-12 show-xl">column only visible on laptop(>1200px)</div>
</div>
```

- miscellaneous  
You'll find various helpers in `src/scss/base/helpers.scss`