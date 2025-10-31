# CodeAlpha_Task
My Internship Tasks.
📚 Unified Project Documentation: Three Core Tasks

This document provides a consolidated technical overview of three single-file web applications: the Frontend Developer Portfolio, a Dynamic Image Gallery, and the Cyberpunk Calculator.

      💻 Task 1: Shivangi | Frontend Developer Portfolio

This is a single-page application (SPA) portfolio designed to be a concise and visually striking showcase of core competencies and featured projects, built using a single HTML file with Tailwind CSS and custom JavaScript.

🛠️ Technology Stack

Category

Technology

Usage / Purpose

Markup

HTML5

Provides the semantic structure of the single-page layout.

Styling

Tailwind CSS (via CDN)

Utility-first framework for rapid, responsive styling.

Dynamics

JavaScript (Vanilla ES6+)

Handles interactive features like the typing effect, scroll animations, and smooth navigation.

Icons

Font Awesome

Provides scalable vector icons for skills, projects, and contact links.

Font

Inter

Primary sans-serif typeface for clean readability.

✨ Dynamic Features and Interactivity

Feature

Location

Mechanism

Dynamic Typing Effect

Hero Section (#home)

Looping animation (typeWriter and deleteText functions) dynamically displays specializations (e.g., "React Specialist").

Scroll-Triggered Fade-In

All Major Sections

Uses the Intersection Observer API to add the is-visible class to elements upon intersection, triggering a smooth fade-in and slight slide-up.

Animated Skill Bars

Skills Section (#skills)

The skillObserver triggers a smooth 1.5-second CSS transition to animate .skill-fill-bar elements based on the percentage defined in their data-fill attribute.

Navigation & Layout

Navigation Bar

Sticky navbar (sticky top-0) with a translucent, blurred background (backdrop-blur-sm).

      🖼️ Task 2: Dynamic Responsive Image Gallery

This project is a modern, single-file image gallery application built for high responsiveness and enhanced user experience through interactive features.

🎨 Design and Layout

Aesthetics: Clean, dark/light-toggle theme with a focus on image clarity and generous spacing.

Layout: Utilizes a Tailwind CSS Grid system to create an adaptive and responsive layout for images, ensuring the display adjusts gracefully from mobile to large desktop screens.

Image Handling: Placeholder images are used, and images are wrapped in card-style components with subtle hover effects.

⚙️ JavaScript Functionality

Feature

Description

Mechanism

Category Filtering

Interactive buttons/tabs

Vanilla JavaScript dynamically changes the visibility of image elements based on their data-category attribute. Allows users to quickly view photos by specific tags (e.g., "Nature," "City," "Abstract").

Lightbox/Modal View

Image Click

Clicking an image triggers a modal (#lightbox-modal) which displays the full-sized image and descriptive caption, centering the focus on the media.

Touch/Keyboard Navigation

Modal Controls

Supports swiping (on touch devices) or arrow key presses (on desktop) to navigate between images while in the modal view.

      👾 Task 3: Dynamic Cyberpunk Calculator

This application is a functional JavaScript calculator engine designed with a unique, high-contrast, neon-themed user interface, built using Tailwind CSS and custom CSS animations.

🎨 Aesthetics and Styling

The design strictly adheres to a Cyberpunk/Sci-Fi aesthetic using a custom neon color palette and retro-digital effects.

1. Tailwind Configuration (Cyberpunk Palette)

Tailwind Class

Hex Value

Description

cp-main

#111827

Deep, dark application background.

cp-op

#00FFFF

Neon Cyan for standard arithmetic operators.

cp-equal

#FF00FF

Neon Pink/Magenta for the Equals button and its glow.

cp-clear

#00FF00

Neon Green for the Clear/Delete buttons and the main display text/glow.

2. Custom CSS Effects

Pulsing Border: The main calculator body (.calculator-body) features a pulse-border keyframe animation that alternates between Neon Cyan and Neon Pink shadows, giving the device a "powered up" effect.

CRT Display Effect: The input field uses box-shadow and text-shadow in Neon Green (#00FF00) to simulate a classic CRT monitor glow.

3D Button Press: Buttons utilize a strong box shadow that is removed and translated on click (active:shadow-none active:translate-x-1 active:translate-y-1), creating a tactile, sunken 3D press effect.

⚙️ JavaScript Functionality

Function

Description

Logic Highlights

appendInput(value)

Handles input for numbers, operators, and decimals.

Includes logic to prevent consecutive operators and ensures proper decimal handling within a single number segment.

calculateResult()

Evaluates the expression displayed in currentInput.

Symbol Conversion: Converts display symbols (×, ÷, −) to JavaScript operators (*, /, -). Evaluation: Uses new Function('return ' + expression)() for safe calculation. Includes Error Handling for invalid expressions.

Keyboard Support

Global keydown listener.

Maps physical keys (0-9, +, -, *, /, Enter, Backspace, Delete) to the corresponding calculator functions.
