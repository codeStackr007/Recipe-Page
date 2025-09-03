# Frontend Mentor - Recipe Page Solution

This is my solution to the [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQH). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
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

### The challenge

The goal was to build a responsive recipe page that matches the provided design as closely as possible. Users should be able to view the optimal layout for the interface depending on their device's screen size.

### Screenshot

![Desktop Screenshot](recipe-page-main/design/desktop-design.jpg)
![Mobile Screenshot](recipe-page-main/design/mobile-design.jpg)

### Links

- Solution URL: [GitHub Repository](https://github.com/codeStackr007/recipe-page-solution)
- Live Site URL: [Live Demo](https://codestackr007.github.io/recipe-page-solution/)

## My process

### Built with

- Semantic HTML5 markup with proper document structure
- CSS custom properties (CSS variables) for consistent theming
- Flexbox for centering and layout alignment
- Mobile-first responsive design with media queries
- Google Fonts integration (Outfit and Young Serif)
- Custom CSS counters for ordered lists
- Semantic elements (`<main>`, `<article>`, `<section>`, `<figure>`)
- Accessible table structure for nutrition information

The project follows a clean, semantic HTML structure with a main container holding a recipe card article. Each section (preparation, ingredients, instructions, nutrition) is properly marked up with semantic elements and styled using CSS custom properties for maintainable code.

### What I learned

This project significantly enhanced my understanding of modern CSS techniques and semantic HTML structure. Key learnings include:

**CSS Custom Properties & Color Management:**
I implemented a comprehensive color system using CSS variables, making the design easily maintainable and consistent throughout:

```css
:root {
  --clr-white: hsl(0, 0%, 100%);
  --clr-stone-100: hsl(30, 54%, 90%);
  --clr-stone-150: hsl(30, 18%, 87%);
  --clr-stone-600: hsl(30, 10%, 34%);
  --clr-stone-900: hsl(24, 5%, 18%);
  --clr-brown-800: hsl(14, 45%, 36%);
  --clr-rose-800: hsl(332, 51%, 32%);
  --clr-rose-50: hsl(330, 100%, 98%);
}
```

**Custom List Styling with CSS Counters:**
I mastered the art of creating custom list markers using `::before` pseudo-elements and CSS counters for the instructions section:

```css
.instructions__list {
  counter-reset: instructions-counter;
}

.instructions__item::before {
  content: counter(instructions-counter) ".";
  counter-increment: instructions-counter;
  position: absolute;
  left: 0.75rem;
  color: var(--clr-brown-800);
  font-weight: var(--fw-bold);
}
```

**Responsive Design Implementation:**
I successfully implemented a mobile-first approach with strategic breakpoints, particularly focusing on the card layout transformation at smaller screen sizes:

```css
@media (max-width: 992px) {
  .recipe-card {
    padding: 0;
  }

  .recipe-card__image {
    border-radius: 10px 10px 0 0;
  }

  .recipe-card__content {
    padding: 2.5rem 2rem;
  }
}
```

I also learned to create accessible table layouts with proper spacing and visual hierarchy for the nutrition information section.

### Continued development

Moving forward, I plan to enhance similar projects by:

- Adding JavaScript functionality for interactive features like ingredient checklist toggles
- Implementing a serving size calculator that dynamically updates nutrition values
- Exploring CSS Grid for more complex recipe layouts and card arrangements
- Enhancing accessibility with comprehensive ARIA labels and keyboard navigation
- Adding print-friendly styles for recipe printing functionality
- Incorporating CSS animations for better user experience

### Useful resources

- [MDN Web Docs on CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/--*) - Essential for understanding CSS variables and their implementation
- [MDN Web Docs on CSS Counters](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Counter_Styles/Using_CSS_counters) - Critical for implementing custom numbered lists
- [Google Fonts](https://fonts.google.com/) - For typography integration and font optimization
- [MDN Web Docs on CSS Pseudo-elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements) - Helped with custom list markers and decorative elements
- [CSS-Tricks Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) - Reference for centering and layout techniques

## Author

- Frontend Mentor - [@codeStackr007](https://www.frontendmentor.io/profile/codeStackr007)
- GitHub - [@codeStackr007](https://github.com/codeStackr007)

---
