<!DOCTYPE html>
<!-- 
  Advanced HTML5 Elements and Forms
  Demonstrating images, lists, tables, forms, and multimedia
-->
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Advanced HTML5 Elements</title>
    <style>
        /* Basic styling for better presentation */
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: left;
        }
        th {
            background-color: #f2f2f2;
        }
        form {
            background-color: #f9f9f9;
            padding: 20px;
            border-radius: 5px;
            margin-top: 20px;
        }
        .form-group {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        img {
            max-width: 100%;
            height: auto;
            display: block;
            margin: 20px 0;
        }
    </style>
</head>
<body>
    <header>
        <h1>Advanced HTML5 Elements Demonstration</h1>
    </header>
    <main>
        <section>
            <h2>Ordered List with Roman Numerals</h2>
            <ol type="I">
                <li>Introduction to HTML5</li>
                <li>Semantic Elements</li>
                <li>Forms and Input Types</li>
                <li>Multimedia Elements</li>
                <li>Accessibility Features</li>
            </ol>
        </section>
        <section>
            <h2>External Image from Pexels.com</h2>
            <!-- Image from Pexels (free stock photo) -->
            <img src="https://images.pexels.com/photos/574071/pexels-photo-574071.jpeg" 
                 alt="Laptop with code on screen" 
                 title="Programming workspace">
            <p>This image demonstrates proper use of the &lt;img&gt; tag with external source and alt text for accessibility.</p>
        </section>
        <section>
            <h2>Contacts Table</h2>
            <table>
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Address</th>
                        <th>Mobile</th>
                        <th>Email</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>John Smith</td>
                        <td>123 Main St, Anytown</td>
                        <td>555-0101</td>
                        <td>john.smith@example.com</td>
                    </tr>
                    <tr>
                        <td>Sarah Johnson</td>
                        <td>456 Oak Ave, Somewhere</td>
                        <td>555-0102</td>
                        <td>sarah.j@example.com</td>
                    </tr>
                    <tr>
                        <td>Michael Brown</td>
                        <td>789 Pine Rd, Nowhere</td>
                        <td>555-0103</td>
                        <td>m.brown@example.com</td>
                    </tr>
                    <tr>
                        <td>Emily Davis</td>
                        <td>321 Elm Blvd, Anywhere</td>
                        <td>555-0104</td>
                        <td>emily.d@example.com</td>
                    </tr>
                    <tr>
                        <td>Robert Wilson</td>
                        <td>654 Maple Ln, Everywhere</td>
                        <td>555-0105</td>
                        <td>rob.wilson@example.com</td>
                    </tr>
                </tbody>
            </table>
        </section>
        <section>
            <h2>Registration Form</h2>
            <form id="registrationForm" novalidate>
                <div class="form-group">
                    <label for="fullName">Full Name:</label>
                    <input type="text" id="fullName" name="fullName" 
                           placeholder="Enter your full name" required
                           minlength="3" maxlength="50">
                    <small class="error-message">Please enter your full name (3-50 characters)</small>
                </div>
            <div class="form-group">
                    <label for="email">Email Address:</label>
                    <input type="email" id="email" name="email" 
                           placeholder="your.email@example.com" required>
                    <small class="error-message">Please enter a valid email address</small>
                </div>
                <div class="form-group">
                    <label for="password">Password:</label>
                    <input type="password" id="password" name="password" 
                           placeholder="Create a password" required
                           minlength="8" pattern="^(?=.*[A-Za-z])(?=.*\d).{8,}$">
                    <small class="error-message">Password must be at least 8 characters with at least one letter and one number</small>
                </div>
                <div class="form-group">
                    <label for="birthDate">Date of Birth:</label>
                    <input type="date" id="birthDate" name="birthDate" required>
                    <small class="error-message">Please select your date of birth</small>
                </div>
                <div class="form-group">
                    <label>Gender:</label>
                    <div>
                        <input type="radio" id="male" name="gender" value="male" required>
                        <label for="male">Male</label>
                        <input type="radio" id="female" name="gender" value="female">
                        <label for="female">Female</label>
                        <input type="radio" id="other" name="gender" value="other">
                        <label for="other">Other</label>
                        <input type="radio" id="preferNot" name="gender" value="preferNot">
                        <label for="preferNot">Prefer not to say</label>
                    </div>
                    <small class="error-message">Please select your gender</small>
                </div>
                <div class="form-group">
                    <label for="country">Country:</label>
                    <select id="country" name="country" required>
                        <option value="" disabled selected>Select your country</option>
                        <option value="us">United States</option>
                        <option value="ca">Canada</option>
                        <option value="uk">United Kingdom</option>
                        <option value="au">Australia</option>
                        <option value="other">Other</option>
                    </select>
                    <small class="error-message">Please select your country</small>
                </div>
                <div class="form-group">
                    <label>Interests:</label>
                    <div>
                        <input type="checkbox" id="webDev" name="interests" value="webDev">
                        <label for="webDev">Web Development</label>
                    </div>
                    <div>
                        <input type="checkbox" id="graphicDesign" name="interests" value="graphicDesign">
                        <label for="graphicDesign">Graphic Design</label>
                    </div>
                    <div>
                        <input type="checkbox" id="marketing" name="interests" value="marketing">
                        <label for="marketing">Digital Marketing</label>
                    </div>
                </div>
                <div class="form-group">
                    <label for="bio">Short Bio:</label>
                    <textarea id="bio" name="bio" rows="4" 
                              placeholder="Tell us about yourself"></textarea>
                </div>
                <div class="form-group">
                    <input type="checkbox" id="terms" name="terms" required>
                    <label for="terms">I agree to the terms and conditions</label>
                    <small class="error-message">You must agree to the terms</small>
                </div>
                <button type="submit">Register</button>
                <button type="reset">Reset Form</button>
            </form>
        </section>
        <section>
            <h2>Multimedia Elements</h2>
            <h3>Audio Example</h3>
            <audio controls>
                <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
                Your browser does not support the audio element.
            </audio>
            <h3>Video Example</h3>
            <video controls width="600">
                <source src="https://samplelib.com/lib/preview/mp4/sample-5s.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>
        </section>
    </main>
    <footer>
        <p>&copy; 2023 Advanced HTML5 Demo. All rights reserved.</p>
    </footer>
    <script>
        // Basic form validation feedback
        document.getElementById('registrationForm').addEventListener('submit', function(e) {
            const form = e.target;
            if (!form.checkValidity()) {
                e.preventDefault();
                e.stopPropagation();   
                // Show validation messages
                const invalidElements = form.querySelectorAll(':invalid');
                invalidElements.forEach(el => {
                    const errorMsg = el.nextElementSibling;
                    if (errorMsg && errorMsg.classList.contains('error-message')) {
                        errorMsg.style.display = 'block';
                    }
                });
            }
            form.classList.add('was-validated');
        });
        // Hide error messages when user starts typing
        document.querySelectorAll('input, select, textarea').forEach(input => {
            input.addEventListener('input', function() {
                const errorMsg = this.nextElementSibling;
                if (errorMsg && errorMsg.classList.contains('error-message')) {
                    errorMsg.style.display = 'none';
                }
            });
        });
    </script>
</body>
</html>
