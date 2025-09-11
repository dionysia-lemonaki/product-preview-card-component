# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshots](#screenshots)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learnt](#what-i-learnt)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshots

Mobile:

![](/images/mobile-screenshot.jpeg)

Desktop:

![](/images/desktop-screenshot.jpeg)

### Links

- [Solution URL](https://www.frontendmentor.io/solutions/product-preview-card-component-ggo4QTDDYv)
- [Live site URL](https://product-preview-card-component-dionysialemonaki.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learnt

I've been learning more about `meta` tags that improve SEO, like `<meta name="author" content="Author name here">` and `<meta name="description" content="Web page description here">`. I also explored `meta` tags that improve how a page looks when shared on social media, such as the Open Graph protocol and Twitter cards. I included them in this project and tested how the page looks using the handy [Meta Tags Toolkit](https://metatags.io/).

The project used different images for mobile and desktop, so I went with the `picture` element to make them responsive. Since I am working with a mobile-first workflow, the `img` serves as the default image for mobile devices, and the `source` element kicks in when the screen size is larger than `600px`:

```html
<picture>
  <source
    srcset="/images/image-product-desktop.jpg"
    media="(min-width: 37.5rem)"
  />
  <img
    src="/images/image-product-mobile.jpg"
    alt="Flat lay of CHANEL Gabrielle perfume bottle with a green leaf on each side."
  />
</picture>
```

Lastly, the design included two prices: one with a much larger font size and bright colour to represent the current price, and one with a strikethrough to represent the original, old price. Instead of using CSS for the strikethrough, I learnt about the `s` element, which represents content that's no longer relevant or accurate and automatically displays the text with a strikethrough. To make this clear to screen readers, I added screen reader-only text inside a `span` and visually hid it:

```html
<div>
  <p><span class="sr-only">Current Price: </span>$149.99</p>
  <p>
    <span class="sr-only">Original Price: </span>
    <s>$169.99</s>
  </p>
</div>
```
