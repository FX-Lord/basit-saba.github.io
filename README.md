<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Saba AbdulBasit | Web Developer & Data Analyst</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.1/dist/chart.umd.min.js"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
</head>
<body class="bg-gray-50 dark:bg-gray-900 text-gray-900 dark:text-white">
  <!-- Navbar -->
  <nav class="fixed top-0 w-full bg-white dark:bg-gray-950 shadow-md z-50">
    <div class="max-w-6xl mx-auto px-6 py-4 flex justify-between items-center">
      <h1 class="text-2xl font-bold">Saba AbdulBasit</h1>
      <div class="flex gap-8">
        <a href="#about" class="hover:text-blue-600">About</a>
        <a href="#projects" class="hover:text-blue-600">Projects</a>
        <a href="#analytics" class="hover:text-blue-600">Analytics</a>
        <a href="#contact" class="hover:text-blue-600">Contact</a>
      </div>
      <button id="theme-toggle" class="text-2xl">🌙</button>
    </div>
  </nav>

  <!-- Hero -->
  <section class="min-h-screen flex items-center pt-20 bg-gradient-to-br from-blue-600 to-purple-600 text-white">
    <div class="max-w-6xl mx-auto px-6 text-center">
      <h2 class="text-5xl font-bold mb-4">Hi, I'm Saba 👋</h2>
      <p class="text-2xl mb-8">300L Mass Communication Student | Aspiring Full-Stack Web Developer & Data Analyst</p>
      <a href="#projects" class="bg-white text-blue-600 px-8 py-4 rounded-full font-semibold text-lg hover:bg-gray-100">View My Work</a>
    </div>
  </section>

  <!-- About -->
  <section id="about" class="py-20 max-w-6xl mx-auto px-6">
    <h2 class="text-4xl font-bold text-center mb-12">About Me</h2>
    <div class="grid md:grid-cols-2 gap-12">
      <div>
        <p class="text-lg">I'm a 300-level Mass Communication student at LASUSTECH who combines creative storytelling with modern web development and data analytics. I build beautiful, responsive websites and turn raw data into actionable insights.</p>
      </div>
      <div>
        <h3 class="font-semibold mb-4">Skills</h3>
        <div class="flex flex-wrap gap-3">
          <span class="bg-blue-100 dark:bg-blue-900 px-4 py-2 rounded-full text-sm">React.js</span>
          <span class="bg-blue-100 dark:bg-blue-900 px-4 py-2 rounded-full text-sm">Tailwind CSS</span>
          <span class="bg-blue-100 dark:bg-blue-900 px-4 py-2 rounded-full text-sm">JavaScript</span>
          <span class="bg-blue-100 dark:bg-blue-900 px-4 py-2 rounded-full text-sm">Chart.js</span>
          <span class="bg-blue-100 dark:bg-blue-900 px-4 py-2 rounded-full text-sm">Python (Pandas)</span>
          <span class="bg-blue-100 dark:bg-blue-900 px-4 py-2 rounded-full text-sm">Git & GitHub</span>
        </div>
      </div>
    </div>
  </section>

  <!-- Projects -->
  <section id="projects" class="bg-gray-100 dark:bg-gray-950 py-20">
    <div class="max-w-6xl mx-auto px-6">
      <h2 class="text-4xl font-bold text-center mb-12">Featured Projects</h2>
      <!-- Add more cards as you build other projects -->
      <div class="grid md:grid-cols-2 gap-8">
        <div class="bg-white dark:bg-gray-900 p-8 rounded-2xl shadow">
          <h3 class="font-bold text-xl mb-3">News Sentiment Analyzer</h3>
          <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">React • NewsAPI • Chart.js</p>
          <p>Live news sentiment analysis tool built for media professionals.</p>
          <a href="#" class="text-blue-600 mt-4 inline-block">→ View on GitHub</a>
        </div>
        <!-- Duplicate this block for other projects later -->
      </div>
    </div>
  </section>

  <!-- Data Analytics Dashboard -->
  <section id="analytics" class="py-20 max-w-6xl mx-auto px-6">
    <h2 class="text-4xl font-bold text-center mb-12">Data Insights Dashboard</h2>
    <div class="bg-white dark:bg-gray-900 p-8 rounded-3xl shadow-xl max-w-2xl mx-auto">
      <canvas id="growthChart"></canvas>
    </div>
  <p class="text-center mt-6 text-sm text-gray-600 dark:text-gray-400">Audience Growth Over 6 Months (simulated data from media projects)</p>
  </section>

  <!-- Contact -->
  <section id="contact" class="py-20 bg-gray-100 dark:bg-gray-950">
    <div class="max-w-2xl mx-auto px-6">
      <h2 class="text-4xl font-bold text-center mb-12">Get In Touch</h2>
      <form class="space-y-6">
        <input type="text" placeholder="Your Name" class="w-full px-6 py-4 rounded-xl border dark:bg-gray-900">
        <input type="email" placeholder="Your Email" class="w-full px-6 py-4 rounded-xl border dark:bg-gray-900">
        <textarea placeholder="Message" rows="6" class="w-full px-6 py-4 rounded-xl border dark:bg-gray-900"></textarea>
        <button type="button" class="w-full bg-blue-600 text-white py-4 rounded-xl font-semibold">Send Message</button>
      </form>
    </div>
  </section>

  <footer class="py-8 text-center text-sm">
    © 2026 Saba AbdulBasit Olamilekan • Built with ❤️ using GitHub Pages
  </footer>

  <script>
    // Tailwind script
    tailwind.config = { content: ["*"], theme: { extend: {} } }

    // Dark mode toggle
    const toggle = document.getElementById('theme-toggle');
    toggle.addEventListener('click', () => {
      document.documentElement.classList.toggle('dark');
      toggle.textContent = document.documentElement.classList.contains('dark') ? '☀️' : '🌙';
    });

    // Chart.js
    new Chart(document.getElementById('growthChart'), {
      type: 'line',
      data: {
        labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun'],
        datasets: [{
          label: 'Audience Growth (%)',
          data: [12, 19, 35, 28, 45, 62],
          borderColor: '#3b82f6',
          tension: 0.4
        }]
      },
      options: { responsive: true, plugins: { legend: { display: false } } }
    });
  </script>
</body>
</html>
