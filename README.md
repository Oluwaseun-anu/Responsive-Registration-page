# Frontend Mentor - Intro component with sign up form solution

This is a solution to the [Intro component with sign up form challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/intro-component-with-signup-form-5cf91bd49edda32581d28fd1). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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


## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page
- Receive an error message when the `form` is submitted if:
  - Any `input` field is empty. The message for this error should say *"[Field Name] cannot be empty"*
  - The email address is not formatted correctly (i.e. a correct email address should have this structure: `name@host.tld`). The message for this error should say *"Looks like this is not an email"*

### Screenshot

(assets/images/screenshot.jpg)


### Links

- Solution URL: (https://github.com/Oluwaseun-anu/Responsive-Registration-page)
- Live Site URL: (https://responsive-registration-page.vercel.app/)

## My process

I structured my content with HTML, then added styles using CSS before writing the Javascript for the form validation.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Media Queries
- JavaVanilla JavaScript for form validation


### What I learned

During this project, I focused on implementing a responsive client-side form validation using vanilla JavaScript. Key learnings include:

Responsive Design: Ensuring the layout adapts well to different screen sizes using media queries.

Event Handling: Attaching submit event listeners to forms and preventing default submission.

DOM Manipulation: Dynamically adding and removing CSS classes (error, visible) to change element styles and visibility based on validation status.

Input Validation: Implementing checks for empty fields and using regular expressions for email format validation.

Error Messaging: Displaying specific error messages next to the relevant input fields.

Example of validation logic
function setError(element, message) {
    const inputGroup = element.parentElement;
    const errorDisplay = inputGroup.querySelector('.error-message');
    const errorIcon = inputGroup.querySelector('.error-icon');

    errorDisplay.innerText = message;
    errorDisplay.style.display = 'block';
    element.classList.add('error');
    errorIcon.classList.add('visible');
    element.setAttribute('placeholder', '');
}

function isValidEmail(email) {
    const re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    return re.test(String(email).toLowerCase());
}

### Continued development

I plan to continue practicing:

How to write better responsive pages using media queries.

Refactoring JavaScript code for better modularity and reusability.

### Useful resources

- (https://www.w3schools.com/css) - This helped me for with my Flexbox and Media queries.


## Author

- Website - [Oluwaseun](https://responsive-registration-page.vercel.app/)
- Frontend Mentor - [@Oluwaseun-anu](https://www.frontendmentor.io/profile/Oluwaseun-anu)



