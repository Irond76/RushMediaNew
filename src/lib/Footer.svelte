<script>
  import logoUrl from '$lib/assets/logo.png';
  
  // Get current year dynamically
  const currentYear = new Date().getFullYear();
</script>

<footer class="site-footer">
  <div class="footer-container">
    <div class="footer-content">
      <span class="powered-by" data-text="Powered By">Powered By</span>
      <img src={logoUrl} alt="Rush Media Tech" class="footer-logo" />
      <span class="copyright">© {currentYear} Rush Media Tech. All rights reserved.</span>
    </div>
  </div>
</footer>

<style>
  :root {
    --primary-teal: #14B8A6;
    --secondary-teal: #0891B2;
    --dark-teal: #0F766E;
    --white: #FFFFFF;
    --light-gray: #F8FAFC;
    --medium-gray: #64748B;
    --charcoal: #1E293B;
    --dark-charcoal: #0F172A;
    --font-primary: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    --font-heading: 'Poppins', var(--font-primary);
  }

  .site-footer {
    background: linear-gradient(135deg, var(--primary-teal) 0%, var(--secondary-teal) 50%, var(--dark-teal) 100%);
    color: var(--white);
    padding: 2rem 0;
    position: relative;
    overflow: hidden;
    margin-top: auto;
  }

  .site-footer::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: 
      radial-gradient(circle at 30% 20%, rgba(255, 255, 255, 0.1) 0%, transparent 50%),
      radial-gradient(circle at 70% 80%, rgba(255, 255, 255, 0.05) 0%, transparent 50%);
    pointer-events: none;
  }

  .footer-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
    position: relative;
    z-index: 10;
  }

  .footer-content {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1.5rem;
    flex-wrap: wrap;
  }

  .powered-by {
    font-family: var(--font-heading);
    font-size: 1.1rem;
    font-weight: 600;
    color: rgba(255, 255, 255, 0.9);
    text-shadow: 0 2px 8px rgba(0, 0, 0, 0.3);
    position: relative;
    cursor: default;
    transition: all 0.3s ease;
  }

  .powered-by::before,
  .powered-by::after {
    content: attr(data-text);
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0;
    pointer-events: none;
  }

  .powered-by::before {
    color: rgba(255, 255, 255, 0.7);
    animation: fuzzyGlow 3s ease-in-out infinite;
    filter: blur(2px);
  }

  .powered-by::after {
    color: rgba(255, 255, 255, 0.4);
    animation: fuzzyGlow 3s ease-in-out infinite reverse;
    filter: blur(4px);
  }

  .powered-by:hover {
    text-shadow: 
      0 0 10px rgba(255, 255, 255, 0.8),
      0 0 20px rgba(255, 255, 255, 0.6),
      0 0 30px rgba(255, 255, 255, 0.4);
    animation: textFuzzy 0.1s infinite;
  }

  @keyframes fuzzyGlow {
    0%, 100% { 
      opacity: 0;
      transform: scale(1);
    }
    50% { 
      opacity: 0.6;
      transform: scale(1.02);
    }
  }

  @keyframes textFuzzy {
    0% { transform: translateX(0); }
    20% { transform: translateX(-0.5px); }
    40% { transform: translateX(0.5px); }
    60% { transform: translateX(-0.3px); }
    80% { transform: translateX(0.3px); }
    100% { transform: translateX(0); }
  }

  .footer-logo {
    height: 40px;
    width: auto;
    filter: 
      drop-shadow(0 6px 20px rgba(0, 0, 0, 0.6))
      drop-shadow(0 0 30px rgba(255, 255, 255, 0.4))
      drop-shadow(0 2px 8px rgba(0, 0, 0, 0.8))
      brightness(1.2)
      contrast(1.15)
      saturate(1.1);
    transition: transform 0.3s ease, filter 0.3s ease;
  }

  .footer-logo:hover {
    transform: scale(1.05);
    filter: 
      drop-shadow(0 8px 25px rgba(0, 0, 0, 0.7))
      drop-shadow(0 0 40px rgba(255, 255, 255, 0.5))
      drop-shadow(0 4px 12px rgba(0, 0, 0, 0.9))
      brightness(1.25)
      contrast(1.2)
      saturate(1.15);
  }

  .copyright {
    font-family: var(--font-primary);
    font-size: 0.9rem;
    font-weight: 400;
    color: rgba(255, 255, 255, 0.8);
    text-shadow: 0 1px 3px rgba(0, 0, 0, 0.3);
  }

  /* Responsive Design */
  @media (max-width: 768px) {
    .site-footer {
      padding: 1.5rem 0;
    }

    .footer-content {
      flex-direction: column;
      gap: 1rem;
      text-align: center;
    }

    .footer-logo {
      height: 35px;
    }

    .powered-by {
      font-size: 1rem;
    }

    .copyright {
      font-size: 0.8rem;
    }
  }

  @media (max-width: 480px) {
    .footer-content {
      gap: 0.8rem;
    }

    .footer-logo {
      height: 30px;
    }

    .powered-by {
      font-size: 0.9rem;
    }

    .copyright {
      font-size: 0.75rem;
      line-height: 1.4;
    }
  }
</style>