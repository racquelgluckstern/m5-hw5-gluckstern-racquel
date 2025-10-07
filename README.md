# Accessibility Audit Fixes

<!-- overall -->
## Issue 1: Missing Alt Text
- **Problem:** Lighthouse flagged missing `alt` attribute on images.  
- **Fix:** Added descriptive `alt` text 

## Issue 2: Meta description
- **Problem:** needs a meta description for SEO purposes
- **Fix:** added <meta description 

<!-- navigatioon bar -->

## Issue 3: incorrect semantic
- **Problem:** Incorrect <div class="nav"> has no proper meaning 
- **Fix:** changed it to the correct semantics <nav class="nav">

## Issue 4: nav links
- **Problem:** <a href="#"> with no clear destination or accessible labeling. Lighthouse flagged them because # alone isn’t meaningful.
- **Fix:** added real destinations for accessibility  <a href="index.html">Home</a>
  <a href="portfolio.html">Portfolio</a>
  <a href="contact.html"

  ## Issue 5: text color visibility
- **Problem:** nav bar no contrast colors for accesibility 
- **Fix:** nav a was #555, now white for contrast + nav hover outline: 2px solid lightpink


<!-- main -->  

## Issue 6: incorrect semantic
- **Problem:** Incorrect <div class="content"> has no proper meaning for the main section
- **Fix:** changed it to <main class="content"> for semantic landmark and closed it off </main>

## Issue 7: H1
- **Problem:** not enough contract accesibility
- **Fix:** text-shadow black to improve text visibility

## Issue 8: incorrect heading hierarchy
- **Problem:** The heading structure was skipped or out of order. You had an <h3> but possibly no <h2> above it, which confuses screen readers. 
- **Fix:** Changed to <h2> to maintain proper heading hierarchy <h2>Reach out for a quote today!</h2>


<!-- section -->

## Issue 9: incorrect semantics
- **Problem:** The <form> section was a <div> with no clear role. 
- **Fix:** Changed <div> to <section> to make styling the area simpler and added aria-labelledby for accessibility.


<!-- Form -->

## Issue 10: Adjusting landmark
- **Problem:** unecessary div <div class="submit-btn">Send Message</div> for embedding button
- **Fix:** Changed div button to actual <button> html

## Issue 11: button contrast
- **Problem:** class="submit-btn" lacked contrast against the light background
- **Fix:** Changed button color to blue for visibility and form text to black

<!-- footer -->  

 ## Issue 12: text visibility
- **Problem:** not enough contrast colors for accesibility 
- **Fix:** was #555, now white for better visibility

## Issue 13: incorrect semantics
- **Problem:** Footer text is inside a <div> as a class which isnt proper/no semantic meaning. 
- **Fix:** Used <footer> instead of <div> to add meaning with aria-hidden="true" so screen readers won’t redundantly read icon as “telephone emoji”