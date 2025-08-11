<script>
  import logoUrl from '$lib/assets/logo.png';
</script>

<svelte:head>
  <style>
    body, html {
      margin: 0 !important;
      padding: 0 !important;
      overflow-x: hidden;
    }
  </style>
</svelte:head>

<header class="hero-header">
  <div class="hero-container">
    <!-- Logo Section -->
    <div class="logo-section">
      <img src={logoUrl} alt="Rush Media Tech" class="hero-logo" />
    </div>
    
    <!-- Main Content -->
    <div class="hero-content">
      <h1 class="hero-title">
        Elevate Your Brand with 
        <span class="gradient-text">Professional Media</span>
      </h1>
      
      <p class="hero-description">
        From stunning visuals to powerful websites, we create content that captivates your audience and drives results. Professional photography, video production, and web development that makes your brand stand out.
      </p>
      
      <div class="hero-buttons">
        <a href="/contact" class="btn-primary">Start Your Project</a>
        <a href="/services" class="btn-secondary">View Our Services</a>
      </div>
    </div>
    
    <!-- Services Grid -->
    <div class="services-grid">
      <div class="service-card">
        <div class="service-icon">📸</div>
        <h3>Visual Content & Media</h3>
        <p>Professional photography and video content that stops the scroll and drives engagement across all platforms.</p>
      </div>
      
      <div class="service-card">
        <div class="service-icon">🎬</div>
        <h3>Video Production</h3>
        <p>From corporate training to promotional content, we bring your story to life with compelling video.</p>
      </div>
      
      <div class="service-card">
        <div class="service-icon">🌐</div>
        <h3>Web Development</h3>
        <p>Beautiful, high-performing websites that convert visitors into customers and grow your business.</p>
      </div>
    </div>
  </div>
</header>

<style>
  :root {
    --primary-teal: #20B2AA;
    --secondary-teal: #48CAE4;
    --dark-teal: #0F5F5C;
    --accent-coral: #FF6B6B;
    --warm-coral: #FF7F7F;
    --gradient-start: #20B2AA;
    --gradient-end: #48CAE4;
    --white: #FFFFFF;
    --light-gray: #F7FAFC;
    --medium-gray: #A0AEC0;
    --charcoal: #2D3748;
    --dark-charcoal: #1A202C;
    --font-primary: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    --font-heading: 'Poppins', var(--font-primary);
  }

  .hero-header {
    min-height: 100vh;
    background: var(--white);
    color: var(--charcoal);
    position: relative;
    overflow: hidden;
    width: 100vw;
    margin: 0;
    padding: 0;
  }

  .hero-header::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: 
      radial-gradient(circle at 20% 20%, rgba(32, 178, 170, 0.05) 0%, transparent 50%),
      radial-gradient(circle at 80% 80%, rgba(255, 107, 107, 0.03) 0%, transparent 50%);
    pointer-events: none;
  }

  .hero-container {
    position: relative;
    z-index: 10;
    max-width: 1400px;
    margin: 0 auto;
    padding: 3rem 2rem;
    display: grid;
    grid-template-areas: 
      "logo"
      "content"
      "services";
    gap: 3rem;
    align-items: center;
    min-height: 100vh;
  }

  .logo-section {
    grid-area: logo;
    text-align: center;
    padding: 2rem 0;
  }

  .hero-logo {
    width: 80%;
    height: auto;
    max-width: none;
    filter: drop-shadow(0 4px 15px rgba(45, 55, 72, 0.15));
    transition: transform 0.3s ease;
  }

  .hero-logo:hover {
    transform: scale(1.05);
  }

  .hero-content {
    grid-area: content;
    text-align: center;
    max-width: 800px;
    margin: 0 auto;
  }

  .hero-title {
    font-family: var(--font-heading);
    font-size: clamp(2.5rem, 6vw, 4.5rem);
    font-weight: 700;
    line-height: 1.1;
    margin: 0 0 2rem 0;
    color: var(--charcoal);
    text-shadow: none;
  }

  .gradient-text {
    background: linear-gradient(45deg, var(--primary-teal), var(--accent-coral));
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-size: 200% 200%;
    animation: gradientShift 4s ease-in-out infinite;
  }

  @keyframes gradientShift {
    0%, 100% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
  }

  .hero-description {
    font-size: clamp(1.1rem, 2.5vw, 1.4rem);
    line-height: 1.6;
    color: var(--medium-gray);
    margin: 0 0 3rem 0;
    text-shadow: none;
  }

  .hero-buttons {
    display: flex;
    gap: 1.5rem;
    justify-content: center;
    flex-wrap: wrap;
  }

  .btn-primary, .btn-secondary {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 1.2rem 2.5rem;
    font-size: 1.1rem;
    font-weight: 600;
    border-radius: 12px;
    text-decoration: none;
    transition: all 0.3s ease;
    border: 2px solid transparent;
    cursor: pointer;
    white-space: nowrap;
    min-width: 200px;
  }

  .btn-primary {
    background: var(--accent-coral);
    color: var(--white);
    box-shadow: 0 10px 25px rgba(255, 107, 107, 0.25);
  }

  .btn-primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 15px 35px rgba(255, 107, 107, 0.35);
    background: var(--warm-coral);
  }

  .btn-secondary {
    background: transparent;
    color: var(--primary-teal);
    border-color: var(--primary-teal);
    backdrop-filter: none;
  }

  .btn-secondary:hover {
    background: var(--primary-teal);
    color: var(--white);
    transform: translateY(-3px);
    box-shadow: 0 10px 25px rgba(32, 178, 170, 0.25);
  }

  .services-grid {
    grid-area: services;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
  }

  .service-card {
    background: var(--white);
    border: 2px solid var(--light-gray);
    border-radius: 20px;
    padding: 2.5rem 2rem;
    text-align: center;
    transition: all 0.4s ease;
    box-shadow: 0 8px 25px rgba(45, 55, 72, 0.08);
  }

  .service-card:hover {
    transform: translateY(-8px);
    background: var(--white);
    box-shadow: 0 20px 40px rgba(45, 55, 72, 0.12);
    border-color: var(--primary-teal);
  }

  .service-icon {
    font-size: 3rem;
    margin-bottom: 1.5rem;
    filter: none;
  }

  .service-card h3 {
    font-family: var(--font-heading);
    font-size: 1.4rem;
    font-weight: 600;
    margin: 0 0 1rem 0;
    color: var(--charcoal);
    text-shadow: none;
  }

  .service-card p {
    color: var(--medium-gray);
    line-height: 1.6;
    margin: 0;
    font-size: 1rem;
    text-shadow: none;
  }

  /* Responsive Design */
  @media (max-width: 768px) {
    .hero-container {
      padding: 2rem 1rem;
      gap: 2rem;
    }

    .hero-logo {
      width: 85%;
    }

    .hero-buttons {
      flex-direction: column;
      align-items: center;
    }

    .btn-primary, .btn-secondary {
      width: 100%;
      max-width: 300px;
    }

    .services-grid {
      grid-template-columns: 1fr;
      gap: 1.5rem;
    }

    .service-card {
      padding: 2rem 1.5rem;
    }
  }

  @media (min-width: 1024px) {
    .hero-container {
      grid-template-areas: 
        "logo logo"
        "content services";
      grid-template-columns: 1fr 1fr;
      gap: 4rem;
      padding: 4rem 3rem;
    }

    .hero-content {
      text-align: left;
      margin: 0;
    }

    .hero-buttons {
      justify-content: flex-start;
    }

    .hero-logo {
      width: 80%;
    }

    .services-grid {
      grid-template-columns: 1fr;
      margin-top: 0;
    }
  }

  @media (min-width: 1200px) {
    .hero-logo {
      width: 75%;
    }

    .hero-container {
      padding: 5rem 4rem;
    }
  }
</style>