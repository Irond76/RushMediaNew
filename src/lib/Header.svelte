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
  <!-- Animated Background Elements -->
  <div class="bg-animation">
    <div class="floating-shape shape-1"></div>
    <div class="floating-shape shape-2"></div>
    <div class="floating-shape shape-3"></div>
  </div>

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
        <a href="/contact" class="btn-primary">
          <span>Start Your Project</span>
          <svg class="btn-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
            <path d="M5 12h14M12 5l7 7-7 7"/>
          </svg>
        </a>
        <a href="/services" class="btn-secondary">
          <span>View Our Services</span>
        </a>
      </div>
    </div>
    
    <!-- Enhanced Services Grid -->
    <div class="services-grid">
      <div class="service-card card-1">
        <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor">
            <rect x="3" y="3" width="18" height="18" rx="2" ry="2"/>
            <circle cx="9" cy="9" r="2"/>
            <path d="m21 15-3.086-3.086a2 2 0 0 0-2.828 0L6 21"/>
          </svg>
        </div>
        <h3>Visual Content & Media</h3>
        <p>Professional photography and video content that stops the scroll and drives engagement across all platforms.</p>
        <div class="card-accent"></div>
      </div>
      
      <div class="service-card card-2">
        <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor">
            <polygon points="23 7 16 12 23 17 23 7"/>
            <rect x="1" y="5" width="15" height="14" rx="2" ry="2"/>
          </svg>
        </div>
        <h3>Video Production</h3>
        <p>From corporate training to promotional content, we bring your story to life with compelling video.</p>
        <div class="card-accent"></div>
      </div>
      
      <div class="service-card card-3">
        <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor">
            <circle cx="12" cy="12" r="10"/>
            <line x1="2" y1="12" x2="22" y2="12"/>
            <path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/>
          </svg>
        </div>
        <h3>Web Development</h3>
        <p>Beautiful, high-performing websites that convert visitors into customers and grow your business.</p>
        <div class="card-accent"></div>
      </div>
    </div>
  </div>
</header>

<style>
  :root {
    --primary-teal: #14B8A6;
    --secondary-teal: #0891B2;
    --dark-teal: #0F766E;
    --accent-orange: #FB923C;
    --accent-coral: #F97316;
    --electric-blue: #0EA5E9;
    --gradient-start: #14B8A6;
    --gradient-end: #0891B2;
    --white: #FFFFFF;
    --light-gray: #F8FAFC;
    --medium-gray: #64748B;
    --charcoal: #1E293B;
    --dark-charcoal: #0F172A;
    --font-primary: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    --font-heading: 'Poppins', var(--font-primary);
  }

  .hero-header {
    min-height: 100vh;
    background: linear-gradient(135deg, var(--gradient-start) 0%, var(--gradient-end) 50%, var(--dark-teal) 100%);
    color: var(--white);
    position: relative;
    overflow: hidden;
    width: 100vw;
    margin: 0;
    padding: 0;
  }

  .bg-animation {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    z-index: 1;
  }

  .floating-shape {
    position: absolute;
    border-radius: 50%;
    background: rgba(255, 255, 255, 0.1);
    animation: float 6s ease-in-out infinite;
  }

  .shape-1 {
    width: 100px;
    height: 100px;
    top: 20%;
    left: 10%;
    animation-delay: 0s;
  }

  .shape-2 {
    width: 60px;
    height: 60px;
    top: 60%;
    right: 15%;
    animation-delay: 2s;
  }

  .shape-3 {
    width: 80px;
    height: 80px;
    bottom: 20%;
    left: 70%;
    animation-delay: 4s;
  }

  @keyframes float {
    0%, 100% { transform: translateY(0) rotate(0deg); opacity: 0.7; }
    50% { transform: translateY(-20px) rotate(180deg); opacity: 1; }
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
    gap: 4rem;
    align-items: center;
    min-height: 100vh;
  }

  .logo-section {
    grid-area: logo;
    text-align: center;
    padding: 2rem 0;
    position: relative;
  }

  .logo-section::before {
    content: '';
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 85%;
    height: 120%;
    background: rgba(255, 255, 255, 0.08);
    backdrop-filter: blur(20px);
    border-radius: 30px;
    border: 1px solid rgba(255, 255, 255, 0.15);
    z-index: 1;
  }

  .hero-logo {
    width: 80%;
    height: auto;
    max-width: none;
    position: relative;
    z-index: 2;
    filter: 
      drop-shadow(0 8px 25px rgba(0, 0, 0, 0.4))
      drop-shadow(0 0 40px rgba(255, 255, 255, 0.2))
      brightness(1.1)
      contrast(1.1);
    transition: transform 0.4s ease;
  }

  .hero-logo:hover {
    transform: scale(1.02);
  }

  .logo-section:hover::before {
    background: rgba(255, 255, 255, 0.12);
    border-color: rgba(255, 255, 255, 0.25);
  }

  .hero-content {
    grid-area: content;
    text-align: center;
    max-width: 800px;
    margin: 0 auto;
  }

  .hero-title {
    font-family: var(--font-heading);
    font-size: clamp(2.5rem, 6vw, 5rem);
    font-weight: 800;
    line-height: 1.1;
    margin: 0 0 2rem 0;
    text-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
  }

  .gradient-text {
    background: linear-gradient(45deg, var(--accent-orange), var(--accent-coral), var(--electric-blue));
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-size: 300% 300%;
    animation: gradientShift 4s ease-in-out infinite;
  }

  @keyframes gradientShift {
    0%, 100% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
  }

  .hero-description {
    font-size: clamp(1.2rem, 2.5vw, 1.5rem);
    line-height: 1.7;
    color: rgba(255, 255, 255, 0.95);
    margin: 0 0 3rem 0;
    text-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
    font-weight: 400;
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
    gap: 0.5rem;
    padding: 1.25rem 2.5rem;
    font-size: 1.1rem;
    font-weight: 600;
    border-radius: 50px;
    text-decoration: none;
    transition: all 0.3s ease;
    border: 2px solid transparent;
    cursor: pointer;
    white-space: nowrap;
    min-width: 220px;
    position: relative;
    overflow: hidden;
  }

  .btn-primary {
    background: linear-gradient(45deg, var(--accent-orange), var(--accent-coral));
    color: var(--white);
    box-shadow: 0 10px 30px rgba(251, 146, 60, 0.4);
  }

  .btn-primary::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
    transition: left 0.5s ease;
  }

  .btn-primary:hover::before {
    left: 100%;
  }

  .btn-primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 15px 40px rgba(251, 146, 60, 0.5);
  }

  .btn-icon {
    width: 20px;
    height: 20px;
    transition: transform 0.3s ease;
  }

  .btn-primary:hover .btn-icon {
    transform: translateX(4px);
  }

  .btn-secondary {
    background: rgba(255, 255, 255, 0.1);
    color: var(--white);
    border-color: rgba(255, 255, 255, 0.3);
    backdrop-filter: blur(10px);
  }

  .btn-secondary:hover {
    background: rgba(255, 255, 255, 0.2);
    border-color: var(--white);
    transform: translateY(-3px);
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
  }

  .services-grid {
    grid-area: services;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
  }

  .service-card {
    background: rgba(255, 255, 255, 0.15);
    backdrop-filter: blur(20px);
    border: 1px solid rgba(255, 255, 255, 0.2);
    border-radius: 24px;
    padding: 3rem 2.5rem;
    text-align: center;
    transition: all 0.4s ease;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    position: relative;
    overflow: hidden;
  }

  .service-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
    background: linear-gradient(90deg, var(--accent-orange), var(--electric-blue));
  }

  .card-accent {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    height: 3px;
    background: linear-gradient(90deg, transparent, var(--accent-coral), transparent);
    opacity: 0;
    transition: opacity 0.3s ease;
  }

  .service-card:hover .card-accent {
    opacity: 1;
  }

  .service-card:hover {
    transform: translateY(-10px);
    background: rgba(255, 255, 255, 0.25);
    box-shadow: 0 25px 50px rgba(0, 0, 0, 0.15);
    border-color: rgba(255, 255, 255, 0.4);
  }

  .service-icon {
    width: 60px;
    height: 60px;
    margin: 0 auto 2rem;
    padding: 15px;
    background: linear-gradient(45deg, var(--accent-orange), var(--accent-coral));
    border-radius: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 8px 25px rgba(251, 146, 60, 0.3);
    transition: transform 0.3s ease;
  }

  .service-icon svg {
    width: 30px;
    height: 30px;
    color: var(--white);
    stroke-width: 2;
  }

  .service-card:hover .service-icon {
    transform: scale(1.1) rotateY(10deg);
  }

  .service-card h3 {
    font-family: var(--font-heading);
    font-size: 1.5rem;
    font-weight: 700;
    margin: 0 0 1.5rem 0;
    color: var(--white);
    text-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
  }

  .service-card p {
    color: rgba(255, 255, 255, 0.9);
    line-height: 1.7;
    margin: 0;
    font-size: 1.05rem;
    text-shadow: 0 1px 5px rgba(0, 0, 0, 0.2);
  }

  /* Enhanced Responsive Design */
  @media (max-width: 768px) {
    .hero-container {
      padding: 2rem 1rem;
      gap: 3rem;
    }

    .logo-section::before {
      width: 90%;
      height: 110%;
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
      max-width: 320px;
    }

    .services-grid {
      grid-template-columns: 1fr;
      gap: 1.5rem;
    }

    .service-card {
      padding: 2.5rem 2rem;
    }

    .floating-shape {
      display: none;
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

    .logo-section::before {
      width: 85%;
      height: 105%;
    }

    .hero-logo {
      width: 75%;
    }

    .services-grid {
      grid-template-columns: 1fr;
      margin-top: 0;
    }
  }

  @media (min-width: 1200px) {
    .logo-section::before {
      width: 80%;
      height: 100%;
    }

    .hero-logo {
      width: 70%;
    }

    .hero-container {
      padding: 5rem 4rem;
    }
  }
</style>