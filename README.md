# Online-Course-Registration-System
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Course Registration System</title>
  <style>
    /* Background image & overlay */
    body {
      font-family: Arial, sans-serif;
      margin: 0; padding: 0;
      color: #333;
      background: url('https://images.unsplash.com/photo-1504384308090-c894fdcc538d?auto=format&fit=crop&w=1920&q=80') no-repeat center center fixed;
      background-size: cover;
      position: relative;
      min-height: 100vh;
    }
    body::before {
      content: "";
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      background-color: rgba(0,0,0,0.45); /* dark overlay */
      z-index: -1;
    }
    body {
      font-family: Arial, sans-serif;
      margin: 0; padding: 0;
      background-color: #f6f6f6;
      color: #333;
    }
    header {
      background-color: #e76a00;
      color: white;
      padding: 20px;
      text-align: center;
    }
    nav {
      margin-top: 10px;
    }
    nav a {
      color: white;
      text-decoration: none;
      margin: 0 12px;
      font-weight: bold;
      cursor: pointer;
    }
    nav a:hover {
      text-decoration: underline;
    }
    main {
      max-width: 900px;
      margin: 20px auto;
      padding: 0 10px;
      min-height: 400px;
      background: white;
      border-radius: 6px;
      box-shadow: 0 0 6px #ccc;
    }
    h1, h2, h3 {
      margin-top: 0;
    }
    .hidden {
      display: none;
    }
    form {
      max-width: 400px;
      margin-top: 10px;
    }
    label {
      display: block;
      margin-top: 10px;
      font-weight: bold;
    }
    input, select, textarea {
      width: 100%;
      padding: 8px;
      margin-top: 4px;
      box-sizing: border-box;
      border: 1px solid #ccc;
      border-radius: 4px;
      font-size: 14px;
    }
    button {
      margin-top: 15px;
      background-color: #e76a00;
      color: white;
      border: none;
      padding: 10px 16px;
      font-size: 16px;
      border-radius: 4px;
      cursor: pointer;
    }
    button:hover {
      background-color: #cf5c00;
    }
    footer {
      text-align: center;
      padding: 15px;
      background-color: #e76a00;
      color: white;
      margin-top: 40px;
    }
    /* Responsive */
    @media (max-width: 600px) {
      nav a {
        display: block;
        margin: 10px 0;
      }
      main {
        margin: 10px;
      }
      .flex-container {
        flex-direction: column;
      }
      form {
        max-width: 100%;
      }
    }
    /* Flex container for login & register side-by-side */
    .flex-container {
      display: flex;
      justify-content: space-between;
      gap: 30px;
      margin-top: 20px;
    }
    .flex-container > div {
      flex: 1;
      background: #fafafa;
      padding: 20px;
      border-radius: 6px;
      box-shadow: 0 0 5px #ccc;
    }
  </style>
</head>
<body>

  <header>
    <h1>Course Registration System</h1>
    <nav aria-label="Main navigation">
      <a onclick="showSection('home')">Home</a>
      <a onclick="showSection('about')">About Us</a>
      <a onclick="showSection('courses')">All Courses</a>
      <a onclick="showSection('loginregister')">Login / Register</a>
      <a onclick="showSection('contact')">Contact Us</a>
      <a onclick="showSection('feedback')">Feedback</a>
    </nav>
  </header>

  <main>
    <!-- Home -->
    <section id="home" class="">
      <h2>Welcome to the Course Registration System</h2>
      <p>Our platform allows you to effortlessly browse and enroll in courses tailored to your academic path.</p>
      <p><strong>Current Registration Period:</strong> May 1 - May 10, 2025</p>

      <h3>Why Choose Our System?</h3>
      <ul>
        <li><strong>User-friendly Interface:</strong> Easily search and register for courses in just a few clicks.</li>
        <li><strong>Real-Time Updates:</strong> Get instant notifications about course availability and registration deadlines.</li>
        <li><strong>Personalized Dashboard:</strong> Manage your enrolled courses, track your progress, and access study materials.</li>
        <li><strong>Secure and Reliable:</strong> Your data and credentials are protected with the latest security standards.</li>
      </ul>

      <h3>Getting Started</h3>
      <p>If you’re new, please register to create your student account. Already have one? Simply log in to start registering for courses.</p>
      <button onclick="showSection('loginregister')">Login / Register Now</button>
    </section>

    <!-- About Us -->
    <section id="about" class="hidden">
      <h2>About Us</h2>
      <p>We are committed to providing a seamless course registration experience for students and faculty alike.</p>
      <p>Our system supports a wide range of degree programs including BTech, BSc, BA, and BCom, ensuring flexibility and accessibility.</p>
      <h3>Our Mission</h3>
      <p>To empower students to take control of their academic journey through a user-friendly, reliable, and efficient registration platform.</p>
      <h3>Key Features</h3>
      <ul>
        <li>Real-time course availability and seat tracking.</li>
        <li>Personalized course recommendations based on your program.</li>
        <li>Secure login and data privacy protection.</li>
        <li>24/7 customer support via email and chat.</li>
      </ul>
      <p>We continuously improve our platform based on user feedback. Your success is our priority!</p>
    </section>

   <!-- All Courses -->
<section id="courses" class="hidden">
  <h2>All Courses</h2>

  <h3>Technical Courses</h3>
  <ul>
    <li><strong>BTech</strong>: Engineering and Technology courses including Computer Science, Mechanical, Electrical, Civil, etc.</li>
    <li><strong>BSc</strong>: Science courses in Physics, Chemistry, Biology, Mathematics, Information Technology, etc.</li>
    <li><strong>Diploma in Software Development</strong>: Programming, Database Management, Web Development.</li>
    <li><strong>Certified Networking Courses</strong>: CCNA, Network Security, Cloud Computing.</li>
  </ul>

  <h3>Non-Technical Courses</h3>
  <ul>
    <li><strong>BA</strong>: Arts courses including History, Literature, Political Science, Sociology, Psychology.</li>
    <li><strong>BCom</strong>: Commerce courses covering Accounting, Finance, Business Management, Marketing, Economics.</li>
    <li><strong>Diploma in Human Resource Management</strong>: Personnel Management, Labour Laws, Organizational Behavior.</li>
    <li><strong>Certificate in Communication Skills</strong>: Public Speaking, Business Communication, Writing Skills.</li>
  </ul>

  <h3>Government Exam Preparation Courses</h3>
  <ul>
    <li><strong>UPSC Civil Services</strong>: General Studies, Optional Subjects, Interview Preparation.</li>
    <li><strong>SSC CGL</strong>: Quantitative Aptitude, Reasoning, General Awareness.</li>
    <li><strong>Railway Recruitment Board (RRB)</strong>: Technical and Non-Technical posts preparation.</li>
    <li><strong>Bank PO/Clerk</strong>: Banking Awareness, English, Aptitude, Computer Knowledge.</li>
    <li><strong>Defence Exams</strong>: NDA, CDS, AFCAT, Physical Fitness Training.</li>
  </ul>
</section>

<!-- Login & Register combined with separate toggle buttons -->
<section id="loginregister" class="hidden" aria-label="Login and Registration forms">
  <h2>Login or Register</h2>
  
  <!-- Buttons to switch between forms -->
  <div style="margin-bottom: 20px;">
    <button type="button" onclick="showLogin()">Login</button>
    <button type="button" onclick="showRegister()">Register</button>
  </div>

  <!-- Login form -->
  <div id="login-form" style="display:none; background:#fafafa; padding:20px; border-radius:6px; box-shadow: 0 0 5px #ccc;">
    <h3>Login</h3>
    <p>Enter your credentials to access your account and manage your courses.</p>
    <form onsubmit="alert('Login submitted!'); return false;">
      <label for="login-email">Email:</label>
      <input type="email" id="login-email" name="login-email" required placeholder="you@example.com" />
      
      <label for="login-password">Password:</label>
      <input type="password" id="login-password" name="login-password" required placeholder="Enter your password" />

      <button type="submit">Login</button>
    </form>
    <p style="margin-top: 15px; font-size: 14px;">
      Forgot your password? <a href="#" onclick="alert('Password reset feature coming soon!'); return false;">Click here</a> to reset it.
    </p>
  </div>

  <!-- Register form -->
  <div id="register-form" style="display:none; background:#fafafa; padding:20px; border-radius:6px; box-shadow: 0 0 5px #ccc;">
    <h3>Register</h3>
    <p>Create a new account to enroll in courses and track your academic progress.</p>
    <form onsubmit="alert('Registration submitted!'); return false;">
      <label for="reg-name">Full Name:</label>
      <input type="text" id="reg-name" name="reg-name" required placeholder="John Doe" />

      <label for="reg-email">Email:</label>
      <input type="email" id="reg-email" name="reg-email" required placeholder="you@example.com" />

      <label for="reg-course">Select Course:</label>
      <select id="reg-course" name="reg-course" required>
        <option value="" disabled selected>Select your course</option>
        <option value="btech">BTech</option>
        <option value="bsc">BSc</option>
        <option value="ba">BA</option>
        <option value="bcom">BCom</option>
      </select>

      <label for="reg-password">Password:</label>
      <input type="password" id="reg-password" name="reg-password" required placeholder="Choose a strong password" />

      <label for="reg-password-confirm">Confirm Password:</label>
      <input type="password" id="reg-password-confirm" name="reg-password-confirm" required placeholder="Re-enter your password" />

      <button type="submit">Register</button>
    </form>
  </div>
</section>

<script>
  function showLogin() {
    document.getElementById('login-form').style.display = 'block';
    document.getElementById('register-form').style.display = 'none';
  }

  function showRegister() {
    document.getElementById('login-form').style.display = 'none';
    document.getElementById('register-form').style.display = 'block';
  }

  // By default, show Login form when user navigates to login/register section
  function showSection(sectionId) {
    const sections = document.querySelectorAll('main > section');
    sections.forEach(sec => {
      if (sec.id === sectionId) {
        sec.classList.remove('hidden');
      } else {
        sec.classList.add('hidden');
      }
    });
    window.scrollTo(0,0);

    if(sectionId === 'loginregister') {
      showLogin(); // default show login form
    }
  }
</script>

    <!-- Contact Us -->
    <section id="contact" class="hidden" aria-label="Contact form">
      <h2>Contact Us</h2>
      <form onsubmit="alert('Message sent!'); return false;">
        <label for="contact-name">Name:</label>
        <input type="text" id="contact-name" name="contact-name" required placeholder="Your Name" />

        <label for="contact-email">Email:</label>
        <input type="email" id="contact-email" name="contact-email" required placeholder="you@example.com" />

        <label for="contact-message">Message:</label>
        <textarea id="contact-message" name="contact-message" rows="5" required placeholder="Write your message here..."></textarea>

        <button type="submit">Send Message</button>
      </form>
    </section>

    <!-- Feedback Section -->
    <section id="feedback" class="hidden" aria-label="Feedback form">
      <h2>Feedback</h2>
      <form onsubmit="alert('Thank you for your feedback!'); return false;">
        <label for="feedback-name">Name:</label>
        <input type="text" id="feedback-name" name="feedback-name" required placeholder="Your Name" />

        <label for="feedback-email">Email:</label>
        <input type="email" id="feedback-email" name="feedback-email" required placeholder="you@example.com" />

        <label for="feedback-message">Your Feedback:</label>
        <textarea id="feedback-message" name="feedback-message" rows="5" required placeholder="Write your feedback or suggestions here..."></textarea>

        <button type="submit">Submit Feedback</button>
      </form>
    </section>
  </main>

  <footer>
    © 2025 Course Registration System
  </footer>

  <script>
    function showSection(sectionId) {
      const sections = document.querySelectorAll('main > section');
      sections.forEach(sec => {
        if (sec.id === sectionId) {
          sec.classList.remove('hidden');
        } else {
          sec.classList.add('hidden');
        }
      });
      // Scroll to top on section change
      window.scrollTo(0,0);
    }

    // Show home by default on load
    document.addEventListener('DOMContentLoaded', () => {
      showSection('home');
    });
  </script>
</body>
</html>
