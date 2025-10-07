# Accessibility Audit Fixes

<!-- overall -->
## Issue 1: Missing Alt Text
- **Problem:** Lighthouse flagged missing `alt` attribute on images.  
- **Fix:** Added descriptive `alt` text 

## Issue 2: Meta description
- **Problem:** The page lacked a meta description, which affects SEO and discoverability.  
- **Fix:** Added a proper `<meta name="description" content="...">` tag within the `<head>` section.

<!-- navigation bar -->

## Issue 3: incorrect semantic
- **Problem:** Incorrect <div class="nav"> has no proper meaning 
- **Fix:** changed it to the correct semantics <nav class="nav">

## Issue 4: nav links
- **Problem:** Links were written as `<a href="#">`, which have no meaningful destination and are flagged by Lighthouse.
- **Fix:** added real destinations for accessibility  <a href="index.html">Home</a>
  <a href="portfolio.html">Portfolio</a>
  <a href="contact.html"

  ## Issue 5: text color visibility
- **Problem:** Navigation links had poor contrast (`#555` on a dark background), making them difficult to read.  
- **Fix:** Changed link color to white and added a hover outline (`outline: 2px solid lightpink;`) for improved visibility and accessibility.


<!-- main -->  

## Issue 6: incorrect semantic
- **Problem:** The main content area used `<div class="content">`, which is not semantically meaningful.  
- **Fix:** Replaced `<div>` with `<main class="content">` and closed with `</main>` to create a proper landmark for assistive technologies. 

## Issue 7: H1
- **Problem:** The `<h1>` heading did not have enough contrast to meet accessibility standards.  
- **Fix:** Added a subtle black `text-shadow` to improve readability and enhance visual contrast against the background.


## Issue 8: incorrect heading hierarchy
- **Problem:** The heading structure was skipped or out of order. You had an <h3> but possibly no <h2> above it, which confuses screen readers. 
- **Fix:** Changed to <h2> to maintain proper heading hierarchy <h2>Reach out for a quote today!</h2>


<!-- section -->

## Issue 9: incorrect semantics
- **Problem:** The <form> section was a <div> with no clear role. 
- **Fix:** Changed <div> to <section> to make styling the area simpler and added The form container used a `<div>` element, which lacks semantic meaning and makes it harder for assistive technologies to interpret and added `aria-labelledby` to link it to the section heading for improved accessibility and structure.  
  ```html
  <section class="form-section" aria-labelledby="contact-heading">
    <h2 id="contact-heading">Reach out for a quote today!</h2>
  </section>


<!-- Form -->

## Issue 10: Adjusting landmark
- **Problem:** improper <div class="submit-btn">Send Message</div> for embedding button
- **Fix:** Changed to proper element <button type="submit" class="submit-btn">Send Message</button>


## Issue 11: button contrast
- **Problem:** button element blended with background 
- **Fix:** Updated button background color to #0077cc and ensured the text color is white for better visibility

<!-- footer -->  

 ## Issue 12: text visibility
- **Problem:** Footer text color was too light (#555), providing insufficient contrast against its dark background
- **Fix:** altered to #ffffff better visibility
## Issue 13: incorrect semantics
- **Problem:** The footer content was placed inside a <div>, not a landmark so no meaning to assistive technologies
- **Fix:** Replaced <div> with <footer> and added aria-hidden="true" to the decorative iconso screen readers won’t redundantly read icon as “telephone emoji” <footer class="footer">
  <span class="icon" aria-hidden="true">📞</span>
  <span>Call me anytime!</span>
</footer>
