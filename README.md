# Frontend Mentor - Clipboard landing page solution

This is a solution to the [Clipboard landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/clipboard-landing-page-5cc9bccd6c4c91111378ecb9). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page

### Screenshot

![Desktop](/images/solution-screenshot-desktop.png)
![Mobile](/images/solution-screenshot-mobile.png)

### Links

- Solution URL: [https://github.com/HaiDangN/clipboard-landing-page]
- Live Site URL: [https://haidangn.github.io/clipboard-landing-page/]

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid

### What I learned

Learned how to give a button some thickness and give it a shadow:

```css
.button--ios {
    background-color: rgb(38, 186, 164);
    box-shadow: 
        0 .4rem 1rem rgba(38, 186, 164, .5),
        0 .1rem 0 rgb(30, 111, 99);
}
```

I learned that if I want to crop off the left side of an image on a page, i can expand the width of the parent to more than 100% instead of having to transform the image. Note that if you do this, you have to apply `overflow-x: hidden;` to the parent container or else it will spill out.

I learned how to get better at BEM conventions. Here is the html for one of the sections:

Feature Feature--snippets
    Section-header
    Description
    Feature-body--snippets (I probably should've created feature-body)
        Feature__subfeatures--snippets (Again, feature__subfeatures)
            Feature__subfeature Feature__subfeature--snippets

```html
    <section class="feature feature--snippets">
      <div class="section-header">
        <h2>Keep track of your snippets</h2>
        <p class="description">
          Clipboard instantly stores any item you copy in the cloud,
          meaning you can access your snippets immediately on all your
          devices. Our Mac and iOS apps will help you organize everything.
        </p>
      </div>
      <div class="feature__body--snippets">
        <img src="images/image-computer.png" alt="Image of mac monitor with a background of beach waves with a white modal window and a green check with a circle.">
        <div class="feature__subfeatures--snippets">
          <div class="feature__subfeature feature__subfeature--snippets">
```

Use `border-radius: 9999px` for fully rounded pill buttons (yes that is conventional)
