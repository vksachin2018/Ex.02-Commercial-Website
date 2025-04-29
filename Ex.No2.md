# Ex02 Commercial Website
## Date:11/03/2025

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
```
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Tutorial Center</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            background: linear-gradient(to bottom, #f0f8ff, #e6e6fa);
            color: #333;
        }

        header {
            background: linear-gradient(to right, #007bff, #00c6ff);
            color: #fff;
            padding: 1rem 0;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .container {
            width: 90%;
            margin: 0 auto;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .brand {
            display: flex;
            align-items: center;
        }

        .brand img {
            width: 50px;
            height: 50px;
            margin-right: 10px;
            border-radius: 50%;
            border: 2px solid #fff;
        }

        .brand h1 {
            font-size: 1.8rem;
            font-weight: bold;
        }

        nav ul {
            list-style: none;
            display: flex;
        }

        nav ul li {
            margin: 0 15px;
        }

        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s ease;
        }

        nav ul li a:hover {
            color: #ffeb3b;
        }

        .hero {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 70vh;
            background: url('tutorial-center-hero.jpg') no-repeat center center/cover;
            color: #fff;
            text-align: center;
            position: relative;
        }

        .hero::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            z-index: 1;
        }

        .hero h1 {
            font-size: 3.5rem;
            text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.7);
            z-index: 2;
            position: relative;
        }

        .features {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin: 2rem 0;
        }

        .feature {
            flex: 1 1 calc(33.333% - 20px);
            max-width: 300px;
            margin: 0 auto;
            padding: 1.5rem;
            background: #fff;
            text-align: center;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .feature:hover {
            transform: translateY(-10px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
        }

        .feature h3 {
            margin-bottom: 1rem;
            color: #007bff;
        }

        .feature p {
            color: #555;
        }

        .feature a {
            display: inline-block;
            margin-top: 1rem;
            padding: 0.5rem 1rem;
            background: #007bff;
            color: #fff;
            text-decoration: none;
            border-radius: 5px;
            transition: background 0.3s ease;
        }

        .feature a:hover {
            background: #0056b3;
        }

        .about, .contact {
            text-align: center;
            padding: 2rem 0;
            background: #f9f9f9;
            margin: 2rem 0;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .about h2, .contact h2 {
            color: #007bff;
            margin-bottom: 1rem;
        }

        .about p, .contact p {
            color: #555;
            max-width: 800px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        footer {
            background: #007bff;
            color: #fff;
            text-align: center;
            padding: 1rem 0;
            margin-top: 2rem;
            box-shadow: 0 -4px 6px rgba(0, 0, 0, 0.1);
        }

        footer p {
            font-size: 0.9rem;
        }

        footer p a {
            color: #ffeb3b;
            text-decoration: none;
            font-weight: bold;
        }

        footer p a:hover {
            text-decoration: underline;
        }

        @media (max-width: 768px) {
            .feature {
                flex: 1 1 calc(50% - 20px);
            }
        }

        @media (max-width: 480px) {
            .feature {
                flex: 1 1 100%;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <nav>
                <div class="brand">
                    <img src="download.png" alt="Tutorial Center Logo">
                    <h1>Tutorial Center</h1>
                </div>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#courses">Courses</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section id="home" class="hero">
        <h1>Learn, Grow, Succeed</h1>
    </section>

    <section id="courses" class="container courses">
        <h2>Our Courses</h2>
        <p>Explore a variety of courses designed to help you achieve your goals. From programming to business, we have something for everyone.</p>
        <div class="features">
            <div class="feature">
                <h3>Web Development</h3>
                <p>Learn how to build websites using HTML, CSS, and JavaScript. Our courses cover everything from the basics to advanced topics.</p>
                <a href="#">Learn More</a>
            </div>
            <div class="feature">
                <h3>Python Programming</h3>
                <p>Master the Python programming language with our comprehensive courses. Start from scratch or take your skills to the next level.
                </p>
                <a href="#">Learn More</a>
            </div>
            <div class="feature">
                <h3>UI/UX</h3>
                <p> master the art of designing user-friendly interfaces. Our courses cover the principles of UI/UX design and best practices.
                     </p>
                <a href="#">Learn More</a>
            </div>
        </div>
    </section>

    <section id="about" class="container about">
        <h2>About Us</h2>
        <p>We are a leading tutorial center dedicated to providing high-quality education to students of all ages. Our mission is to empower learners with the skills they need to succeed.</p>
    </section>

    <section id="contact" class="container contact">
        <h2>Contact Us</h2>
        <p>Have questions? Reach out to us at <a href="mailto:info@tutorialcenter.com">info@tutorialcenter.com</a> or call us at +91 2345678910.</p>
    </section>

    <footer>
        <p>&copy; 2025 <a href="#">Tutorial Center</a>. All rights reserved.</p>
    </footer>
</body>
</html>
```

## OUTPUT
![Screenshot 2025-03-16 165820](https://github.com/user-attachments/assets/f070b389-2aa2-44ac-b9fd-817528716775)
![Screenshot 2025-03-16 165831](https://github.com/user-attachments/assets/eb8df828-83aa-4be6-a8fd-1132f5954745)
![Screenshot 2025-03-16 165840](https://github.com/user-attachments/assets/f70bdbfd-1a4e-44b3-bf7b-bc1b24b1ca35)



## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
