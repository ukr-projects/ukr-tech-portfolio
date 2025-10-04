# Code Explanation

This document provides a detailed explanation of the HTML and CSS code used to build my personal portfolio website.

## `index.html`

The `index.html` file is the main structure of the website, defining its content and layout.

### Document Structure

*   **`<!DOCTYPE html>`**: Declares the document as an HTML5 file.
*   **`<html lang="en">`**: The root element of the page, specifying the language as English.
*   **`<head>`**: Contains meta-information about the HTML document.
    *   **`<meta charset="UTF-8">`**: Specifies the character encoding for the document.
    *   **`<meta name="viewport" content="width=device-width, initial-scale=1.0">`**: Configures the viewport for responsive design.
    *   **`<title>UKR Portfolio</title>`**: Sets the title that appears in the browser tab.
    *   **`<link rel="stylesheet" type="text/css" href="styles.css">`**: Links the external stylesheet (`styles.css`) to apply styling.
*   **`<body>`**: Contains the visible page content.

### Navigation (`<nav>`)

The navigation bar is fixed at the top of the page and includes links to different sections of the portfolio.

*   **`<ul>`**: An unordered list containing navigation items.
*   **`<li><a href="#section-id">Link Text</a></li>`**: Each list item is a link that scrolls to a specific section on the page (e.g., `#home`, `#about`, `#projects`).

### Scroll Indicator (`<div class="scroll-indicator">`)

A visual cue at the bottom of the page to indicate that the user can scroll down.

### Sections (`<section>`)

The website is divided into several semantic sections, each with a unique `id` for navigation and styling.

#### Home Section (`<section id="home">`)

This is the introductory section of the portfolio.

*   **`<h1>Ujjwal Kumar Rai</h1>`**: My name as the main heading.
*   **`<img src="about.jpg" alt="Profile Picture" class="home-profile-image">`**: My profile picture.
*   **`<p class="hero-text">Full Stack Developer</p>`**: My primary role.
*   **`<p class="hero-text">A passionate Developer creating projects and learning.</p>`**: A brief description.
*   **`<a href="#projects" class="cta-button">View My Work</a>`**: A call-to-action button linking to the projects section.

#### About Me Section (`<section id="about">`)

This section provides personal details and a narrative about my interests.

*   **`<h2>About Me</h2>`**: Section heading.
*   **`<img src="about.jpg" alt="Profile Picture" class="about-image">`**: Another instance of my profile picture, styled differently.
*   **`<div class="about-text">`**: Contains paragraphs of text describing my background and philosophy.

#### My Domains Section (`<section id="domain">`)

This section showcases my areas of expertise.

*   **`<h2>My Domains</h2>`**: Section heading.
*   **`<div class="domain-container">`**: A container for multiple domain boxes.
*   **`<div class="domain-box">`**: Each box represents a domain.
    *   **`<div class="domain-icon">💻</div>`**: An emoji icon for the domain.
    *   **`<div class="domain-title">Web Development</div>`**: The title of the domain.
    *   **`<div class="domain-desc">Creating responsive and dynamic websites...</div>`**: A description of the domain.

#### My Projects Section (`<section id="projects">`)

This section lists my key projects.

*   **`<h2>My Projects</h2>`**: Section heading.
*   **`<div class="projects-container">`**: A container for multiple project cards.
*   **`<div class="project-card">`**: Each card represents a project.
    *   **`<a href="..." class="project-link-icon">🔗</a>`**: A link to the project's GitHub repository.
    *   **`<div class="project-title">⚔️ chatterbox-tts-colab</div>`**: The title of the project.
    *   **`<div class="project-desc">Transform any text into natural-sounding speech...</div>`**: A brief description of the project.

#### Contact Me Section (`<section id="contact">`)

This section provides ways to contact me.

*   **`<h2>Contact Me</h2>`**: Section heading.
*   **`<div class="contact-container">`**: A container for contact information.
*   **`<p class="contact-info">`**: Each paragraph contains a piece of contact information.
    *   **`📧 Email: <a href="mailto:ujjwalkrai@example.com" class="contact-link">ujjwalkrai@example.com</a>`**: My email address.
    *   **`🐱 GitHub: <a href="https://github.com/ukr-projects" class="contact-link" target="_blank">github.com</a>`**: Link to my GitHub profile.
    *   **`💼 LinkedIn: <a href="https://www.linkedin.com/in/u-k-r/" class="contact-link" target="_blank">linkedin.com</a>`**: Link to my LinkedIn profile.

## `styles.css`

The `styles.css` file defines the visual presentation of the portfolio website, including layout, colors, typography, and animations.

### Global Styles

*   **`*`**: Resets default margin and padding, and sets `box-sizing` to `border-box` for consistent layout.
*   **`body`**: Sets the default font family, background color (`#283845`), text color (`#f2f2f2`), and relative positioning.

### Navigation Bar (`nav`)

*   **`position: fixed; top: 0; width: 100%;`**: Makes the navigation bar stick to the top of the viewport.
*   **`background: rgba(40, 56, 69, 0.9);`**: Semi-transparent background.
*   **`border-bottom: 2px solid #41B3A3; box-shadow: ...;`**: Adds a bottom border and shadow for visual depth.
*   **`z-index: 1000;`**: Ensures the navigation bar stays on top of other content.
*   **`nav ul`**: Styles the list of navigation links, using `flexbox` for horizontal alignment and `gap` for spacing.
*   **`nav a`**: Styles the individual navigation links, including color, text decoration, font size, weight, and a `::before` pseudo-element for an animated underline effect on hover.
*   **`nav a:hover`**: Changes link color on hover.

### Sections (`section`)

*   **`min-height: 100vh;`**: Ensures each section takes at least the full viewport height.
*   **`padding`**: Provides spacing around the content.
*   **`h1`, `h2`**: Styles for main and sub-headings, including font size, color (`#41B3A3`), text alignment, and letter spacing. `h2::after` creates a decorative underline.

### Home Section Specific Styles (`#home`)

*   **`display: flex; flex-direction: column; justify-content: center; align-items: center;`**: Centers content vertically and horizontally.
*   **`.home-profile-image`**: Styles the profile picture with a circular shape, border, shadow, and a `pulse` animation.
*   **`.hero-text`**: Styles the introductory text with a distinct color (`#E8A87C`) and a `fadeIn` animation.
*   **`.cta-button`**: Styles the call-to-action button with background, text color, padding, border-radius, and hover effects.

### About Section Specific Styles (`#about`)

*   **`.about-image`**: Similar to the home profile image but with different border and shadow colors, and a `pulse` animation.
*   **`.about-text`**: Styles the text container with a maximum width, centered text, line height, padding, a semi-transparent background, border, and border-radius.

### Domain Section Specific Styles (`#domain`)

*   **`.domain-container`**: Uses CSS Grid to create a responsive grid of domain boxes.
*   **`.domain-box`**: Styles individual domain boxes with background, border, border-radius, padding, text alignment, and hover effects (`transform`, `box-shadow`, `border-color`).
*   **`.domain-icon`, `.domain-title`, `.domain-desc`**: Styles for the icon, title, and description within each domain box.

### Projects Section Specific Styles (`#projects`)

*   **`.projects-container`**: Uses CSS Grid for a responsive layout of project cards.
*   **`.project-card`**: Styles individual project cards with background, border, border-radius, padding, and hover effects (`transform`, `box-shadow`, `border-color`).
*   **`.project-link-icon`**: Styles the link icon for each project, positioning it at the top-right corner.
*   **`.project-title`, `.project-desc`**: Styles for the project title and description.

### Contact Section Specific Styles (`#contact`)

*   **`.contact-container`**: Styles the container for contact information with a maximum width, padding, background, border, and border-radius.
*   **`.contact-info`**: Styles individual contact information paragraphs.
*   **`.contact-link`**: Styles the contact links with color, text decoration, font weight, and hover effects.

### Animations

*   **`@keyframes fadeIn`**: Animates the opacity for a fade-in effect.
*   **`@keyframes pulse`**: Animates the scale and box-shadow for a pulsing effect on images.
*   **`@keyframes bounce`**: Animates the vertical position of the scroll indicator.
*   **`@keyframes scrollDot`**: Animates the opacity and vertical position of the dot within the scroll indicator.

### Responsive Design (`@media` queries)

Media queries are used to adjust the layout and styling for different screen sizes, ensuring the website is responsive on mobile devices, tablets, and desktops.

*   **`@media (max-width: 768px)`**: Styles applied for screens up to 768px wide (e.g., tablets).
*   **`@media (max-width: 480px)`**: Styles applied for screens up to 480px wide (e.g., mobile phones).
