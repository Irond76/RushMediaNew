<script>
  import logoUrl from '$lib/assets/logo.png';
</script>

<svelte:head>
  <style>
    body, html {
      margin: 0 !important;
      padding: 0 !important;
      overflow-x: hidden;
    @media (min-width: 1200px) {
    .header-logo {
      width: 55%;
      max-width: 900px;
    }

    .word {
      font-size: 2.2rem;
    }
  }
  </style>
</svelte:head>

<header class="site-header">
  <!-- Animated Background Elements -->
  <div class="bg-animation">
    <div class="floating-shape shape-1"></div>
    <div class="floating-shape shape-2"></div>
    <div class="floating-shape shape-3"></div>
  </div>

  <div class="header-container">
    <!-- Logo Section -->
    <div class="logo-section">
      <img src={logoUrl} alt="Rush Media Tech" class="header-logo" />
      
      <!-- Animated Words -->
      <div class="animated-words">
        <span class="word word-1" data-text="Video">Video</span>
        <span class="word word-2" data-text="Media">Media</span>
        <span class="word word-3" data-text="Web">Web</span>
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

  .site-header {
    height: 40vh;
    min-height: 300px;
    background: linear-gradient(135deg, var(--gradient-start) 0%, var(--gradient-end) 50%, var(--dark-teal) 100%);
    color: var(--white);
    position: relative;
    overflow: hidden;
    width: 100vw;
    margin: 0;
    padding: 0;
    display: flex;
    align-items: center;
    justify-content: center;
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
    width: 80px;
    height: 80px;
    top: 20%;
    left: 15%;
    animation-delay: 0s;
  }

  .shape-2 {
    width: 50px;
    height: 50px;
    top: 60%;
    right: 20%;
    animation-delay: 2s;
  }

  .shape-3 {
    width: 60px;
    height: 60px;
    bottom: 25%;
    left: 70%;
    animation-delay: 4s;
  }

  @keyframes float {
    0%, 100% { transform: translateY(0) rotate(0deg); opacity: 0.7; }
    50% { transform: translateY(-15px) rotate(180deg); opacity: 1; }
  }

  .header-container {
    position: relative;
    z-index: 10;
    width: 100%;
    max-width: 1400px;
    margin: 0 auto;
    padding: 2rem;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .logo-section {
    text-align: center;
    width: 100%;
  }

  .header-logo {
    width: 70%;
    height: auto;
    max-width: 800px;
    position: relative;
    z-index: 2;
    filter: 
      drop-shadow(0 10px 30px rgba(0, 0, 0, 0.6))
      drop-shadow(0 0 60px rgba(255, 255, 255, 0.4))
      brightness(1.15)
      contrast(1.2)
      saturate(1.1);
    transition: transform 0.4s ease, filter 0.3s ease;
  }

  .header-logo:hover {
    transform: scale(1.02);
    filter: 
      drop-shadow(0 15px 40px rgba(0, 0, 0, 0.7))
      drop-shadow(0 0 80px rgba(255, 255, 255, 0.5))
      brightness(1.2)
      contrast(1.25)
      saturate(1.15);
  }

  .animated-words {
    margin-top: 2rem;
    display: flex;
    justify-content: center;
    gap: 3rem;
    flex-wrap: wrap;
  }

  .word {
    font-family: var(--font-heading);
    font-size: clamp(1.5rem, 4vw, 2.5rem);
    font-weight: 700;
    color: var(--white);
    text-shadow: 0 4px 15px rgba(0, 0, 0, 0.4);
    opacity: 0;
    transform: translateY(30px);
    animation: wordAppear 0.8s ease forwards;
    position: relative;
    cursor: default;
    transition: all 0.3s ease;
  }

  .word::before,
  .word::after {
    content: attr(data-text);
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    opacity: 0;
    pointer-events: none;
  }

  .word::before {
    color: rgba(255, 255, 255, 0.7);
    animation: fuzzyGlow 2s ease-in-out infinite;
    filter: blur(2px);
  }

  .word::after {
    color: rgba(255, 255, 255, 0.3);
    animation: fuzzyGlow 2s ease-in-out infinite reverse;
    filter: blur(4px);
  }

  .word:hover {
    transform: translateY(-5px);
    text-shadow: 
      0 0 10px rgba(255, 255, 255, 0.8),
      0 0 20px rgba(255, 255, 255, 0.6),
      0 0 30px rgba(255, 255, 255, 0.4);
    animation: textFuzzy 0.1s infinite;
  }

  .word-1 {
    animation-delay: 0.3s;
    color: #FFE0E6;
    text-shadow: 
      0 0 5px rgba(255, 224, 230, 0.8),
      0 4px 15px rgba(0, 0, 0, 0.4);
  }

  .word-2 {
    animation-delay: 0.6s;
    color: #E0F7FF;
    text-shadow: 
      0 0 5px rgba(224, 247, 255, 0.8),
      0 4px 15px rgba(0, 0, 0, 0.4);
  }

  .word-3 {
    animation-delay: 0.9s;
    color: #E8FFE8;
    text-shadow: 
      0 0 5px rgba(232, 255, 232, 0.8),
      0 4px 15px rgba(0, 0, 0, 0.4);
  }

  @keyframes wordAppear {
    from {
      opacity: 0;
      transform: translateY(30px) rotateX(90deg);
    }
    to {
      opacity: 1;
      transform: translateY(0) rotateX(0deg);
    }
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
    0% { transform: translateY(-5px) translateX(0); }
    20% { transform: translateY(-5px) translateX(-0.5px); }
    40% { transform: translateY(-5px) translateX(0.5px); }
    60% { transform: translateY(-5px) translateX(-0.3px); }
    80% { transform: translateY(-5px) translateX(0.3px); }
    100% { transform: translateY(-5px) translateX(0); }
  }

  /* Responsive Design */
  @media (max-width: 768px) {
    .site-header {
      height: 30vh;
      min-height: 250px;
    }

    .header-container {
      padding: 1.5rem;
    }

    .header-logo {
      width: 80%;
    }

    .animated-words {
      gap: 2rem;
      margin-top: 1.5rem;
    }

    .word {
      font-size: clamp(1.2rem, 5vw, 1.8rem);
    }
  }

    .floating-shape {
      display: none;
    }

  @media (min-width: 769px) and (max-width: 1024px) {
    .header-logo {
      width: 65%;
    }
  }

  @media (min-width: 1025px) {
    .site-header {
      height: 45vh;
      min-height: 350px;
    }

    .header-logo {
      width: 60%;
    }

    .animated-words {
      gap: 4rem;
    }
  }
</style>