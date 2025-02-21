# Frontend Mentor - Loopstudios landing page solution

This is a solution to the [Loopstudios landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/loopstudios-landing-page-N88J5Onjw). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Frontend Mentor - Loopstudios landing page solution](#frontend-mentor---loopstudios-landing-page-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
  - [Author](#author)


## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page

### Screenshot

![Screenshot](/images/screenshot.jpeg)


### Links

- Solution URL: [Ver](https://github.com/rafopm/loopstudios-landing-page)
- Live Site URL: [Ver](https://rafopm.github.io/loopstudios-landing-page/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- [Astro](https://astro.build/) - JS library

### What I learned


```html
<div class="cards-container">
        {
            cards.map((card) => (
                <div class="card">
                    <img
                        src={card.img}
                        srcset={`${card.img} 400w, ${card.img} 750w,${card.imgdesktop} 1440w`}
                        alt={card.alt}
                    />
                    <span>{card.title}</span>
                </div>
            ))
        }
        <button>See all</button>
    </div>
```
```css

    .card {
        position: relative;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width: auto;
        max-width: 100%;
        padding: 0;
        margin: 0 auto;
        overflow: hidden;
    }

    .card img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        display: block;
        margin: 0;
    }

    .card::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 50%;
        height: 100%;
        background: linear-gradient(to right, rgba(0, 0, 0, 0.5), transparent);
        z-index: 1;
    }

    .card span {
        position: absolute;
        bottom: 20px;
        left: 20px;
        color: var(--white);
        font-size: 24px;
        font-family: var(--ff-josefin);
        font-weight: 300;
        z-index: 2;
        text-transform: uppercase;
        text-align: left;
        width: 130px;
    }
```

## Author

- Website - [Rafael Pampavilca](https://rafopm.netlify.app/)
- Frontend Mentor - [@rafopm](https://www.frontendmentor.io/profile/rafopm)
