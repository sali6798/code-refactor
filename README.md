# code-refactor

## Changes made to the original code
* renamed the `<title>` to Horiseon
    * previous label was non descriptive/irrelevant to the company
* added #search-engine-optimization id to the SEO `<section>` in `<main>`
    * _Search Engine Optimization_ nav link referenced this id but did not jump to it when clicked because it did not exist
* added alt text to all images
    * need alt text to help with accessibility and screen readers or if the image fails to load
* changed some `<div>`'s to semantic HTML elements
    * `<div class="header">` => `<header>`
    * `<div>` => `<nav>`
    * `<div class="content">` => `<main class="content">`
        * `<div>`'s in .content => `<section>`
    * `<div class="benefits">` => `<aside class="content">`
    * `<div class="footer">` => `<footer>`
* consolidated CSS selectors
    * there were a few selectors that had the same properties as others 
        * .benefit-lead, .benefit-brand and .benefit-cost all had the same styling, so they were grouped together as `.benefits > div` to make it cleaner than listing the three class 
            * styling was applied to the `<h3>` and `<img>` for these classes. The `<h3>` were given a class .benefits-headings and `<img>` class .benefits-images to make it easier if changes wanted to be made to them
        * same as above applied for .search-engine-optimization, .online-reputation-management and .social-media-marketing they were grouped to `main > section`
            * there was also styling applied to the `<h2>` and `<img>` for these classes. The `<h2>` were given a class .section-headings and `<img>` class .section-images to make it easier if changes wanted to be made to them
* organized CSS by specifity and then in order of HTML layout
    * makes it easier to find a selector if searching by element then class then id and if within each group it is ordered the same way as the layout of the HTML




