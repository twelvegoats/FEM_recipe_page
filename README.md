# Frontend Mentor - Recipe Page Solution

This is a solution to the [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### Screenshot

![Recipe Page Screenshot](./preview.jpg)

### Links

- Solution URL: [GitHub Repository](https://github.com/twelvegoats/FEM_recipe_page)
- Live Site URL: [Live Demo](#)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties (SCSS variables)
- Flexbox
- Mobile-first workflow
- SCSS/Sass preprocessor
- BEM methodology for CSS class naming
- Accessibility best practices

### What I learned

This project helped me strengthen several key web development concepts:

#### 1. **SCSS Architecture & Organization**

I learned to structure SCSS files using partials and the `@use` directive for better modularity:

```scss
@use './base/variables' as *;
@use './base/reset' as *;
@use './base/typography' as *;
@use './base/base' as *;
```

#### 2. **Accessibility Implementation**

Implemented proper accessibility features including:

- Skip navigation for keyboard users
- Semantic HTML structure with proper headings
- ARIA labels and roles for complex content like the nutrition table
- Focus management for interactive elements

```
<a href="#main-content" class="skip-link">Skip to main content</a>
```

#### 3. **Custom List Styling**

Created custom numbered lists using CSS counters instead of default browser styling:

```
.instructions__list {
  counter-reset: instruction-counter;
  list-style: none;
  padding-left: 0;
}

.instructions__list-item::before {
  content: counter(instruction-counter) '.';
  position: absolute;
  color: $brown-800;
  font-weight: $font-weight-bold;
}
```

#### 4. Responsive Design Patterns\*\*

Implemented mobile-first responsive design with strategic breakpoints:

```
@media (max-width: 768px) {
  .recipe {
    max-width: 100%;
    padding: 0;
    margin: 0;
    border-radius: 0;
  }
}
```

#### 5. Typography & Design Systems\*\*

Learned to implement consistent typography using SCSS variables and proper font loading:

```
$young-serif: 'Young Serif', serif;
$outfit: 'Outfit', sans-serif;
$body-copy-font-size: 16px;
```

#### 6. Semantic Table Alternative\*\*

Used div elements with ARIA roles to create accessible table-like content:

```
<div class="nutrition__list" role="table" aria-label="Nutritional information">
  <div class="nutrition__item" role="row">
    <span class="nutrition__label" role="rowheader">Calories</span>
    <span class="nutrition__value" role="cell">277kcal</span>
  </div>
</div>
```

### **Continued Development**

Areas I want to focus on in future projects:

#### **1. Advanced SCSS Features**

- Explore mixins and functions for more reusable code
- Implement CSS Grid for more complex layouts
- Learn about SCSS maps for better color and spacing systems

#### **2. Enhanced Accessibility**

- Implement focus indicators that meet WCAG AAA standards
- Add support for reduced motion preferences
- Test with actual screen readers for better UX

#### **3. Modern CSS Features**

- Explore CSS Container Queries for component-based responsive design
- Implement CSS Custom Properties for dynamic theming
- Learn CSS Subgrid for more flexible layouts

#### **4. Build Process Improvement**

- Set up automated SCSS compilation
- Implement CSS purging for production builds
- Add linting and formatting tools

### **Useful Resources**

- [SCSS Documentation](https://sass-lang.com/documentation/)
- [MDN WebDocs - Accessibility](https://developer.mozilla.org/en-US/docs/Web/Accessibility)
- [CSS Tricks - Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [WebAIM - Skip Navigation Links](https://webaim.org/techniques/skipnav/)

### **Author**

- Frontend Mentor - [@twelvegoats](https://www.frontendmentor.io/profile/twelvegoats)
- GitHub - [@twelvegoats](https://github.com/twelvegoats)

```text
MIT License

Copyright (c) 2025 Sean Wildman

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
