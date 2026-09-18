## Mel-s-WEDE-POE 

**Project Overview**

MEL CAKES is a responsive bakery website developed to showcase a cake business and provide customers with information about available products, services, and contact details.
The purpose of this project is to create an attractive and user-friendly website where customers can explore cake offerings and learn more about the business.

**Project Objectives**
- Create a professional online presence for MEL CAKES.
- Design a user-friendly website interface.
- Display cake products and services.

**SITEMAP**
<img width="2720" height="1880" alt="mels_cakes_site_map" src="https://github.com/user-attachments/assets/6e0cd225-2707-4a6e-9228-ede10c62b4cb" />

**Project Structure**
<img width="1919" height="1079" alt="Screenshot 2026-08-16 214627" src="https://github.com/user-attachments/assets/7ba633bc-2df8-46e9-a300-0f55e59f8d8d" />

## Changelog
**PART 1**
The site is six plain HTML pages — no JavaScript, nothing fancy — for a home baker's business called Mel's Cakes & Treats. Every page follows the same basic pattern: a header area with the logo and business name, a nav bar with links to all six pages (Home, About Us, Products, Order, Enquiry, Contact), a main content area, and a simple copyright footer. The home page is mostly a welcome hero with a couple of photos and a call-to-action button. About Us is just three blocks of text covering the backstory, mission and vision. Products lays out six cards — cakes, cupcakes, cookies, dessert boxes and two wedding cake options — each with a picture, price and an "Order Now" link. Then there are three forms: a fairly detailed order form (customer info, product choice, size, flavour, delivery vs collection, payment method), a short enquiry form for people who just want a quote, and a contact form with the shop's details, two embedded Google Maps and a WhatsApp link.
It's solid for a first build, but there are a few rough edges worth cleaning up: the logo/business-name block is accidentally sitting inside the <head> on five of the six pages (so it won't actually show up in the browser), the order page is missing a proper page title and language tag, both forms don't actually submit anywhere since they point to action="#", and there's a small typo on the Enquiry page ("a Enquiry" instead of "an Enquiry").

**Part 2**
- Added `css/style.css` as the stylesheet for all six pages.
- Applied a CSS reset and set base typography: Arial for body text, Georgia
  for headings, a maroon/pink colour palette (`#6f2849` on `#fff7fa`), and
  smooth scroll behaviour.
- Built a fixed sidebar navigation (15rem wide, dark maroon background,
  white links, active/hover states with a highlight background and slide
  transform), collapsing to a horizontal bar on tablet and a stacked column
  on mobile.
- Styled the home page hero with a soft pink gradient background, rounded
  corners and a subtle shadow, plus a two-column responsive image grid.
- Added `.content-card` styling for the About page — white cards with a
  light border, rounded corners and soft shadow.
- Built the Products grid (`.product-grid`, `.product-card`,
  `.product-card-content`, `.price`) with card images, padding and a bold
  price label, responsive down to 3 / 2 / 1 columns depending on screen
  width.
- Added `.order-icon` button styling for "Order Now" links, with a pink
  background and darker hover state.
- Styled all forms consistently: `.form-group`, bold labels, full-width
  inputs/selects/textareas with rounded borders and a focus outline,
  `.form-actions` for button rows, and shared `.button` /
  `input[type="submit"/"reset"]` styling.
- Styled fieldsets and legends on the order form (rounded borders, coloured
  legend text) and radio/checkbox accent colours.
- Added Contact page styling: `.map-grid` for the embedded iframes and
  spacing for the `address` block.
- Styled the footer with a light pink background and centered text.
- Added `.header`, `.header-top`, `.logo` and `.logo-link` styling for the
  logo and business name block used across pages.
- Added responsive breakpoints at 64rem (tablet) and 40rem (mobile)
  covering nav layout, grid column counts and form button stacking.

  ## SCREENSHOT EVIDENCE OF RESPONSIVENESS**
**MOBILE**
<img width="785" height="983" alt="MOBILE" src="https://github.com/user-attachments/assets/fc3a2fe7-b58e-4961-86d5-4be671c1aa55" />

**TABLET**
<img width="747" height="957" alt="TABLET" src="https://github.com/user-attachments/assets/3df0c5c2-3d63-4466-bbef-34538de3b73e" />

**DESKTOP**
<img width="762" height="1007" alt="desktop" src="https://github.com/user-attachments/assets/086de512-04f8-46fd-a938-e097bffc24be" />


**Features**

- Home page introducing MEL CAKES.
- About Us section describing the business.
- Cake/product showcase.
- Contact information section.
- Responsive website design.
- Attractive bakery-themed layout.


## REFERENCES
Berners-Lee, T. and Connolly, D. (1995) Hypertext Markup Language - 2.0. Available at: https://www.rfc-editor.org/rfc/rfc1866 (Accessed: 18 September 2026).
Marcotte, E. (2011) Responsive web design. New York: A Book Apart.
Mozilla Developer Network (2024) CSS: Cascading Style Sheets. Available at: https://developer.mozilla.org/en-US/docs/Web/CSS (Accessed: 18 September 2026).
Nielsen, J. (2020) 10 usability heuristics for user interface design. Available at: https://www.nngroup.com/articles/ten-usability-heuristics/ (Accessed: 18 September 2026).
W3C (2023) Web Content Accessibility Guidelines (WCAG) 2.2. Available at: https://www.w3.org/TR/WCAG22/ (Accessed: 18 September 2026).
W3C (2022) HTML: Living Standard. Available at: https://html.spec.whatwg.org/ (Accessed: 18 September 2026).







