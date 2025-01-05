Designing a Responsive Layout
a. Create a webpage with the following sections:

Header (including a logo and navigation links). Main content area (with two columns: one for text content and the other for an image). Footer (with links to social media and a copyright notice). b. Use Flexbox to style the navigation menu in the header. c. Use CSS Grid to structure the main content area.

Creating Media Queries for Responsiveness
a. Implement media queries to ensure the webpage looks good on the following screen sizes:

Small screens (up to 600px): Stack all sections vertically. Medium screens (601px to 1024px): Keep the header and footer horizontal, but stack the main content columns. Large screens (above 1024px): Display the layout as designed with Flexbox and Grid.

Bonus
Add animations or transitions when resizing the screen.
# Week-3-day-4-assignment-
Assignment for week 3 day 4 

HTML and CSS Code Implementation:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Webpage</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Header Section -->
    <header class="header">
        <div class="logo">
            <img src="logo.png" alt="Logo">
        </div>
        <nav class="navigation">
            <ul class="nav-links">
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Main Content Section -->
    <main class="main-content">
        <div class="text-content">
            <h1>Welcome to Our Website</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam scelerisque tortor ut felis cursus, at vulputate massa gravida.</p>
        </div>
        <div class="image-content">
            <img src="image.jpg" alt="Description of Image">
        </div>
    </main>

    <!-- Footer Section -->
    <footer class="footer">
        <p>&copy; 2025 Your Company. All rights reserved.</p>
        <ul class="social-links">
            <li><a href="#">Facebook</a></li>
            <li><a href="#">Twitter</a></li>
            <li><a href="#">LinkedIn</a></li>
        </ul>
    </footer>

</body>
</html>


CSS (style.css) Code:

/* Reset and Base Styles */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

header {
    background-color: #333;
    color: white;
    padding: 1rem;
}

.logo img {
    width: 100px;
}

.navigation {
    display: flex;
    justify-content: space-around;
}

.nav-links {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
}

.nav-links li {
    margin-right: 1rem;
}

.nav-links a {
    color: white;
    text-decoration: none;
}

.nav-links a:hover {
    text-decoration: underline;
}

.main-content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
    padding: 2rem;
    background-color: #f9f9f9;
}

.text-content {
    padding: 1rem;
}

.image-content img {
    width: 100%;
    height: auto;
}

.footer {
    background-color: #333;
    color: white;
    padding: 1rem;
    text-align: center;
}

.social-links {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
}

.social-links li {
    margin-right: 1rem;
}

.social-links a {
    color: white;
    text-decoration: none;
}

.social-links a:hover {
    text-decoration: underline;
}

/* Media Queries */
@media (max-width: 600px) {
    .main-content {
        grid-template-columns: 1fr;
    }

    .nav-links {
        flex-direction: column;
        text-align: center;
    }

    .nav-links li {
        margin-bottom: 0.5rem;
    }
}

@media (min-width: 601px) and (max-width: 1024px) {
    .main-content {
        grid-template-columns: 1fr;
    }
}

@media (min-width: 1025px) {
    .main-content {
        grid-template-columns: 1fr 1fr;
    }

    .nav-links {
        flex-direction: row;
        justify-content: space-around;
    }
}

