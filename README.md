# Blog Site
## Description

This is a simple blog site that showcases a clean and responsive layout for a personal or professional blog wich is created using Tailwind and Javascript. The project includes features like a theme toggle for light and dark modes, a hamburger menu for mobile navigation, and a "back to top" button for better user experience. This project is ideal for practice Tailwind and JavaScript.

## Features

- **Responsive Design**: Adapts to various screen sizes with a mobile-friendly layout.
- **Dark Mode**: Toggle between light and dark themes.
- **Back to Top Button**: Smoothly scrolls back to the top of the page.
- **Hamburger Menu**: Collapsible menu for mobile and tablet devices.
- **Multi-Page Navigation**: Links to different blog posts and the home page.

## Prerequisites

- A modern web browser (e.g., Chrome, Firefox, Edge).
- Basic understanding of HTML, CSS, Tailwind and JavaScript.

## JavaScript Code Highlights

- **Theme Toggle**:
    ```javascript
    const themeToggleBtn = document.getElementById('theme-toggle');
    themeToggleBtn.addEventListener('click', toggleTheme);
    function toggleTheme() {
        document.documentElement.classList.toggle('dark');
        const isDarkTheme = document.documentElement.classList.contains('dark');
        localStorage.setItem('color-theme', isDarkTheme ? 'dark' : 'light');
        themeToggleText.textContent = isDarkTheme ? '☼' : '☾';
    }
    ```

- **Hamburger Menu**:
    ```javascript
    const hamburgerButton = document.querySelector(".hamburger-button");
    const menuLinks = document.querySelector(".menu-links");
    hamburgerButton.addEventListener("click", () => {
        menuLinks.classList.toggle("hidden");
    });
    ```

- **Back to Top Button**:
    ```javascript
    document.addEventListener("DOMContentLoaded", function () {
        const backToTopButton = document.getElementById("back-to-top-button");
        window.addEventListener("scroll", function () {
            if (window.scrollY > 300) {
                backToTopButton.classList.remove("hidden");
            } else {
                backToTopButton.classList.add("hidden");
            }
        });
        backToTopButton.addEventListener("click", function () {
            window.scrollTo({ top: 0, behavior: "smooth" });
        });
    });

