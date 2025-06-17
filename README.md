# Frontend Mentor - Fylo dark theme landing page solution

This is a solution to the [Fylo dark theme landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/fylo-dark-theme-landing-page-5ca5f2d21e82137ec91a50fd). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page

### Screenshot

![screenshot of the solution](./screenshot.png)

### Links

- Solution URL: [github.com/Emmanuel-Xs/fylo-dark-theme-landing-page-master](https://github.com/Emmanuel-Xs/fylo-dark-theme-landing-page-master)
- Live Site URL: [fylo-dark-theme-landing-page-master-self.vercel.app](https://fylo-dark-theme-landing-page-master-self.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties or variables
- Flexbox
- Mobile-first workflow

### What I learned

To match the design of the hero section as close as possible, i had to learn how to stack colors and image on each other using `linear-gradient()` and even used an inset box-shadow to add background for the paragraph text of the hero section.

checkout the code below

```css
.hero {
  /* border: 1px solid red; */
  background-image: url("./images/bg-curvy-mobile.svg"), linear-gradient(to
        bottom, var(--primary-color-intro-email), var(--primary-color-intro-email));
  background-repeat: no-repeat;
  background-size: contain, cover;
  background-position: center bottom 47cqmin, top;
  box-shadow: inset 0 -48cqmin 0 0 var(--primary-color-main);
  min-height: 60svh;

  @media (min-width: 360px) {
    background-position: center bottom 57cqmin, top;
    box-shadow: inset 0 -58cqmin 0 0 var(--primary-color-main);
  }

  @media (min-width: 375px) {
    background-position: center bottom 53cqmin, top;
    box-shadow: inset 0 -54cqmin 0 0 var(--primary-color-main);
  }

  @media (min-width: 400px) {
    background-position: center bottom 39cqmin, top;
    box-shadow: inset 0 -40cqmin 0 0 var(--primary-color-main);
  }

  @media (min-width: 420px) {
    background-position: center bottom 31cqmin, top;
    box-shadow: inset 0 -32cqmin 0 0 var(--primary-color-main);
  }

  @media (min-width: 480px) {
    background-position: center bottom 22cqmin, top;
    box-shadow: inset 0 -23cqmin 0 0 var(--primary-color-main);
  }
  @media (min-width: 540px) {
    background-position: center bottom 16cqmin, top;
    box-shadow: inset 0 -17cqmin 0 0 var(--primary-color-main);
  }
  @media (min-width: 580px) {
    background-position: center bottom 15cqmin, top;
    box-shadow: inset 0 -16cqmin 0 0 var(--primary-color-main);
  }
  @media (min-width: 620px) {
    background-position: center bottom 11cqmin, top;
    box-shadow: inset 0 -12cqmin 0 0 var(--primary-color-main);
  }
  @media (min-width: 680px) {
    background-position: center bottom 8cqmin, top;
    box-shadow: inset 0 -9cqmin 0 0 var(--primary-color-main);
  }
  @media (min-width: 740px) {
    background-position: center bottom 5cqmin, top;
    box-shadow: inset 0 -6cqmin 0 0 var(--primary-color-main);
  }
  @media (min-width: 760px) {
    background-position: center bottom 3cqmin, top;
    box-shadow: inset 0 -4cqmin 0 0 var(--primary-color-main);
  }

  @media (min-width: 768px) {
    background-image: url("./images/bg-curvy-desktop.svg"), linear-gradient(to
          bottom, var(--primary-color-intro-email), var(--primary-color-intro-email));
    min-height: 100vh;
    background-size: 100% 50vh, cover;
    background-position: center bottom, top;
    box-shadow: none;
  }
  padding-top: 20px;
  @media (min-width: 375px) {
    padding-top: 16px;
  }
}
```

I also learnt how to use css for input validation with the help of the `:user-valid` pseudo-class which validates an input only when the user is interacting with it

here is the code

```css
.cta-form {
  span {
    color: var(--accent-color-error);
    font-size: 12px;
  }

  &:has(input:user-invalid) span::before {
    content: attr(data-error);
  }

  &:has(input:user-valid) span::before {
    content: "";
  }

  /* error for desktop only */
  & > span {
    padding-inline-start: 8em;

    @media (max-width: 768px) {
      display: none;
    }
  }
}
```

### Continued development

I would love to be able to build more stuffs with gradients and also use some tricks to solve special problems.

## Author

- Frontend Mentor - [Emmanuel-Xs](https://www.frontendmentor.io/profile/Emmanuel-Xs)
- Twitter - [xs_emmanuel](https://x.com/xs_emmanuel)
