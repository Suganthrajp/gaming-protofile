# gaming-protofile
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gaming Professional Portfolio</title>
    <style>
        /* CSS Styles */
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #1e1e1e;
            color: white;
        }
        header {
            background-color: #000;
            padding: 20px;
            text-align: center;
        }
        header h1 {
            margin: 0;
            font-size: 2.5em;
        }
        nav {
            margin: 20px 0;
        }
        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-size: 18px;
        }
        h2 {
            text-align: center;
            color: #e91e63;
        }
        main {
            padding: 20px;
        }
        .profile-section, .achievements-section, .contact-section {
            margin: 50px 0;
        }
        .profile-info {
            display: flex;
            justify-content: space-around;
            align-items: center;
        }
        .profile-info img {
            border-radius: 50%;
            width: 200px;
        }
        .achievements-list {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }
        .achievement-item {
            background-color: #333;
            padding: 20px;
            border-radius: 10px;
            width: 300px;
            text-align: center;
        }
        .achievement-item h3 {
            margin: 0;
            color: #e91e63;
        }
        form {
            max-width: 600px;
            margin: 0 auto;
            text-align: left;
        }
        form label, form input, form textarea {
            display: block;
            width: 100%;
            margin-bottom: 10px;
        }
        form input, form textarea {
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        form button {
            background-color: #e91e63;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
        }
        form button:hover {
            background-color: #ff4081;
        }
        footer {
            background-color: #000;
            color: white;
            text-align: center;
            padding: 15px;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>

    <!-- Header and Navigation -->
    <header>
        <h1>Gaming Professional Portfolio</h1>
        <nav>
            <a href="#" onclick="showSection('profile')">Profile</a>
            <a href="#" onclick="showSection('achievements')">Achievements</a>
            <a href="#" onclick="showSection('contact')">Contact</a>
        </nav>
    </header>

    <!-- Main Content -->
    <main id="content">
        <!-- Profile Section -->
        <section id="profile" class="profile-section">
            <h2>About Me</h2>
            <div class="profile-info">
                <img src="https://via.placeholder.com/200" alt="Profile Image">
                <div>
                    <p>Hello! I am a professional gamer with over 10 years of experience in competitive gaming. I specialize in first-person shooters and have participated in international tournaments. My journey started with small local competitions, and over the years, I have become a seasoned expert in various gaming genres.</p>
                    <p>From strategy games to fast-paced shooters, gaming has been my passion. Here, I showcase my journey, achievements, and how to get in touch with me.</p>
                </div>
            </div>
        </section>

        <!-- Achievements Section -->
        <section id="achievements" class="achievements-section" style="display:none;">
            <h2>Achievements</h2>
            <div class="achievements-list">
                <div class="achievement-item">
                    <h3>1st Place - Global FPS Tournament</h3>
                    <p>Won first place in the 2022 Global FPS Tournament with a team of skilled players. Over 100 teams participated in the competition.</p>
                </div>
                <div class="achievement-item">
                    <h3>2nd Place - Strategy Masters 2023</h3>
                    <p>A runner-up position in the 2023 Strategy Masters Championship, showcasing superior team coordination and critical thinking.</p>
                </div>
                <div class="achievement-item">
                    <h3>MVP Award - XYZ Gaming League</h3>
                    <p>Awarded Most Valuable Player in the XYZ Gaming League for outstanding performance in 10 consecutive matches.</p>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="contact-section" style="display:none;">
            <h2>Contact Me</h2>
            <form id="contact-form">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>

                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>

                <label for="message">Message:</label>
                <textarea id="message" name="message" rows="5" required></textarea>

                <button type="submit">Submit</button>
            </form>
        </section>
    </main>

    <!-- Footer -->
    <footer>
        <p>© 2024 Gaming Professional. All Rights Reserved.</p>
    </footer>

    <script>
        // JavaScript: Section Navigation
        function showSection(sectionId) {
            const sections = document.querySelectorAll('main > section');
            sections.forEach(section => {
                section.style.display = 'none';
            });
            document.getElementById(sectionId).style.display = 'block';
        }

        // Show Profile by default on page load
        document.addEventListener('DOMContentLoaded', function() {
            showSection('profile');
        });

        // Contact Form Submission Handling
        document.getElementById('contact-form').addEventListener('submit', function(event) {
            event.preventDefault();
            alert('Thank you for reaching out! I will get back to you soon.');
            event.target.reset();
        });
    </script>
</body>
</html>
