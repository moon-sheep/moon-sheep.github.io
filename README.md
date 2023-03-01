# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size (I stuck with desktop view because I'm only starting out with HTML and CSS)
- See hover and focus states for interactive elements

### Links

- Solution URL: https://github.com/moon-sheep/product-preview-desktop.git
- Live Site URL: https://moon-sheep.github.io/product-preview-desktop/

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid

- CodePen
- Visual Studio Code

### What I learned

1. Linking fonts using Google Fonts

Previously, I've only used pre-existing fonts but this challenge included Google Font links for different blocks of text. So I did research on how to add it into my HTML and CSS which turns out to mainly copy pasting code that Google Fonts make for you. Very convenient.

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,700&family=Montserrat:wght@500;700&display=swap" rel="stylesheet">
```

2. Adding SVG icon within button input

One of the bigger struggles since I've never worked with icons before. After finding a code that works, I backtracked into studying position and ::before which I understand in theory but I definitely still need to try more in practice. The end result is close to what I wanted to do but there's a lot more room for improvement and CSS to learn. 

```css
label::before {
  content: "";
  position: absolute;
  left: 60px;
  top: 0;
  bottom: 25px;
  width: 15px;
  background: url(https://moon-sheep.github.io/product-card-challenge/icon-cart.svg) center / contain no-repeat; 
}
```

3. Using minmax() for more secure grid area

This is a tip I discovered that helped me fix my grid layout more. Initially, a lot of content was unnecessarily overlapping and there was a lot of space I didn't know how to get rid of, especially at the bottom of the div. Eventually, I realized that fr was mostly not helping. Using a minmax() for the rows achieved removed all the excess space and cleaned up the content. In the end, it looked like how I wanted to which I'm kinda proud of.

```css
grid-template-rows: repeat(5, minmax(1fr, 75px));
```

### Continued development

1. Grid 

I understand how they work but actually doing them is hard. I want to practice using it more and with unconventional layouts until it hopefully sticks to muscle memory. With CodePen, I couldn't use devtools to see the grid on liveview which made sizing difficult, as a visual learner, but I think I got most of it down regardless. I just cleaned it up on VSC with devtools. Overall, I think I need a better understanding of how a viewport works and how it's sized versus just eyeing measurements.

2. Icon within button

I think this involves more advanced CSS but I really want to figure out how to properly code an SVG icon within input with more flexibility. I think what I did worked but was also very stiff. 

### Useful resources

- https://css-tricks.com/you-want-minmax10px-1fr-not-1fr/ - This article helped me layout the grid properly to avoid messy overlapping. Will definitely keep it mind.
- https://stackoverflow.com/questions/40808493/how-to-add-a-svg-icon-within-an-input - This taught me how to use psuedo label class for adding SVG icons. It works though I'm still about other methods. 

## Author

- moon-sheep 
