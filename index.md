Assignment 3.4 — Semantic HTML & Accessibility
1. Aim
To convert a webpage built with generic <div> elements into semantic HTML by using appropriate structural elements, improving accessibility, organizing headings correctly, and adding meaningful alternative text to images.

2. Before: Div-Based HTML
Save this example as before.html. It demonstrates a webpage that relies on generic <div> elements instead of semantic structure.


<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
</head>
<body>
    <div>
        <h1>My Learning Website</h1>
        <div>
            <a href="index.html">Home</a>
            <a href="about.html">About</a>
            <a href="contact.html">Contact</a>
        </div>
    </div>

    <div>
        <div>
            <h2>Welcome</h2>
            <p>Welcome to my learning website.</p>
            <img src="images/learning.jpg">
        </div>

        <div>
            <h2>Learning HTML</h2>
            <p>HTML is used to structure webpages.</p>
        </div>

        <div>
            <h3>Quick Tip</h3>
            <p>Practice HTML regularly to improve your skills.</p>
        </div>
    </div>

    <div>
        <p>Copyright 2026 My Learning Website</p>
    </div>
</body>
</html>
Problems in the original code
Generic <div> elements do not clearly identify the purpose of each page region.

Navigation links are not grouped in a <nav> element.

The main content is not enclosed in <main>.

The image has no alt attribute.

The page uses an inconsistent heading hierarchy.

The document is missing the lang attribute and responsive viewport metadata.

3. After: Semantic HTML
Save the corrected code as index.html. This version uses semantic elements to make the webpage structure clearer and more accessible.


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Learning Website</title>
</head>
<body>
    <header>
        <h1>My Learning Website</h1>

        <nav aria-label="Main navigation">
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section aria-labelledby="welcome-heading">
            <h2 id="welcome-heading">Welcome</h2>
            <p>Welcome to my learning website.</p>

            <img
                src="images/learning.jpg"
                alt="A student learning HTML on a computer"
                width="400"
                height="250"
            >
        </section>

        <section aria-labelledby="html-heading">
            <h2 id="html-heading">Learning HTML</h2>

            <article>
                <h3>Introduction to HTML</h3>
                <p>
                    HTML is used to structure webpages. It provides
                    elements for headings, paragraphs, images,
                    links, and other content.
                </p>
            </article>
        </section>

        <aside aria-labelledby="tip-heading">
            <h2 id="tip-heading">Quick Tip</h2>
            <p>
                Practice HTML regularly to improve your skills.
            </p>
        </aside>
    </main>

    <footer>
        <p>&copy; 2026 My Learning Website</p>
    </footer>
</body>
</html>
Important: Place an actual image named learning.jpg inside the images folder. The alternative text should describe the image you actually use.

4. Semantic HTML Elements Explained
Element

Purpose

<header>

Contains the website heading and introductory content.

<nav>

Groups the main navigation links.

<main>

Contains the primary content of the webpage.

<section>

Groups related content under a heading.

<article>

Represents a self-contained piece of content.

<aside>

Contains supplementary content, such as a tip.

<footer>

Contains footer information, such as copyright details.

5. Accessibility Improvements
Meaningful image text: The alt attribute describes the image to screen-reader users and provides text when the image cannot load.

Correct heading hierarchy: The page uses an <h1> for the main website title, <h2> for major sections, and <h3> for a subsection.

Understandable navigation: The links are grouped in a <nav> element and displayed as a list.

Landmark elements: Semantic HTML helps assistive technologies identify the header, navigation, main content, and footer.

Language declaration: lang="en" identifies the page language as English.

Responsive metadata: The viewport setting helps the page display correctly on mobile devices.

6. Expected Output
My Learning Website
Home

About

Contact

Welcome
Welcome to my learning website.

ChatGPT jako programátor: Jak vytvořit web s umělou inteligencí? | Ábíčko.cz
Learning HTML
Introduction to HTML
HTML is used to structure webpages. It provides elements for headings, paragraphs, images, links, and other content.

Quick Tip
Practice HTML regularly to improve your skills.
© 2026 My Learning Website

Illustrative preview of the semantic webpage using default browser styling.
7. Before-and-After Comparison
Before

After

Generic <div> elements

Semantic structural elements

Navigation links grouped in a <div>

Links grouped in <nav>

Main content not identified

Content placed inside <main>

Image without alternative text

Image has meaningful alt text

Inconsistent headings

Organized heading hierarchy

Limited accessibility information

Language and navigation landmarks provided

8. How to Test the Webpage
Save the original code as before.html.

Save the corrected code as index.html.

Create an images folder and add learning.jpg.

Open both HTML files in a browser.

Compare the structure and appearance of both webpages.

Use browser DevTools by pressing F12 and inspecting the Elements panel.

Test navigation links and verify that the image loads correctly.

Optionally, run index.html through the W3C HTML Validator  to check its markup.

Note: The about.html and contact.html pages must exist for those navigation links to lead to working pages. You can create those files or update the links to pages that already exist.

9. Screenshots for Submission
Capture these screenshots from your own browser:

Before screenshot: Open before.html and capture the original div-based webpage.

After screenshot: Open index.html and capture the corrected semantic webpage.

Ensure the page title, navigation, content, image, and footer are visible where possible.

10. Result
The div-based webpage was converted into a semantic HTML webpage using <header>, <nav>, <main>, <section>, <article>, <aside>, and <footer>. The heading hierarchy and image alternative text were improved to support accessibility and make the webpage structure easier to understand.