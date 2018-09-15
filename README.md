# HTML Me Something

Project Page: [Rebel Starfighters](https://trevorstinson.github.io/html-me-something/)

This page was created for the first assignment of LC101 Unit 2.  Since I am traveling for work and unable to present this assignment in class, I am providing an extra-detailed README.

I chose to make this assignment a tribute to a few of my favorite starfighters from *Star Wars*. The page includes a header with a hero image, text overlay, and a lead paragraph. This is followed by five sections, each with one image and a paragraph or two about a specific starfighter. The footer includes some information about the page, links for further reading, and footnotes.

I already have experience with HTML and CSS, so I created an extra challenge for myself to learn more about the build tools I've been using for front end work outside of class. This is covered in the Bonus Missions section at the end of this README.

## HTML

**`<p>`:** Seen in every section of the page. First appearance: line 15.

**`<header>`**: Used to contain the hero image, page title, and lead paragraph. It is given an orange background to distinguish it from the rest of the page, and to make sure the header text is visible if the hero image fails to load. First appearance: line 11.

**`<footer>`:** Used to contain the About, Further Reading, and Footnotes sections. It is given a blue background to distinguish it from the rest of the page. First appearance: line 104.

**`<main>`:** Used to contain the main body of the page where all of the articles are. Excludes the header and footer sections. First appearance: line 17.

**`<article>`:** Used to designate a section for each starfighter. Each of these contains an image followed by one or two paragraphs. First appearance: line 27.

**`<img>`:** One image appears at the beginning of each `<article>`. I had originally use this tag for the header image as well, but I swapped it out for a background image once I started working on the CSS. Using a background image made it easier to handle the text overlay for the page header. `<img>` worked well for the article images, though. First appearance: line 28.

**HTML entities:** I selected three HTML entities (along with two regular letters) to use as glyphs representing the different starfighters. (Each one looks like one of the starfighters in profile or from above.) I created a decorative section divider that appears as an `<aside>` between each `<article>`. Additionally, each glyph is a link to the section of the page for the starfighter which it represents (the one that looks like a Y-wing links to the `#ywing` id, etc.). Note the blue hover color indicating that each glyph is a link. First appearance: line 19.

## CSS

**Normalization:** I used normalize.css. I used Gulp & Sass to compile the stylesheets into a single document, so my own styles begin on line 333 of css/main.css.

**`margin` and `padding`:** Used throughout. Notice how margin and padding are combined with the decorative glyph element (discussed above) to provide spacing between the `<article>` elements. The padding and margin in the footer also required special attention.

**element selector:** Most of the stylesheet is constructed with element selectors.

**class selector:** The class `.decoration` is used for the section divider that I constructed with HTML entities. A class makes sense for this rather than an id because the element appears several times throughout the page.

**id selector:** `#lead` is used to style the lead paragraph in the header section since it is unique in styling. `#about`, `#further-reading`, and `#footnotes` are used to apply subtle differences to the three sections of the footer.

**Avoid adding HTML elements in order to achieve a specific visual effect:** There are only two areas where I modified the HTML for styling purposes. First, I removed the `<img>` tag I had originally placed in the header and replaced it with a background image so that I could achieve the text overlay and use `background-size: cover`. Second, during the styling phase of the project, I used HTML entities to create a section divider. I do not believe either of these breaks the spirit of the "don't use HTML for styling" rule.

**Use document-level and inline styles sparingly, and only when absolutely necessary:** All styles are in the `main.css` stylesheet. No document-level or inline styles are used.

## Extra Touches

- There is no 100% white or black on the page. All colors are derived from the featured images.
- The section divider helps with spacing and is also functional for navigation (each glyph links to the starfighter that it represents).
- The page is mobile-first and fully responsive. It was tested at various sizes in Safari, Google Chrome, and Firefox.
- The images are full width at small screen sizes, and have subtle rounded corners at large screen sizes.
- Subtle letter spacing is applied to make `<h1>` & `<h2>` more readable.
- Footnotes are linked in both directions.

## Bonus Missions

**GitHub Pages:** The page is published at [trevorstinson.github.io/html-me-something/](https://trevorstinson.github.io/html-me-something/)

**Yarn/Gulp/Sass:** In order to provide an extra challenge for myself, I decided to use this project to work on learning some more things about the build tools I've been using lately. I've used Yarn, Gulp, and Sass before, but I've mostly relied on preconfigured setups. For this project, I learned how to configure Yarn and Gulp myself. I also used Yarn to include normalize.css as a Node module rather than simply downloading or copying the stylesheet.