# quiz-world.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Quiz World</title>

  <style>
    body {
      font-family: 'Arial', sans-serif;
      margin: 0;
      padding: 0;
      background: #f7f9fc;
      color: #333;
      text-align: center;
      transition: background 0.3s ease, color 0.3s ease;
    }

    header {
      background: linear-gradient(90deg, #6a11cb 0%, #2575fc 100%);
      color: white;
      padding: 20px 0;
    }

    h1 {
      margin: 0;
      font-size: 2.5rem;
    }

    .intro {
      margin: 40px 0;
      font-size: 1.2rem;
      max-width: 800px;
      margin-left: auto;
      margin-right: auto;
      color: #555;
    }

    .quiz-list {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      margin-top: 30px;
    }

    .quiz-card {
      background: #fff;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      padding: 20px;
      width: 250px;
      text-align: center;
      transition: transform 0.3s ease;
    }

    .quiz-card:hover {
      transform: translateY(-10px);
    }

    .quiz-card h3 {
      margin: 10px 0;
      font-size: 1.5rem;
    }

    .quiz-card p {
      font-size: 1rem;
      margin: 10px 0;
      color: #777;
    }

    .quiz-card a {
      display: inline-block;
      background: #28a745;
      color: white;
      padding: 10px 20px;
      text-decoration: none;
      border-radius: 5px;
      font-weight: bold;
      transition: background 0.3s ease;
    }

    .quiz-card a:hover {
      background: #218838;
    }

    .cta-button {
      margin-top: 20px;
      background: #007bff;
      color: white;
      padding: 15px 30px;
      font-size: 1.2rem;
      text-decoration: none;
      border-radius: 8px;
      display: inline-block;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    .cta-button:hover {
      background: #0056b3;
    }

    footer {
      background: linear-gradient(90deg, #6a11cb 0%, #2575fc 100%);
      color: white;
      padding: 10px 0;
      margin-top: 40px;
    }

    /* Fade-In Animation */
    .fade-in {
      opacity: 0;
      transform: translateY(20px);
      transition: opacity 0.5s ease, transform 0.5s ease;
    }

    .fade-in.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* Language switcher styles */
    .language-switch {
      margin-top: 20px;
    }

    .language-switch button {
      padding: 10px 20px;
      margin: 0 10px;
      font-size: 1rem;
      cursor: pointer;
      border-radius: 5px;
      border: none;
    }

    /* Grade selection styles */
    .grade-select {
      margin-top: 20px;
    }

    .grade-select select {
      padding: 10px;
      font-size: 1rem;
      border-radius: 5px;
      border: 1px solid #ccc;
      margin-top: 10px;
    }

    /* Contact Us Section */
    .contact-us {
      margin-top: 40px;
      text-align: center;
    }

    .contact-us h2 {
      font-size: 2rem;
      margin-bottom: 20px;
    }

    .contact-buttons {
      display: flex;
      justify-content: center;
      gap: 15px;
      margin-top: 20px;
    }

    .contact-buttons a {
      display: flex;
      align-items: center;
      justify-content: center;
      background: #25d366; /* WhatsApp color */
      color: white;
      padding: 10px 15px;
      border-radius: 50%;
      font-size: 1.5rem;
      text-decoration: none;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease, background 0.3s ease;
    }

    .contact-buttons a:hover {
      transform: scale(1.1);
    }

    .contact-buttons .facebook {
      background: #3b5998;
    }

    .contact-buttons .youtube {
      background: #ff0000;
    }

    .contact-buttons .call {
      background: #34b7f1;
    }

    /* Responsive for contact buttons */
    @media (max-width: 600px) {
      .contact-buttons {
        flex-direction: column;
        gap: 10px;
      }
    }

    /* Dark Theme */
    body.dark {
      background-color: #121212;
      color: #e0e0e0;
    }

    body.dark header,
    body.dark footer {
      background: linear-gradient(90deg, #1e1e1e 0%, #3a3a3a 100%);
    }

    body.dark .quiz-card {
      background: #1f1f1f;
      color: #fff;
    }

    body.dark .quiz-card p {
      color: #bbb;
    }

    body.dark .quiz-card a {
      background: #00c851;
    }

    body.dark .quiz-card a:hover {
      background: #007e33;
    }

    body.dark .cta-button {
      background: #3399ff;
    }

    body.dark .cta-button:hover {
      background: #0056b3;
    }

    body.dark .cta-card {
      background: #222;
      color: #eee;
    }

    /* CTA Section */
    .cta-card {
      background: #ffffff;
      padding: 30px;
      margin: 40px auto;
      border-radius: 15px;
      box-shadow: 0 6px 15px rgba(0,0,0,0.1);
      max-width: 600px;
      text-align: center;
    }
  </style>
</head>
<body>

  <!-- Language Switch -->
  <div class="language-switch">
    <button onclick="switchLanguage('en')">English 😊 </button>
    <button onclick="switchLanguage('si')">සිංහල 😁</button>
    <button onclick="toggleTheme()">🌙 Toggle Theme</button>
  </div>

  <!-- Header Section -->
  <header>
    <h1 class="fade-in">Quiz World🧠</h1>
  </header>

  <!-- Introduction Section -->
  <section class="intro fade-in">
    <p>Welcome to the Quiz World! Test your knowledge by participating in various quiz competitions hosted on Google Forms. Join now and test your knowledge!🧠</p>
  </section>

  <!-- Grade Selection Section -->
  <section class="fade-in">
    <h2>Select Your Grade</h2>
    <div class="grade-select">
      <select id="grade-select" onchange="selectGrade(this.value)">
        <option value="none" selected disabled>Select Grade</option>
        <option value="10">Grade 10</option>
        <option value="11">Grade 11</option>
      </select>
    </div>
  </section>

  <!-- Available Quizzes Section -->
  <section class="fade-in">
    <h2>Open Quizzes</h2>
    <div class="quiz-list">
      <!-- Quiz Card 1 -->
      <div class="quiz-card">
        <h3 class="quiz-title">ICT Quiz</h3>
        <p>Test your knowledge in Information and Communication Technology (ICT).</p>
        <a href="https://forms.gle/xyz123" target="_blank" onclick="trackQuizClick('ICT Quiz')">Join Quiz</a>
      </div>

      <!-- Quiz Card 2 -->
      <div class="quiz-card">
        <h3 class="quiz-title">General Knowledge</h3>
        <p>Test your general knowledge on a variety of topics!</p>
        <a href="https://docs.google.com/forms/d/e/1FAIpQLSc8Vkxr3iMY01qJ_Eq9todNi3ZbgvJJF9mwosaQphzYf87I1g/viewform?usp=dialog" target="_blank" onclick="trackQuizClick('General Knowledge')">Join Quiz</a>
      </div>

      <!-- Quiz Card 3 -->
      <div class="quiz-card">
        <h3 class="quiz-title">Math Challenge</h3>
        <p>Are you ready for a tough math competition?</p>
        <a href="https://forms.gle/789xyz" target="_blank" onclick="trackQuizClick('Math Challenge')">Join Quiz</a>
      </div>
    </div>
  </section>

  <!-- CTA Covered Button Section -->
  <section class="cta-card fade-in">
    <h2>Ready to Join the Quiz Hub?</h2>
    <p>Challenge your brain with fun quizzes and show what you know!</p>
    <a href="https://docs.google.com/forms/d/e/1FAIpQLSfqMFUrghd7vSwU-P4PV6TGvPpix24y0gWcEumX9jeyDH-gkg/viewform?usp=dialog" target="_blank" class="cta-button">🧠 Join Quiz World! 🧠</a>
  </section>

  <!-- Contact Us Section -->
  <section class="contact-us fade-in">
    <h2>Contact Us</h2>
    <div class="contact-buttons">
      <a href="https://wa.me/1234567890" target="_blank" aria-label="Contact us via WhatsApp">
        <i class="fab fa-whatsapp"></i>
      </a>
      <a href="tel:+1234567890" class="call" aria-label="Call us">
        <i class="fas fa-phone"></i>
      </a>
      <a href="https://www.facebook.com/yourpage" class="facebook" target="_blank" aria-label="Visit our Facebook page">
        <i class="fab fa-facebook"></i>
      </a>
      <a href="https://www.youtube.com/yourchannel" class="youtube" target="_blank" aria-label="Visit our YouTube channel">
        <i class="fab fa-youtube"></i>
      </a>
    </div>
  </section>

  <!-- Footer Section -->
  <footer>
    <p>&copy; Powered by Bisco Wipars | Designed by Maheen❤️ | © 2025 Quiz World | All Rights Reserved</p>
  </footer>

  <script>
    // Fade-In on scroll
    document.addEventListener('DOMContentLoaded', () => {
      const fadeElements = document.querySelectorAll('.fade-in');
      const observerOptions = {
        root: null,
        threshold: 0.1,
      };
      const fadeInObserver = new IntersectionObserver((entries, observer) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add('visible');
            observer.unobserve(entry.target);
          }
        });
      }, observerOptions);
      fadeElements.forEach(el => fadeInObserver.observe(el));
    });

    // Google Analytics Click Tracking
    function trackQuizClick(quizName) {
      if (typeof gtag === 'function') {
        gtag('event', 'quiz_click', {
          'event_category': 'Quizzes',
          'event_label': quizName,
          'value': 1
        });
      }
    }

    // Language Switcher
    const content = {
      en: {
        header: 'Quiz World🧠',
        intro: 'Welcome to the Quiz Hub! Test your knowledge...',
        quiz1: 'ICT Quiz',
        quiz2: 'General Knowledge',
        quiz3: 'Math Challenge',
        grade: 'Select Your Grade',
        grade10: 'Grade 10',
        grade11: 'Grade 11'
      },
      si: {
        header: 'දැනුම ලෝකය 🧠',
        intro: 'දැනුම පරීක්ෂණ සඳහා එක්වන්න...',
        quiz1: 'I.C.T. පරීක්ෂණය',
        quiz2: 'සාමාන්‍ය දැනුම',
        quiz3: 'ගණිතය',
        grade: 'ඔබේ පන්තිය තෝරන්න',
        grade10: 'පන්තිය 10',
        grade11: 'පන්තිය 11'
      }
    };

    function switchLanguage(lang) {
      document.querySelector('h1').textContent = content[lang].header;
      document.querySelector('.intro p').textContent = content[lang].intro;
      document.querySelectorAll('.quiz-title')[0].textContent = content[lang].quiz1;
      document.querySelectorAll('.quiz-title')[1].textContent = content[lang].quiz2;
      document.querySelectorAll('.quiz-title')[2].textContent = content[lang].quiz3;
      document.querySelector('h2').textContent = content[lang].grade;
      document.querySelectorAll('option')[1].textContent = content[lang].grade10;
      document.querySelectorAll('option')[2].textContent = content[lang].grade11;
    }

    function selectGrade(grade) {
      if (grade === '10') {
        window.location.href = "grade10.html";
      } else if (grade === '11') {
        window.location.href = "grade11.html";
      }
    }

    function toggleTheme() {
      document.body.classList.toggle('dark');
    }
  </script>

</body>
</html>
