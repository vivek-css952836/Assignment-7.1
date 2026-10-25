Step 1: HTML Structure (index.html)
This file sets up the semantic <header> containing a logo, navigation links, and a call-to-action button.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Navigation Bar</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Step 1: Header containing a logo, links, and action button -->
    <header class="navbar-header">
        <div class="logo">BrandLogo</div>
        
        <nav class="nav-links">
            <a href="#home">Home</a>
            <a href="#features">Features</a>
            <a href="#pricing">Pricing</a>
            <a href="#about">About</a>
        </nav>

        <div class="nav-action">
            <a href="#get-started" class="btn-primary">Get Started</a>
        </div>
    </header>

</body>
</html>

Steps 2–6: CSS Code (style.css)
This stylesheet applies Flexbox properties (display: flex, justify-content, align-items) and includes a media query for screen responsiveness.

/* Reset and Base Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    background-color: #f8f9fa;
}

/* Step 2 & 3 & 4: Flexbox Container Layout */
.navbar-header {
    display: flex;                  /* Step 2: Apply display: flex */
    justify-content: space-between; /* Step 3: Spread items across the container */
    align-items: center;            /* Step 4: Vertically center items */
    padding: 1rem 5%;
    background-color: #ffffff;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

/* Logo Styling */
.logo {
    font-size: 1.5rem;
    font-weight: bold;
    color: #333333;
}

/* Navigation Links Container */
.nav-links {
    display: flex;
    gap: 2rem; /* Spacing between links */
}

/* Step 5: Style the navigation links */
.nav-links a {
    text-decoration: none;
    color: #555555;
    font-weight: 500;
    transition: color 0.3s ease;
}

.nav-links a:hover {
    color: #007bff;
}

/* Step 5: Style the button */
.btn-primary {
    display: inline-block;
    padding: 0.5rem 1.25rem;
    background-color: #007bff;
    color: #ffffff;
    text-decoration: none;
    border-radius: 4px;
    font-weight: 500;
    transition: background-color 0.3s ease;
}

.btn-primary:hover {
    background-color: #0056b3;
}

/* Step 6: Responsive Layout (Inspecting width changes) */
@media (max-width: 768px) {
    .navbar-header {
        flex-direction: column; /* Stack header items vertically on small screens */
        align-items: flex-start;
        gap: 1rem;
    }

    .nav-links {
        flex-direction: column; /* Stack navigation links */
        gap: 0.75rem;
        width: 100%;
    }

    .nav-action {
        width: 100%;
    }

    .btn-primary {
        display: block;
        text-align: center;
    }
}