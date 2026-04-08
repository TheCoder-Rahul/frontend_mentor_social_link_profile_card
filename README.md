# Frontend Mentor - Social proof section solution

This is a solution to the [Social proof section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/social-proof-section-6e0qTv_bA). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

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

- View the optimal layout for the section depending on their device's screen size

### Screenshot

![Design screenshot](https://github.com/TheCoder-Rahul/frontend_mentor_social_proof_section/blob/main/project_screenshot.png)

### Links

- 👉 [Solution URL](https://github.com/TheCoder-Rahul/frontend_mentor_social_proof_section.git)
- 👉 [Live Site URL](https://thecoder-rahul.github.io/frontend_mentor_social_proof_section/)

## My process

### Built with

- 👉 **Markup:** Semantic HTML5 for better accessibility and SEO.
- 👉 **Styling:** CSS3 with Custom Properties (variables) for a maintainable color scheme, font-properties, and different sizes.
- 👉 **Layout:** Flexbox for centering the card and managing the internal alignment.
- 👉 **Workflow:** Mobile-first approach and Responsive Design using Media Queries.

### What I learned

Check the code snippets attached below:

```html
<main>
  <section class="main_desc">
    <h1 class="title">10,000+ of our users love our products.</h1>
    <p class="desc">We only provide great products combined with excellent customer service. See what our satisfied customers are saying about our services.</p>
  </section>
  <section class="ratings">
    <article>
      <div class="rating_stars">
        <img src="images/icon-star.svg" alt="Stars Yellow Filled Icon for Rating">
        <img src="images/icon-star.svg" alt="Stars Yellow Filled Icon for Rating">
        <img src="images/icon-star.svg" alt="Stars Yellow Filled Icon for Rating">
        <img src="images/icon-star.svg" alt="Stars Yellow Filled Icon for Rating">
        <img src="images/icon-star.svg" alt="Stars Yellow Filled Icon for Rating">
      </div>
      <p>Rated 5 Stars in Reviews</p>
    </article>
    <article>
      <div class="rating_stars">
        <img src="images/icon-star.svg" alt="Stars Yellow Filled Icon for Rating">
        <img src="images/icon-star.svg" alt="Stars Yellow Filled Icon for Rating">
        <img src="images/icon-star.svg" alt="Stars Yellow Filled Icon for Rating">
        <img src="images/icon-star.svg" alt="Stars Yellow Filled Icon for Rating">
        <img src="images/icon-star.svg" alt="Stars Yellow Filled Icon for Rating">
      </div>
      <p>Rated 5 Stars in Report Guru</p>
    </article>
    <article>
      <div class="rating_stars">
        <img src="images/icon-star.svg" alt="Stars Yellow Filled Icon for Rating">
        <img src="images/icon-star.svg" alt="Stars Yellow Filled Icon for Rating">
        <img src="images/icon-star.svg" alt="Stars Yellow Filled Icon for Rating">
        <img src="images/icon-star.svg" alt="Stars Yellow Filled Icon for Rating">
        <img src="images/icon-star.svg" alt="Stars Yellow Filled Icon for Rating">
      </div>
      <p>Rated 5 Stars in BestTech</p>
    </article>
  </section>
  <section class="testimonials">
    <article>
      <header>
        <img src="images/image-colton.jpg" alt="Profile Pic of Colton Smith">
        <section class="testmonial_provider">
          <h2>Colton Smith</h2>
          <p>Verified Buyer</p>
        </section>
      </header>
      <section><p>"We needed the same printed design as the one we had ordered a week prior. Not only did they find the original order, but we also received it in time. Excellent!"</p></section>
    </article>
    <article>
      <header>
        <img src="images/image-irene.jpg" alt="Profile Pic of Irene Roberts">
        <section class="testmonial_provider">
          <h2>Irene Roberts</h2>
          <p>Verified Buyer</p>
        </section>
      </header>
      <section><p>"Customer service is always excellent and very quick turn around. Completely delighted with the simplicity of the purchase and the speed of delivery."</p></section>
    </article>
    <article>
      <header>
        <img src="images/image-anne.jpg" alt="Profile Pic of Anne Wallace">
        <section class="testmonial_provider">
          <h2>Anne Wallace</h2>
          <p>Verified Buyer</p>
        </section>
      </header>
      <section><p>"Put an order with this company and can only praise them for the very high standard. Will definitely use them again and recommend them to everyone!"</p></section>
    </article>
  </section>
</main>
```
```css
*, *::before, *::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
:root {
  --white: hsl(0, 0%, 100%);
  --soft-pink: hsl(333, 80%, 67%);
  --very-dark-magenta: hsl(300, 43%, 22%);
  --dark-grayish-magenta: hsl(303, 10%, 53%);
  --light-grayish-magenta: hsl(300, 24%, 96%);
}
body {
  display: flex;
  font-size: 1rem;
  min-height: 100vh;
  position: relative;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  background-color: var(--white);
  font-family: "League Spartan", sans-serif;
}
body::before, body::after {
  content: '';
  width: 100%;
  height: 232px;
  position: absolute;
  inset: 0 auto auto 0;
  display: inline-block;
  background-size: cover;
  background-repeat: no-repeat;
  background-image: url(./images/bg-pattern-top-mobile.svg);
}
body::after {
  height: 503px;
  inset: auto 0 0 auto;
  background-image: url(./images/bg-pattern-bottom-mobile.svg);
}
main {
  gap: 3rem;
  display: grid;
  margin-block: 6rem;
  text-align: center;
  align-items: center;
  width: min(65rem, 90%);
}
.title {
  line-height: 80%;
  margin-block-end: 1.5rem;
  color: var(--very-dark-magenta);
  font-size: clamp(1.5rem, calc(2vw + 2rem), 3.5rem);
}
.desc {
  font-weight: 500;
  line-height: 1.25;
  color: var(--dark-grayish-magenta);
  font-size: clamp(1rem, calc(1.5vw + 0.725rem), 1.25rem);
}
.ratings, .testimonials {
  gap: 1rem;
  display: flex;
  flex-direction: column;
}
.ratings article {
  gap: 1rem;
  display: flex;
  font-weight: 700;
  padding: 1rem 3rem;
  align-items: center;
  border-radius: 0.5rem;
  flex-direction: column;
  justify-content: center;
  color: var(--very-dark-magenta);
  background-color: var(--light-grayish-magenta);
}
.testimonials article {
  padding: 2rem;
  text-align: start;
  color: var(--white);
  border-radius: 0.5rem;
  background-color: var(--very-dark-magenta);
}
.testimonials article header {
  gap: 1.5rem;
  display: flex;
  align-items: center;
  margin-block-end: 2rem;
  justify-content: flex-start;
}
.testimonials img {
  width: 2.5rem;
  height: 2.5rem;
  border-radius: 50%;
}
.testimonials p {
  line-height: 1.5;
}
.testmonial_provider h2 {
  font-size: 1.125rem;
}
.testmonial_provider p {
  line-height: 1.2;
  color: var(--soft-pink);
}
.attribution { font-size: 0.6875rem; text-align: center; }
.attribution a { color: var(--very-dark-magenta); }

@media (min-width: 768px) {
  body::before {
    width: 584px;
    height: 362px;
    background-image: url(./images/bg-pattern-top-desktop.svg);
  }
  body::after {
    width: 1085px;
    height: 673px;
    background-image: url(./images/bg-pattern-bottom-desktop.svg);
  }
  main {
    text-align: start;
    grid-template-columns: repeat(2, 1fr);
  }
  .ratings, .testimonials {
    align-items: center;
  }
  .ratings article {
    width: 26.25rem;
    flex-direction: row;
    display: inline-flex;
  }
  .ratings article:first-child, .testimonials article:first-child {
    align-self: flex-start;
  }
  .ratings article:last-child, .testimonials article:last-child {
    align-self: flex-end;
  }
  .testimonials {
    height: 17rem;
    flex-direction: row;
    grid-column: span 2;
  }
  .attribution { position: absolute; bottom: 0.5rem; }
}
```

## Author

- 👉 GitHub - [TheCoder-Rahul](https://github.com/TheCoder-Rahul)
- 👉 Frontend Mentor - [@TheCoder-Rahul](https://www.frontendmentor.io/profile/TheCoder-Rahul)
- 👉 LinkedIn - [@Rahul Kumar](https://www.linkedin.com/in/rahul-the-developer/)