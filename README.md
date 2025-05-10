# Softsell--Website2
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>SoftSell - Sell Your Unused Software Licenses</title>
  <link rel="stylesheet" href="style.css" />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
</head>
<body>
  <!-- Header -->
  <header>
    <div class="container nav">
      <h1>SoftSell</h1>
      <button class="btn-primary">Get a Quote</button>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="hero fade-in">
    <div class="container">
      <h2>Turn Unused Licenses Into Cash</h2>
      <p>Sell your unused software licenses safely, quickly, and for top dollar.</p>
      <button class="btn-primary">Sell My Licenses</button>
    </div>
  </section>

  <!-- How It Works -->
  <section class="how-it-works fade-in">
    <div class="container">
      <h2>How It Works</h2>
      <div class="steps">
        <div class="card">
          <h3>1. Upload License</h3>
          <p>Submit your license details securely.</p>
        </div>
        <div class="card">
          <h3>2. Get Valuation</h3>
          <p>Receive a fair market value instantly.</p>
        </div>
        <div class="card">
          <h3>3. Get Paid</h3>
          <p>Receive payment via your preferred method.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Why Choose Us -->
  <section class="why-us fade-in">
    <div class="container">
      <h2>Why Choose Us</h2>
      <div class="tiles">
        <div class="tile">✅ Fast Payments</div>
        <div class="tile">✅ 1000+ Trusted Clients</div>
        <div class="tile">✅ 24/7 Support</div>
        <div class="tile">✅ Secure Transactions</div>
      </div>
    </div>
  </section>

  <!-- Testimonials -->
  <section class="testimonials fade-in">
    <div class="container">
      <h2>Customer Testimonials</h2>
      <div class="testimonial">
        <p>“Super easy process and great support!”</p>
        <span>- Jane Doe, IT Manager at XYZ Corp</span>
      </div>
      <div class="testimonial">
        <p>“I had licenses just sitting there. Now I have cash.”</p>
        <span>- John Smith, Freelancer</span>
      </div>
    </div>
  </section>

  <!-- Contact Form -->
  <section class="contact fade-in">
    <div class="container">
      <h2>Contact Us</h2>
      <form id="lead-form">
        <input type="text" name="name" placeholder="Name" required />
        <input type="email" name="email" placeholder="Email" required />
        <input type="text" name="company" placeholder="Company" required />
        <select name="license-type" required>
          <option value="">Select License Type</option>
          <option value="windows">Windows</option>
          <option value="office">MS Office</option>
          <option value="adobe">Adobe Suite</option>
        </select>
        <textarea name="message" placeholder="Message" required></textarea>
        <button type="submit" class="btn-primary">Submit</button>
      </form>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="container">
      <p>&copy; 2025 SoftSell. All rights reserved.</p>
    </div>
  </footer>
  <script>
  const faders = document.querySelectorAll('.fade-in');

  const appearOptions = {
    threshold: 0.3
  };

  const appearOnScroll = new IntersectionObserver(function(entries, observer) {
    entries.forEach(entry => {
      if (!entry.isIntersecting) return;
      entry.target.classList.add('animate');
      observer.unobserve(entry.target);
    });
  }, appearOptions);

  faders.forEach(fader => {
    appearOnScroll.observe(fader);
  });
</script>

</body>
</html>

:root {
  --primary: #007BFF;
  --secondary: #f9f9f9;
  --text: #333;
  --accent: #28a745;
  --bg-gradient: linear-gradient(135deg, #e3f2fd, #ffffff);
}

* {
  box-sizing: border-box;
}

body {
  font-family: 'Inter', sans-serif;
  margin: 0;
  background: var(--bg-gradient);
  color: var(--text);
}

.container {
  max-width: 1100px;
  margin: 0 auto;
  padding: 2em;
}

header {
  background-color: white;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.hero {
  text-align: center;
  padding: 5em 2em;
  background: linear-gradient(to right, #007BFF, #00b4d8);
  color: white;
}

.hero h2 {
  font-size: 2.5em;
  margin-bottom: 0.5em;
}

.btn-primary {
  padding: 0.75em 1.5em;
  font-weight: bold;
  border: none;
  background-color: var(--accent);
  color: white;
  border-radius: 5px;
  cursor: pointer;
  transition: background 0.3s ease;
}

.btn-primary:hover {
  background-color: #218838;
}

section {
  padding: 3em 0;
}

.steps, .tiles {
  display: flex;
  flex-wrap: wrap;
  gap: 1.5em;
  justify-content: center;
}

.card, .tile, .testimonial {
  background: white;
  padding: 1.5em;
  border-radius: 8px;
  box-shadow: 0 3px 6px rgba(0,0,0,0.1);
  flex: 1 1 250px;
  transition: transform 0.2s;
}

.card:hover, .tile:hover {
  transform: translateY(-5px);
}

.testimonial p {
  font-style: italic;
}

.testimonial span {
  display: block;
  margin-top: 0.5em;
  color: #666;
}

form {
  display: flex;
  flex-direction: column;
  gap: 1em;
  max-width: 500px;
  margin: 0 auto;
}

input, select, textarea {
  padding: 0.75em;
  border: 1px solid #ccc;
  border-radius: 5px;
}

textarea {
  resize: vertical;
  height: 100px;
}

footer {
  background-color: #f0f0f0;
  text-align: center;
  padding: 1.5em 0;
  font-size: 0.9em;
}

@media (max-width: 768px) {
  .steps, .tiles {
    flex-direction: column;
  }

  .nav {
    flex-direction: column;
    gap: 1em;
  }
}
/* Fade-in animation */
.fade-in {
  opacity: 0;
  transform: translateY(20px);
  animation: fadeInUp 0.8s ease-out forwards;
}

@keyframes fadeInUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Zoom-in on hover */
.card:hover, .tile:hover {
  transform: scale(1.05);
  box-shadow: 0 6px 12px rgba(0,0,0,0.15);
}

/* Button click animation */
.btn-primary:active {
  transform: scale(0.95);
  transition: transform 0.1s;
}
.fade-in {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.6s ease, transform 0.6s ease;
}

.fade-in.animate {
  opacity: 1;
  transform: translateY(0);
}
