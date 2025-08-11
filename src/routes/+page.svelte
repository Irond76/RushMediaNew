<!-- Homepage Hero Content -->
<section class="hero-content-section">
  <div class="hero-container">
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
        <a href="mailto:dale@rushmediatech.com?subject=New Project Inquiry&body=Hi Dale,%0D%0A%0D%0AI'm interested in discussing a new project with Rush Media Tech. Please let me know when we can schedule a time to talk.%0D%0A%0D%0AThank you!" class="btn-primary btn-single">
          <span>Start Your Project</span>
          <svg class="btn-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor">
            <path d="M5 12h14M12 5l7 7-7 7"/>
          </svg>
        </a>
      </div>
    </div>
    
    <!-- Enhanced Services Grid -->
    <div class="services-grid">
      <a href="/Visual-Content" class="service-card card-1">
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
      </a>
      
      <a href="/Video-Production" class="service-card card-2">
        <div class="service-icon">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor">
            <polygon points="23 7 16 12 23 17 23 7"/>
            <rect x="1" y="5" width="15" height="14" rx="2" ry="2"/>
          </svg>
        </div>
        <h3>Video Production</h3>
        <p>From corporate training to promotional content, we bring your story to life with compelling video.</p>
        <div class="card-accent"></div>
      </a>
      
      <a href="/Web-Development" class="service-card card-3">
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
      </a>
    </div>
  </div>
</section>

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

  .hero-content-section {
    background: var(--white);
    color: var(--charcoal);
    padding: 4rem 0 6rem;
    position: relative;
  }

  .hero-content-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 100px;
    background: linear-gradient(180deg, rgba(20, 184, 166, 0.05) 0%, transparent 100%);
    pointer-events: none;
  }

  .hero-container {
    max-width: 1400px;
    margin: 0 auto;
    padding: 0 2rem;
    display: grid;
    grid-template-areas: 
      "content"
      "services";
    gap: 4rem;
    align-items: start;
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
    font-weight: 800;
    line-height: 1.1;
    margin: 0 0 2rem 0;
    color: var(--charcoal);
  }

  .gradient-text {
    background: linear-gradient(45deg, var(--primary-teal), var(--accent-coral));
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
    font-size: clamp(1.2rem, 2.5vw, 1.4rem);
    line-height: 1.7;
    color: var(--medium-gray);
    margin: 0 0 3rem 0;
    font-weight: 400;
  }

  .hero-buttons {
    display: flex;
    justify-content: center;
    margin-bottom: 2rem;
  }

  .btn-primary {
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
    position: relative;
    overflow: hidden;
    background: linear-gradient(45deg, var(--accent-orange), var(--accent-coral));
    color: var(--white);
    box-shadow: 0 10px 30px rgba(251, 146, 60, 0.4);
  }

  .btn-single {
    min-width: 280px;
    padding: 1.5rem 3rem;
    font-size: 1.2rem;
    font-weight: 700;
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

  .services-grid {
    grid-area: services;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 2rem;
  }

  .service-card {
    background: var(--white);
    border: 2px solid var(--light-gray);
    border-radius: 24px;
    padding: 3rem 2.5rem;
    text-align: center;
    transition: all 0.4s ease;
    box-shadow: 0 8px 25px rgba(45, 55, 72, 0.08);
    position: relative;
    overflow: hidden;
    text-decoration: none;
    color: inherit;
    display: block;
    cursor: pointer;
  }

  .service-card:visited {
    color: inherit;
  }

  .service-card:focus {
    outline: 3px solid var(--accent-orange);
    outline-offset: 2px;
  }

  .service-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
    background: linear-gradient(90deg, var(--primary-teal), var(--accent-coral));
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
    transform: translateY(-8px);
    background: var(--white);
    box-shadow: 0 20px 40px rgba(45, 55, 72, 0.12);
    border-color: var(--primary-teal);
  }

  .service-card:active {
    transform: translateY(-6px);
  }

  .service-icon {
    width: 60px;
    height: 60px;
    margin: 0 auto 2rem;
    padding: 15px;
    background: linear-gradient(45deg, var(--primary-teal), var(--accent-coral));
    border-radius: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 8px 25px rgba(20, 184, 166, 0.3);
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
    color: var(--charcoal);
  }

  .service-card p {
    color: var(--medium-gray);
    line-height: 1.7;
    margin: 0;
    font-size: 1.05rem;
  }

  /* Enhanced Responsive Design */
  @media (max-width: 768px) {
    .hero-content-section {
      padding: 3rem 0 4rem;
    }

    .hero-container {
      padding: 0 1rem;
      gap: 3rem;
    }

    .btn-single {
      width: 100%;
      max-width: 350px;
    }

    .services-grid {
      grid-template-columns: 1fr;
      gap: 1.5rem;
    }

    .service-card {
      padding: 2.5rem 2rem;
    }
  }

  @media (min-width: 1024px) {
    .hero-container {
      grid-template-areas: 
        "content content"
        "services services";
      grid-template-columns: 1fr 1fr;
      gap: 4rem;
      padding: 0 3rem;
    }

    .hero-content {
      grid-area: content;
    }

    .services-grid {
      grid-area: services;
    }
  }

  @media (min-width: 1200px) {
    .hero-container {
      padding: 0 4rem;
    }
  }
</style>
