## 1. Aim

To create a responsive article and portfolio webpage in which text, headings, paragraphs, and images adjust properly to different screen sizes using HTML and CSS.

## 2. Objectives

- Create a responsive article and portfolio webpage.
- Use `rem`, `em`, and `clamp()` for responsive typography.
- Make images responsive using `max-width: 100%` and `height: auto`.
- Set a suitable `max-width` on the content container.
- Improve text readability, line length, and spacing.
- Prevent text overflow and image stretching.
- Test the webpage on mobile and desktop screens.

## 3. Project Structure

Create the following files:

```text
Assignment-9.2/
├── index.html
├── style.css
└── screenshots/
    ├── mobile.png
    └── desktop.png
```

## 4. HTML Code (index.html)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">

    <!-- Responsive viewport for mobile devices -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <meta
        name="description"
        content="A responsive article and portfolio webpage demonstrating responsive typography and images."
    >

    <title>Responsive Typography & Images</title>

    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Website Header -->
    <header class="site-header">
        <div class="header-container">
            <a href="#home" class="logo">CreativeSpace</a>

            <nav class="navigation" aria-label="Main navigation">
                <a href="#home">Home</a>
                <a href="#article">Article</a>
                <a href="#portfolio">Portfolio</a>
                <a href="#about">About</a>
            </nav>
        </div>
    </header>

    <!-- Main Content -->
    <main id="home">

        <!-- Hero Section -->
        <section class="hero">
            <div class="hero-content">
                <p class="eyebrow">DESIGN • TECHNOLOGY • CREATIVITY</p>

                <h1>Building Beautiful and Responsive Websites</h1>

                <p class="hero-description">
                    Explore how thoughtful typography, flexible images,
                    and responsive layouts create better experiences
                    on every device.
                </p>

                <a href="#article" class="primary-button">
                    Read the Article
                </a>
            </div>

            <figure class="hero-image">
                <img
                    src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=1200&q=85"
                    alt="Laptop displaying a web development workspace"
                    width="1200"
                    height="800"
                >
                <figcaption>
                    A creative workspace for modern web development.
                </figcaption>
            </figure>
        </section>

        <!-- Article Section -->
        <article class="article-section" id="article">
            <div class="article-content">

                <p class="eyebrow">WEB DEVELOPMENT</p>

                <h2>Why Responsive Design Matters</h2>

                <p class="article-intro">
                    Responsive design allows a website to adapt to
                    different screen sizes, providing a comfortable
                    reading and browsing experience on phones,
                    tablets, and desktop computers.
                </p>

                <figure class="article-image">
                    <img
                        src="https://images.unsplash.com/photo-1516321318423-f06f85e504b3?auto=format&fit=crop&w=1200&q=85"
                        alt="Person working on a laptop at a desk"
                        width="1200"
                        height="800"
                        loading="lazy"
                    >
                    <figcaption>
                        A flexible layout helps content work across devices.
                    </figcaption>
                </figure>

                <h3>1. Responsive Typography</h3>

                <p>
                    Typography plays an important role in website
                    readability. Text that looks comfortable on a
                    desktop monitor may appear too large or too small
                    on a mobile screen. CSS units such as rem and em,
                    along with the clamp() function, help developers
                    create flexible font sizes.
                </p>

                <p>
                    The clamp() function accepts a minimum value,
                    a preferred responsive value, and a maximum value.
                    This allows headings to grow with the viewport
                    without becoming excessively large.
                </p>

                <h3>2. Responsive Images</h3>

                <p>
                    Images should fit within their containers without
                    exceeding the available screen width. The CSS
                    properties max-width: 100% and height: auto help
                    images scale proportionally while maintaining
                    their original aspect ratio.
                </p>

                <figure class="article-image">
                    <img
                        src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?auto=format&fit=crop&w=1200&q=85"
                        alt="Computer screen showing website analytics and charts"
                        width="1200"
                        height="800"
                        loading="lazy"
                    >
                    <figcaption>
                        Flexible images keep important visual information
                        inside the page layout.
                    </figcaption>
                </figure>

                <h3>3. Readable Content Width</h3>

                <p>
                    Long lines of text can make reading difficult.
                    A content container with a suitable maximum width
                    keeps paragraphs readable on large screens. On
                    smaller devices, the container should use the
                    available width with enough padding to keep text
                    away from the screen edges.
                </p>

                <h3>4. Consistent Spacing</h3>

                <p>
                    Appropriate spacing between headings, paragraphs,
                    and images makes content easier to understand.
                    Relative CSS units such as rem and em help maintain
                    consistent spacing throughout a webpage.
                </p>

                <blockquote>
                    Good responsive design makes content easy to read
                    and use, regardless of the device.
                </blockquote>

            </div>
        </article>

        <!-- Portfolio Section -->
        <section class="portfolio-section" id="portfolio">
            <div class="section-heading">
                <p class="eyebrow">MY WORK</p>
                <h2>Featured Projects</h2>
                <p>
                    A few examples of projects that demonstrate
                    creativity and web development skills.
                </p>
            </div>

            <div class="portfolio-grid">

                <article class="portfolio-card">
                    <img
                        src="https://images.unsplash.com/photo-1467232004584-a241de8bcf5d?auto=format&fit=crop&w=900&q=85"
                        alt="Website design displayed on a computer screen"
                        width="900"
                        height="600"
                        loading="lazy"
                    >

                    <div class="portfolio-card-content">
                        <h3>Website Design</h3>
                        <p>
                            A clean and modern design for a responsive
                            business website.
                        </p>
                    </div>
                </article>

                <article class="portfolio-card">
                    <img
                        src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?auto=format&fit=crop&w=900&q=85"
                        alt="Analytics dashboard with charts and data"
                        width="900"
                        height="600"
                        loading="lazy"
                    >

                    <div class="portfolio-card-content">
                        <h3>Analytics Dashboard</h3>
                        <p>
                            A dashboard concept for presenting useful
                            information in a clear layout.
                        </p>
                    </div>
                </article>

                <article class="portfolio-card">
                    <img
                        src="https://images.unsplash.com/photo-1519389950473-47ba0277781c?auto=format&fit=crop&w=900&q=85"
                        alt="Team collaborating on a technology project"
                        width="900"
                        height="600"
                        loading="lazy"
                    >

                    <div class="portfolio-card-content">
                        <h3>Team Project</h3>
                        <p>
                            A collaborative project focused on planning,
                            design, and development.
                        </p>
                    </div>
                </article>

            </div>
        </section>

        <!-- About Section -->
        <section class="about-section" id="about">
            <div class="about-content">
                <p class="eyebrow">ABOUT THIS PROJECT</p>

                <h2>Learning Responsive Web Design</h2>

                <p>
                    This webpage demonstrates how HTML and CSS can
                    create accessible, readable, and flexible content.
                    Responsive typography, suitable content widths,
                    and proportional images help provide a consistent
                    experience across different devices.
                </p>
            </div>
        </section>

    </main>

    <!-- Website Footer -->
    <footer class="site-footer">
        <p>&copy; 2026 CreativeSpace. Created for Assignment 9.2.</p>
        <p>Built with HTML and CSS.</p>
    </footer>

</body>
</html>
```

## 5. CSS Code (style.css)

```css
/* ======================================
   1. Global Styles
====================================== */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    font-size: 100%;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    font-size: 1rem;
    line-height: 1.7;
    color: #243047;
    background-color: #ffffff;
    min-width: 0;
}

img {
    display: block;
    max-width: 100%;
    height: auto;
}

a {
    color: inherit;
    text-decoration: none;
}

p,
h1,
h2,
h3,
figcaption {
    overflow-wrap: break-word;
}

figure {
    margin: 0;
}

:focus-visible {
    outline: 3px solid #7c5ce7;
    outline-offset: 4px;
}

/* ======================================
   2. Website Header
====================================== */

.site-header {
    width: 100%;
    background-color: #ffffff;
    border-bottom: 1px solid #e5eaf1;
}

.header-container {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 1rem;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 1rem;
}

.logo {
    font-size: 1.5rem;
    font-weight: 800;
    color: #6546d7;
    letter-spacing: -0.04em;
}

.navigation {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem 1rem;
}

.navigation a {
    color: #526078;
    font-size: 0.9rem;
}

.navigation a:hover {
    color: #6546d7;
}

/* ======================================
   3. Hero Section
====================================== */

.hero {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 3rem 1rem;
    display: grid;
    grid-template-columns: minmax(0, 1fr);
    gap: 2rem;
    align-items: center;
}

.hero-content {
    min-width: 0;
}

.eyebrow {
    color: #6546d7;
    font-size: 0.75rem;
    font-weight: 800;
    letter-spacing: 0.12em;
    line-height: 1.5;
    margin-bottom: 0.75rem;
}

.hero h1 {
    font-size: clamp(2rem, 7vw, 4rem);
    line-height: 1.12;
    letter-spacing: -0.045em;
    margin-bottom: 1.25rem;
    color: #172033;
}

.hero-description {
    max-width: 38rem;
    color: #64748b;
    font-size: clamp(1rem, 2.2vw, 1.15rem);
    line-height: 1.8;
    margin-bottom: 1.5rem;
}

.primary-button {
    display: inline-block;
    padding: 0.8rem 1.25rem;
    border-radius: 0.5rem;
    background-color: #6546d7;
    color: #ffffff;
    font-size: 0.95rem;
    font-weight: 700;
}

.primary-button:hover {
    background-color: #5033bc;
}

.hero-image {
    width: 100%;
    min-width: 0;
}

.hero-image img {
    width: 100%;
    height: auto;
    aspect-ratio: 3 / 2;
    object-fit: cover;
    border-radius: 1rem;
}

figcaption {
    color: #7b879a;
    font-size: 0.8rem;
    line-height: 1.5;
    margin-top: 0.6rem;
}

/* ======================================
   4. Article Section
====================================== */

.article-section {
    padding: 3rem 1rem;
    background-color: #f7f8fc;
}

.article-content {
    width: 100%;
    max-width: 760px;
    margin: 0 auto;
    min-width: 0;
}

.article-content h2 {
    color: #172033;
    font-size: clamp(1.8rem, 5vw, 2.75rem);
    line-height: 1.2;
    letter-spacing: -0.035em;
    margin-bottom: 1.25rem;
}

.article-intro {
    color: #526078;
    font-size: clamp(1.05rem, 2.5vw, 1.2rem);
    line-height: 1.85;
    margin-bottom: 1.75rem;
}

.article-content h3 {
    font-size: clamp(1.25rem, 3vw, 1.6rem);
    line-height: 1.3;
    margin-top: 2rem;
    margin-bottom: 0.75rem;
    color: #243047;
}

.article-content p:not(.eyebrow) {
    margin-bottom: 1.25rem;
}

.article-image {
    width: 100%;
    margin: 1.75rem 0;
}

.article-image img {
    width: 100%;
    height: auto;
    aspect-ratio: 16 / 9;
    object-fit: cover;
    border-radius: 0.75rem;
}

.article-content blockquote {
    margin: 2rem 0;
    padding: 1.25rem;
    border-left: 4px solid #6546d7;
    background-color: #eeeaff;
    color: #49349d;
    font-size: clamp(1.05rem, 2.5vw, 1.3rem);
    font-weight: 600;
    line-height: 1.7;
}

/* ======================================
   5. Portfolio Section
====================================== */

.portfolio-section {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 3rem 1rem;
}

.section-heading {
    max-width: 650px;
    margin-bottom: 2rem;
}

.section-heading h2 {
    font-size: clamp(1.8rem, 5vw, 2.6rem);
    line-height: 1.2;
    letter-spacing: -0.035em;
    margin-bottom: 0.75rem;
}

.section-heading > p:last-child {
    color: #64748b;
    font-size: 1rem;
}

.portfolio-grid {
    display: grid;
    grid-template-columns: minmax(0, 1fr);
    gap: 1.5rem;
}

.portfolio-card {
    min-width: 0;
    overflow: hidden;
    background-color: #ffffff;
    border: 1px solid #e5eaf1;
    border-radius: 0.9rem;
    box-shadow: 0 5px 20px rgba(30, 41, 59, 0.05);
}

.portfolio-card img {
    width: 100%;
    height: auto;
    aspect-ratio: 16 / 10;
    object-fit: cover;
}

.portfolio-card-content {
    padding: 1.25rem;
}

.portfolio-card h3 {
    font-size: 1.2rem;
    line-height: 1.4;
    margin-bottom: 0.5rem;
}

.portfolio-card p {
    color: #64748b;
    font-size: 0.95rem;
    line-height: 1.7;
}

/* ======================================
   6. About Section
====================================== */

.about-section {
    padding: 3rem 1rem;
    background-color: #f7f8fc;
}

.about-content {
    width: 100%;
    max-width: 760px;
    margin: 0 auto;
}

.about-content h2 {
    font-size: clamp(1.7rem, 5vw, 2.5rem);
    line-height: 1.25;
    margin-bottom: 1rem;
}

.about-content p:last-child {
    color: #526078;
    font-size: 1rem;
    line-height: 1.85;
}

/* ======================================
   7. Website Footer
====================================== */

.site-footer {
    display: flex;
    flex-direction: column;
    gap: 0.4rem;
    align-items: center;
    text-align: center;
    padding: 1.5rem 1rem;
    background-color: #172033;
    color: #d7deea;
    font-size: 0.85rem;
}

/* ======================================
   8. Tablet Breakpoint
   600px and above
====================================== */

@media (min-width: 600px) {

    .header-container {
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        padding: 1.25rem 1.5rem;
    }

    .hero {
        padding: 4rem 1.5rem;
        grid-template-columns: minmax(0, 1fr) minmax(0, 1fr);
        gap: 2rem;
    }

    .article-section {
        padding: 4rem 1.5rem;
    }

    .portfolio-section {
        padding: 4rem 1.5rem;
    }

    .portfolio-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .about-section {
        padding: 4rem 1.5rem;
    }

    .site-footer {
        flex-direction: row;
        justify-content: space-between;
        padding: 1.5rem;
    }
}

/* ======================================
   9. Desktop Breakpoint
   1024px and above
====================================== */

@media (min-width: 1024px) {

    .header-container {
        padding: 1.25rem 2rem;
    }

    .hero {
        padding: 5rem 2rem;
        gap: 4rem;
    }

    .article-section {
        padding: 5rem 2rem;
    }

    .portfolio-section {
        padding: 5rem 2rem;
    }

    .portfolio-grid {
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 2rem;
    }

    .about-section {
        padding: 5rem 2rem;
    }
}

/* ======================================
   10. Small Screen Adjustments
====================================== */

@media (max-width: 360px) {

    .header-container,
    .hero,
    .portfolio-section,
    .article-section,
    .about-section {
        padding-left: 0.75rem;
        padding-right: 0.75rem;
    }

    .navigation {
        gap: 0.5rem 0.75rem;
    }

    .hero h1 {
        font-size: clamp(1.8rem, 8vw, 2.2rem);
    }

    .article-content blockquote {
        padding: 1rem;
    }
}
```

## 6. Responsive Typography Explanation

Responsive typography ensures that text remains readable on small and large screens.

### CSS Units Used

**1. `rem`**

The `rem` unit is relative to the root element's font size.

```css
body {
    font-size: 1rem;
}

p {
    font-size: 1rem;
}
```

**2. `em`**

The `em` unit is relative to the font size of the relevant element or its parent, depending on the property.

```css
.card-content {
    padding: 1.5em;
}
```

**3. `clamp()`**

The `clamp()` function sets a minimum, preferred, and maximum value.

```css
h1 {
    font-size: clamp(2rem, 7vw, 4rem);
}
```

In this example, the heading scales with the viewport while staying between 2rem and 4rem.

## 7. Responsive Images Explanation

The following CSS properties prevent images from exceeding their containers:

```css
img {
    max-width: 100%;
    height: auto;
    display: block;
}
```

- `max-width: 100%` prevents an image from becoming wider than its container.
- `height: auto` preserves the image's natural aspect ratio.
- `display: block` removes unwanted inline-image spacing.
- `object-fit: cover` fills a fixed aspect-ratio frame when cropping is appropriate.

The `aspect-ratio` property keeps image frames consistent in the hero, article, and portfolio sections.

## 8. Content Width and Readability

The article uses a maximum width of 760px to keep paragraphs comfortable to read on larger screens.

```css
.article-content {
    width: 100%;
    max-width: 760px;
    margin: 0 auto;
}
```

The layout uses responsive padding and grid columns to prevent content from touching the edges of mobile screens.

## 9. How to Run the Project

1. Open Visual Studio Code.
2. Create a folder named `Assignment-9.2`.
3. Create `index.html` and `style.css`.
4. Paste the respective code into both files.
5. Save both files.
6. Install the Live Server extension if it is not already installed.
7. Right-click `index.html` and select **Open with Live Server**.
8. Check that the webpage and images load correctly.

**Note:** The images use online Unsplash URLs, so an internet connection is required to load them.

## 10. Testing on Mobile and Desktop

1. Open the webpage in Google Chrome.
2. Press `Ctrl + Shift + M` to open Chrome DevTools Device Mode.
3. Set the mobile viewport to approximately `375 × 812`.
4. Check that the headings, paragraphs, and images fit the screen.
5. Set a desktop viewport to approximately `1440 × 900`.
6. Check that the article remains readable and the portfolio cards appear in three columns.
7. Test an intermediate tablet width, such as `768px`.
8. Check for horizontal scrolling, stretched images, and overlapping text.
9. Confirm that the navigation links and page sections remain accessible.

## 11. Screenshot Submission

Capture screenshots from the actual running webpage.

**Mobile screenshot**
- Set the viewport to `375 × 812`.
- Ensure the page content is readable.
- Save the screenshot as `mobile.png`.

**Desktop screenshot**
- Set the viewport to `1440 × 900`.
- Ensure the desktop layout and portfolio cards are visible.
- Save the screenshot as `desktop.png`.

Place both screenshots in the `screenshots` folder.

## 12. Problems Prevented

1. Text overflowing beyond the viewport.
2. Images stretching or exceeding their containers.
3. Paragraphs becoming too wide on desktop screens.
4. Headings becoming too large on mobile screens.
5. Inconsistent spacing between content sections.
6. Portfolio cards becoming cramped on smaller devices.
7. Images and text overlapping at different screen sizes.

## 13. Result

A responsive article and portfolio webpage was created using HTML and CSS. Responsive typography, flexible images, maximum content widths, and media queries allow the page to adapt to mobile, tablet, and desktop screens.

## 14. Conclusion

This assignment demonstrates the importance of responsive typography and images in modern web development. By using `rem`, `em`, `clamp()`, `max-width`, `height: auto`, and media queries, websites can remain readable, visually consistent, and user-friendly across different devices.
