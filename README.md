# 🌲 Casco Bay Property Care

A responsive one-page website for Casco Bay Property Care, a year-round property maintenance company in the Portland, Maine area. The page introduces the business's services (mowing in summer, plowing in winter, and odd jobs in between), shows a customer review, and includes a form for requesting a free quote.

**Live demo:** https://soyalrjbk.github.io/Casco-Bay-Property-Care/

[![Screenshot-2026-10-10-at-3-41-17-AM.png](https://i.postimg.cc/3NT1WNhJ/Screenshot-2026-10-10-at-3-41-17-AM.png)](https://postimg.cc/VrKnVY53)

## How It's Made:

**Tech used:**

<p align="left">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
</p>

The page is built with semantic HTML: a `<header>` with the business name and `<nav>`, a `<main>` area with the headline, hero image, and services, a review section, the quote form, and a `<footer>` with the service area and phone number. The nav links jump to each section using matching `id`s.

**Services:** the three service cards sit side by side using Flexbox. Each card takes up 32% of the width with a 2% gap between them, and a green top border ties them to the site's color scheme.

**Customer review:** the testimonial uses a `<blockquote>` with a green left border so it stands out from the rest of the content, with the customer's name and town underneath.

**Quote form:** the form is grouped in a `<fieldset>`, and every field has a `<label>` connected to its input with `for` and `id`, so clicking a label focuses the right field. It uses the right input types for each piece of info: `type="tel"` for the phone number, a `<select>` dropdown for the type of service, and a `<textarea>` for property details.

**Responsiveness:** media queries at 900px, 600px, and 400px adjust the layout for smaller screens. On tablets and phones, the header stacks and centers, the service cards stack into a single column, the hero image keeps its proportions, and on the smallest screens the text shrinks and the submit button stretches to full width.

## Optimizations

- Connect the form to a working service like Formspree or Netlify Forms. Right now it submits to `FreeQuote.html`, which doesn't exist, and the inputs need `name` attributes so their values are actually sent.
- Add `required` to the name and phone fields so the form can't be submitted empty.
- Make the phone number in the footer a `tel:` link so visitors on a phone can tap to call.
- Use `object-fit: cover` on the hero image so it doesn't stretch at its fixed 300px height on wide screens.
- Replace the `float` layout in the header with Flexbox, and use `gap` for the service cards instead of percentage margins.
- Use the Roboto font that's already loaded from Google Fonts. Right now the CSS sets everything to Arial.
- Rename the hero image file to something short without spaces (e.g. `mowing-crew.png`).

## Lessons Learned:

This project taught me how to build an accessible form the right way: grouping fields with `<fieldset>`, connecting every `<label>` to its input, and picking input types that match the data. It also gave me practice with responsive design, using media queries to rearrange the header and stack the service cards on smaller screens. Working on a small-business page made me think about what a real customer needs to see first: what the business does, proof that it's trusted, and an easy way to get in touch.
