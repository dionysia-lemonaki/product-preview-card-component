# Frontend Mentor - Product preview card component solution

This is my solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshots](#screenshots)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshots

Mobile:

![mobile screenshot](/assets/images/screenshots/mobile-screenshot.jpeg)

Desktop:

![desktop screenshot](/assets/images/screenshots/desktop-screenshot.jpeg)

### Links

- [Solution URL](https://www.frontendmentor.io/solutions/product-preview-card-component-aCWmqIX6qm)
- [Live site URL](https://product-preview-card-component-dionysialemonaki.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

The biggest learning experience with this project was getting the markup and structure right.

There were two images for this project: one for smaller screens and one for larger screens. To create responsive images, I used the `picture` element with a mobile-first approach. The `img` is the default for smaller mobile screens, and the image specified in the `source` is for larger screens. I also added meaningful alt text to convey the image to screen reader users.

```html
<picture>
  <source
    srcset="/assets/images/image-product-desktop.jpg"
    media="(width >= 37.5rem)"
  />
  <img
    src="/assets/images/image-product-mobile.jpg"
    alt="Flat lay of CHANEL Gabrielle Essence perfume bottle surrounded by two green leaves."
    class="card__image"
  />
</picture>
```

This project also needed extra info for screen reader users, especially for the price section. There are two prices: one larger and one much smaller with a strikethrough. To communicate that to screen-readers, I used `sr-only` text to convey which is the current price and which is the original one. For the original crossed-out price, I also used the `s` element to semantically represent that that price is no longer relevant.

```html
<div class="price flex-row">
  <p class="price__current text-preset-1">
    <span class="sr-only">Current price: </span>$149.99
  </p>
  <p class="price__original text-preset-5">
    <span class="sr-only">Original price: </span><s>$169.99</s>
  </p>
</div>
```

The favicon used in this project is from [Perfume icons created by Freepik - Flaticon](https://www.flaticon.com/free-icons/perfume)
