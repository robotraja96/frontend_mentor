# Frontend Mentor - Blog preview card solution

This is a solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)




## Overview
A Blog Preview Card built using basic HTML and CSS with Hover effect.

### The challenge

Users should be able to:

- See hover and focus states for all interactive elements on the page

### Screenshot

![My Output](E:\Frontend_Mentor\Blog_Preview_Card\blog-preview-card-main\blog_preview_card.png)



### Links

- Solution URL: [Add solution URL here](https://github.com/robotraja96/frontend_mentor/tree/main/Blog_Preview_Card/blog-preview-card-main)
- Live Site URL: [Add live site URL here](https://frontendmentor-blog-preview-card-ma-seven.vercel.app)

## My process
Utilizing stuff I learned in the previous QR Code project, I started from outside to in and top to bottom. This time I used a container with a card component justified at the center instead of making `<body>` a flexbox. Most of this was quite easy and the flow came quite naturally. There was no real block point actually.
One thing I realized after completion is that the custom fonts in the assets/fonts folder were not properly being implemented or computed. This prompted me to search for proper import and application of local font files. 

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Figtree font




### What I learned

Working through this project helped me master local font imports, variable font weights, CSS color syntax, and interactive hover states.

Proper @font-face syntax for TTF files:
  I learned that inside format(), the browser expects 'truetype' rather than 'ttf'. In addition, since I was using a variable font, defining the weight range (500 800) allowed the single font file to support both medium and extra bold variants smoothly:

```CSS
@font-face {
  font-family: 'Figtree';
  src: url('./assets/fonts/Figtree-VariableFont_wght.ttf') format('truetype');
  font-weight: 500 800;
  font-style: normal;
  font-display: swap;
}
```

Font family inheritance vs weight declarations:
  Instead of trying to reference font variants by fabricated names like 'Figtree Medium' or 'Figtree Extra Bold', you define the single family name ('Figtree') once and let font-weight: 500 or font-weight: 800 handle the rendering.

Interactive hover effects and HSL corrections:
  I implemented the required hover state on the blog title using the :hover pseudo-class and fixed HSL syntax issues where missing percentage signs (e.g. hsl(0, 0, 7%) vs hsl(0, 0%, 7%)) previously broke color evaluation:

```CSS
h1 {
  font-size: 24px;
  font-weight: 800;
  color: hsl(0, 0%, 7%);
  font-family: 'Figtree', sans-serif;
  transition: color 0.2s ease;
}

h1:hover {
  color: #F4D04E;
  cursor: pointer;
}
```

### Continued development
In future projects, I will continue to focus on:
    - Deepening my understanding of variable fonts and performance optimization.

    - Semantic HTML choices (such as wrapping cards in <article> tags and titles in anchor <a> links for authentic card navigation).

    - Implementing accessible :focus-visible styles alongside hover states for keyboard-only users.
### Useful resources
    - MDN Web Docs: @font-face - Helped clarify the correct format string ('truetype') and variable font-weight ranges.

    - MDN Web Docs: :hover pseudo-class - Clear reference on structuring hover state transitions.


### AI Collaboration
Tools used: Claude

How it was used:

  - Consulted Claude to debug why the custom local fonts were not computing or rendering in the browser.

  - Claude guided me to check the @font-face syntax, pointing out that format('truetype') was needed rather than format('ttf').

  - Claude also voluntarily flagged that assigning non-existent font-family names (such as 'Figtree Medium' and 'Figtree Extra Bold') prevented the browser from loading the face, helping me understand that font-weight should control thickness instead.

  - Identified an invalid hsl() syntax error where hsl(0, 0, 7%) was missing the % unit on the saturation parameter (hsl(0, 0%, 7%)).

## Author

- Frontend Mentor - [@robotraja96](https://www.frontendmentor.io/profile/robotraja96)



