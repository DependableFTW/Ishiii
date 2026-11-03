<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ayush & Ishika — Our Journey of Memories & Love</title>
  
  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  
  <!-- Fonts: Cormorant Garamond & Plus Jakarta Sans -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;0,700;1,300;1,400;1,600&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  
  <!-- Phosphor Icons -->
  <script src="https://unpkg.com/@phosphor-icons/web"></script>

  <!-- Canvas Confetti Library for Smooth Celebrations -->
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.9.3/dist/confetti.browser.min.js"></script>

  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          colors: {
            obsidian: '#0a0508',
            nightVelvet: '#14080e',
            crimsonVelvet: '#871228',
            crimsonGlow: '#e83e5c',
            champagne: '#d4af37',
            champagneLight: '#fae392',
            roseMist: '#f4cac3',
            pearlWhite: '#fdfbf7'
          },
          fontFamily: {
            serif: ['"Cormorant Garamond"', 'serif'],
            sans: ['"Plus Jakarta Sans"', 'sans-serif'],
          },
          animation: {
            'float-gentle': 'float 6s ease-in-out infinite',
            'pulse-glow': 'pulseGlow 3s ease-in-out infinite',
          },
          keyframes: {
            float: {
              '0%, 100%': { transform: 'translateY(0px)' },
              '50%': { transform: 'translateY(-8px)' },
            },
            pulseGlow: {
              '0%, 100%': { opacity: '0.4', transform: 'scale(1)' },
              '50%': { opacity: '0.8', transform: 'scale(1.05)' },
            }
          }
        }
      }
    }
  </script>

  <style>
    /* Custom Scrollbar */
    ::-webkit-scrollbar { width: 7px; }
    ::-webkit-scrollbar-track { background: #0a0508; }
    ::-webkit-scrollbar-thumb { background: #2b111b; border-radius: 9999px; }
    ::-webkit-scrollbar-thumb:hover { background: #d4af37; }

    .glass-surface {
      background: rgba(20, 8, 14, 0.78);
      backdrop-filter: blur(20px);
      -webkit-backdrop-filter: blur(20px);
      border: 1px solid rgba(212, 175, 55, 0.2);
      box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.7), inset 0 1px 1px rgba(255, 255, 255, 0.08);
    }
    
    .glass-surface-lock {
      background: rgba(12, 5, 9, 0.92);
      backdrop-filter: blur(24px);
      -webkit-backdrop-filter: blur(24px);
      border: 1px dashed rgba(212, 175, 55, 0.35);
    }

    .radial-glow {
      position: absolute;
      border-radius: 50%;
      filter: blur(110px);
      pointer-events: none;
      z-index: 0;
    }

    /* 3D Envelope Flip Card */
    .envelope-3d-wrap { perspective: 1200px; }
    .envelope-card {
      transition: transform 0.85s cubic-bezier(0.34, 1.56, 0.64, 1);
      transform-style: preserve-3d;
    }
    .envelope-card.is-open { transform: rotateY(180deg); }
    .envelope-front, .envelope-back {
      backface-visibility: hidden;
      -webkit-backface-visibility: hidden;
    }
    .envelope-back { transform: rotateY(180deg); }
  </style>
</head>

<body class="bg-obsidian text-pearlWhite font-sans antialiased selection:bg-champagne selection:text-obsidian min-h-screen overflow-x-hidden relative">

  <!-- MASTER PRIVACY LOCK SCREEN (PREVENTS STRANGERS FROM VIEWING) -->
  <div id="masterPrivacyScreen" class="fixed inset-0 z-[100] bg-obsidian flex flex-col items-center justify-center px-4 transition-all duration-700">
    <div class="glass-surface-lock max-w-md w-full p-8 sm:p-10 rounded-3xl border border-champagne/40 text-center relative shadow-2xl">
      <!-- Wax seal badge -->
      <div class="w-20 h-20 rounded-full bg-gradient-to-tr from-crimsonVelvet via-crimsonGlow to-champagne mx-auto flex items-center justify-center text-pearlWhite text-3xl shadow-xl shadow-crimsonVelvet/50 border border-champagne/40 mb-5 animate-pulse-glow">
        <i class="ph-fill ph-lock-key"></i>
      </div>
      
      <span class="text-[11px] uppercase tracking-widest text-champagne font-semibold font-mono">Private & Confidential</span>
      <h2 class="font-serif text-3xl sm:text-4xl text-pearlWhite mt-1 mb-3">Only For Ishika</h2>
      <p class="text-xs sm:text-sm text-pearlWhite/70 font-serif italic mb-6">
        "This sanctuary of memories was built for one person only. Enter the master key to enter."
      </p>

      <div class="space-y-3">
        <div class="relative">
          <input type="password" id="masterPasscodeInput" placeholder="Enter secret key..." class="w-full bg-nightVelvet/90 border border-pearlWhite/20 focus:border-champagne rounded-xl px-4 py-3.5 text-sm text-pearlWhite text-center tracking-widest focus:outline-none transition-colors" onkeydown="if(event.key === 'Enter') unlockMasterPrivacy()">
        </div>
        <button onclick="unlockMasterPrivacy()" class="w-full py-3 rounded-xl bg-gradient-to-r from-champagne via-champagneLight to-champagne text-obsidian font-bold text-xs uppercase tracking-wider hover:scale-[1.02] active:scale-95 transition-all shadow-lg shadow-champagne/20 flex items-center justify-center gap-2">
          <i class="ph-bold ph-key"></i>
          <span>Open My Sanctuary</span>
        </button>
        <div id="masterPassFeedback" class="text-xs font-semibold min-h-[1.25rem]"></div>
      </div>

      <p class="text-[10px] text-pearlWhite/40 mt-4 tracking-wider uppercase font-mono">
        Authorized Access Only • 04-11-2026
      </p>
    </div>
  </div>

  <!-- Floating Canvas Particles (Rose Petals & Golden Stardust) -->
  <canvas id="starsCanvas" class="fixed inset-0 pointer-events-none z-0"></canvas>

  <!-- Ambient Ambient Lighting Orbs -->
  <div class="radial-glow w-96 h-96 bg-crimsonVelvet/30 top-[-60px] left-[-100px] animate-pulse-glow"></div>
  <div class="radial-glow w-[34rem] h-[34rem] bg-champagne/15 top-[35%] right-[-140px] animate-pulse-glow"></div>
  <div class="radial-glow w-96 h-96 bg-purple-950/30 bottom-10 left-[-80px]"></div>

  <!-- STICKY TOP HUD: PROGRESS & MASTER UNLOCK ALL -->
  <header class="fixed top-3 sm:top-5 inset-x-0 mx-auto w-[94%] max-w-5xl z-50">
    <div class="glass-surface px-4 sm:px-6 py-2.5 rounded-full flex items-center justify-between transition-all">
      
      <!-- Monogram -->
      <a href="#hero" class="flex items-center gap-2 group">
        <div class="w-8 h-8 rounded-full bg-gradient-to-tr from-champagne via-crimsonGlow to-crimsonVelvet flex items-center justify-center text-obsidian shadow-md group-hover:scale-105 transition-transform">
          <i class="ph-fill ph-heart text-sm text-pearlWhite"></i>
        </div>
        <span class="font-serif tracking-widest text-base sm:text-lg font-medium text-transparent bg-clip-text bg-gradient-to-r from-pearlWhite via-champagneLight to-champagne">
          Ayush & Ishika
        </span>
      </a>

      <!-- Visual Quest Tracker (Chapter 1 to 4) -->
      <div class="hidden md:flex items-center gap-2 text-xs tracking-wider">
        <div id="progChip1" class="flex items-center gap-1 px-2.5 py-1 rounded-full bg-obsidian border border-pearlWhite/10 text-pearlWhite/40 transition-all">
          <i class="ph-bold ph-lock text-[10px]"></i><span>Ch. 1 Video</span>
        </div>
        <div id="progChip2" class="flex items-center gap-1 px-2.5 py-1 rounded-full bg-obsidian border border-pearlWhite/10 text-pearlWhite/40 transition-all">
          <i class="ph-bold ph-lock text-[10px]"></i><span>Ch. 2 Poem</span>
        </div>
        <div id="progChip3" class="flex items-center gap-1 px-2.5 py-1 rounded-full bg-obsidian border border-pearlWhite/10 text-pearlWhite/40 transition-all">
          <i class="ph-bold ph-lock text-[10px]"></i><span>Ch. 3 Edits</span>
        </div>
        <div id="progChip4" class="flex items-center gap-1 px-2.5 py-1 rounded-full bg-obsidian border border-pearlWhite/10 text-pearlWhite/40 transition-all">
          <i class="ph-bold ph-lock text-[10px]"></i><span>Ch. 4 Letter</span>
        </div>
      </div>

      <!-- Controls & Master Unlock Key -->
      <div class="flex items-center gap-2">
        <!-- Audio Synthesizer Toggle -->
        <button id="audioToggleBtn" title="Play Romantic Melody" class="px-3 py-1.5 rounded-full text-xs font-medium border border-champagne/40 bg-nightVelvet/70 text-champagneLight hover:bg-champagne hover:text-obsidian transition-all flex items-center gap-1.5 shadow-sm">
          <i id="audioIcon" class="ph-bold ph-speaker-simple-slash text-sm"></i>
          <span id="audioLabel" class="hidden sm:inline">Music</span>
        </button>

        <!-- Confetti Heart Trigger -->
        <button onclick="triggerPetalConfetti()" title="Shower of Love" class="w-8 h-8 rounded-full bg-crimsonVelvet/40 border border-crimsonGlow/40 text-crimsonGlow hover:bg-crimsonGlow hover:text-white flex items-center justify-center transition-all text-sm">
          <i class="ph-fill ph-heart"></i>
        </button>
      </div>
    </div>
  </header>

  <!-- ================= MAIN CONTENT ================= -->
  <main class="relative z-10">

    <!-- HERO SECTION -->
    <section id="hero" class="min-h-screen flex flex-col items-center justify-center text-center px-4 pt-28 pb-16 relative">
      <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full border border-champagne/30 bg-champagne/10 text-champagneLight text-xs tracking-widest uppercase font-medium mb-6 animate-float-gentle">
        <i class="ph-fill ph-sparkle text-champagne"></i>
        <span>A Journey of Memories & Love — For Ishika</span>
        <i class="ph-fill ph-sparkle text-champagne"></i>
      </div>

      <h1 class="font-serif text-4xl sm:text-6xl md:text-7xl lg:text-8xl font-normal tracking-tight text-pearlWhite max-w-4xl leading-[1.08] mb-6">
        To Unlock My Heart, <br>
        <span class="italic font-light text-transparent bg-clip-text bg-gradient-to-r from-champagneLight via-roseMist to-crimsonGlow">
          Answer Our Memories.
        </span>
      </h1>

      <p class="text-pearlWhite/75 text-base sm:text-lg md:text-xl font-light max-w-2xl leading-relaxed mb-8">
        Every milestone in our story holds a sacred key. Enter the secret memories we both carry in our hearts to reveal each chapter.
      </p>

      <!-- Overall Unlock Quest Progress Card -->
      <div class="w-full max-w-md glass-surface rounded-2xl p-5 mb-8 border border-champagne/25">
        <div class="flex items-center justify-between text-xs uppercase tracking-wider mb-2">
          <span class="text-pearlWhite/70 font-medium">Chapters Unlocked</span>
          <span id="progressText" class="text-champagneLight font-bold">0 / 4 Unlocked</span>
        </div>
        <div class="w-full h-2.5 bg-obsidian rounded-full overflow-hidden border border-pearlWhite/10 p-0.5">
          <div id="questProgressBar" class="h-full bg-gradient-to-r from-crimsonGlow via-roseMist to-champagne rounded-full w-0 transition-all duration-700 ease-out"></div>
        </div>
      </div>

      <!-- Action Buttons -->
      <div class="flex items-center justify-center">
        <a href="#chapter-1" class="px-8 py-3.5 rounded-full bg-gradient-to-r from-champagne to-champagneLight text-obsidian font-semibold text-sm tracking-wide shadow-lg shadow-champagne/20 hover:scale-105 transition-all flex items-center gap-2">
          <i class="ph-fill ph-lock-key"></i>
          <span>Begin With Chapter One</span>
        </a>
      </div>
    </section>

    <!-- CHAPTER 1: THE MAIN RECORDED VIDEO -->
    <section id="chapter-1" class="py-20 px-4 sm:px-6 max-w-5xl mx-auto scroll-mt-24">
      <div class="flex items-center justify-between mb-8">
        <div>
          <span class="text-xs uppercase tracking-widest text-champagne font-semibold flex items-center gap-1.5 mb-1">
            <i class="ph-fill ph-number-circle-one"></i> Chapter One
          </span>
          <h2 class="font-serif text-3xl sm:text-4xl text-pearlWhite">The Recorded Film</h2>
        </div>
        <div id="statusBadge1" class="px-3 py-1 rounded-full text-xs font-medium border border-roseMist/20 text-roseMist bg-nightVelvet flex items-center gap-1.5">
          <i class="ph-bold ph-lock text-xs"></i> <span>Locked</span>
        </div>
      </div>

      <div class="relative rounded-3xl overflow-hidden min-h-[380px] transition-all duration-700" id="cardContainer1">
        
        <!-- LOCKED OVERLAY VIEW (STRICT INPUT LOCK) -->
        <div id="lockView1" class="glass-surface-lock p-8 sm:p-14 text-center rounded-3xl flex flex-col items-center justify-center min-h-[380px]">
          <div class="w-16 h-16 rounded-full bg-crimsonVelvet/30 border border-crimsonGlow/40 flex items-center justify-center text-champagneLight text-2xl mb-4 shadow-inner animate-pulse-glow">
            <i class="ph-fill ph-film-strip"></i>
          </div>
          <h3 class="font-serif text-2xl sm:text-3xl text-pearlWhite mb-2">A Film Recorded Only For You</h3>
          <p class="text-champagneLight font-serif italic text-base sm:text-lg max-w-lg mb-6">
            "What was the date when we went on our 1st Movie date? 🎬"
          </p>

          <!-- Strict Answer Form -->
          <div class="w-full max-w-md space-y-3">
            <div class="relative">
              <input type="text" id="answerInput1" placeholder="Type our special date..." class="w-full bg-obsidian/90 border border-pearlWhite/20 focus:border-champagne rounded-xl px-4 py-3 text-sm text-pearlWhite pr-24 focus:outline-none transition-colors" onkeydown="if(event.key === 'Enter') submitDirectAnswer(1)">
              <button onclick="submitDirectAnswer(1)" class="absolute right-1.5 top-1.5 bottom-1.5 px-4 rounded-lg bg-gradient-to-r from-champagne to-champagneLight text-obsidian text-xs font-bold hover:scale-105 transition-transform flex items-center gap-1 shadow-sm">
                <i class="ph-bold ph-key"></i>
                <span>Unlock</span>
              </button>
            </div>
            
            <div id="feedbackText1" class="text-xs font-medium min-h-[1.25rem]"></div>

            <div class="pt-1">
              <button onclick="toggleHint(1)" class="text-xs text-pearlWhite/60 hover:text-champagneLight underline flex items-center justify-center gap-1 mx-auto transition-colors">
                <i class="ph-bold ph-lightbulb"></i>
                <span>Need a hint?</span>
              </button>
              <p id="hintBox1" class="text-xs text-roseMist bg-nightVelvet/80 p-3 rounded-xl border border-roseMist/30 italic mt-3 hidden text-center transition-all">
                "If you don't get this, call me and say 'I Love You, I forgot the date, I owe you 1 Movie Date' 🎬❤️"
              </p>
            </div>
          </div>
        </div>

        <!-- UNLOCKED VIEW: THE VIDEO PLAYER -->
        <div id="unlockedView1" class="hidden glass-surface rounded-3xl p-4 sm:p-6 border border-champagne/30">
          <div class="flex flex-col sm:flex-row sm:items-center justify-between pb-4 border-b border-pearlWhite/10 mb-4 gap-3">
            <div class="flex items-center gap-2">
              <span class="w-2.5 h-2.5 rounded-full bg-emerald-400 animate-pulse"></span>
              <span class="font-serif text-lg text-pearlWhite" id="mainVideoHeading">For Ishika — The One I Chose & Choose Today</span>
            </div>
            <!-- Video Switcher Controls -->
            <button onclick="document.getElementById('videoUploadModal').classList.remove('hidden')" class="px-3.5 py-1.5 rounded-xl bg-champagne/15 hover:bg-champagne/25 text-champagneLight text-xs flex items-center gap-1.5 border border-champagne/30 transition-colors self-start sm:self-auto">
              <i class="ph-bold ph-video-camera"></i>
              <span>Switch / Re-load Video</span>
            </button>
          </div>

          <!-- Video Container (Google Drive Streaming Player) -->
          <div class="relative aspect-video rounded-2xl overflow-hidden bg-black shadow-2xl border border-pearlWhite/10 group">
            <iframe id="heroDriveIframe" class="w-full h-full border-0" src="https://drive.google.com/file/d/1TN3WOetxS9yxB4nBJoNv7jm1yrp7lemv/preview?autoplay=1" allow="autoplay; fullscreen" allowfullscreen></iframe>
            <video id="heroVideoElement" class="w-full h-full object-contain cursor-pointer hidden" playsinline controls preload="metadata">
              <source id="heroVideoSource" src="" type="video/mp4">
              Your browser does not support video playback.
            </video>
          </div>

          <p class="text-xs text-pearlWhite/50 mt-3 italic text-center">
            Streaming directly from your Google Drive for Ishika.
          </p>
        </div>

      </div>
    </section>

    <!-- CHAPTER 2: THE POETRY MANUSCRIPT -->
    <section id="chapter-2" class="py-20 px-4 sm:px-6 max-w-5xl mx-auto scroll-mt-24">
      <div class="flex items-center justify-between mb-8">
        <div>
          <span class="text-xs uppercase tracking-widest text-champagne font-semibold flex items-center gap-1.5 mb-1">
            <i class="ph-fill ph-number-circle-two"></i> Chapter Two
          </span>
          <h2 class="font-serif text-3xl sm:text-4xl text-pearlWhite">Our Story — A Poem for Ishika</h2>
        </div>
        <div id="statusBadge2" class="px-3 py-1 rounded-full text-xs font-medium border border-roseMist/20 text-roseMist bg-nightVelvet flex items-center gap-1.5">
          <i class="ph-bold ph-lock text-xs"></i> <span>Locked</span>
        </div>
      </div>

      <div class="relative rounded-3xl overflow-hidden min-h-[380px] transition-all duration-700" id="cardContainer2">
        
        <!-- LOCKED OVERLAY VIEW (STRICT INPUT LOCK) -->
        <div id="lockView2" class="glass-surface-lock p-8 sm:p-14 text-center rounded-3xl flex flex-col items-center justify-center min-h-[380px]">
          <div class="w-16 h-16 rounded-full bg-crimsonVelvet/30 border border-crimsonGlow/40 flex items-center justify-center text-champagneLight text-2xl mb-4 shadow-inner animate-pulse-glow">
            <i class="ph-fill ph-feather"></i>
          </div>
          <h3 class="font-serif text-2xl sm:text-3xl text-pearlWhite mb-2">13 Chapters Written With All My Heart</h3>
          <p class="text-champagneLight font-serif italic text-base sm:text-lg max-w-lg mb-6">
            "What was the First thing I ever ordered for you, without even asking you, whether you want or not? 🍹"
          </p>

          <!-- Strict Answer Form -->
          <div class="w-full max-w-md space-y-3">
            <div class="relative">
              <input type="text" id="answerInput2" placeholder="Type your answer here..." class="w-full bg-obsidian/90 border border-pearlWhite/20 focus:border-champagne rounded-xl px-4 py-3 text-sm text-pearlWhite pr-24 focus:outline-none transition-colors" onkeydown="if(event.key === 'Enter') submitDirectAnswer(2)">
              <button onclick="submitDirectAnswer(2)" class="absolute right-1.5 top-1.5 bottom-1.5 px-4 rounded-lg bg-gradient-to-r from-champagne to-champagneLight text-obsidian text-xs font-bold hover:scale-105 transition-transform flex items-center gap-1 shadow-sm">
                <i class="ph-bold ph-key"></i>
                <span>Unlock</span>
              </button>
            </div>
            
            <div id="feedbackText2" class="text-xs font-medium min-h-[1.25rem]"></div>

            <div class="pt-1">
              <button onclick="toggleHint(2)" class="text-xs text-pearlWhite/60 hover:text-champagneLight underline flex items-center justify-center gap-1 mx-auto transition-colors">
                <i class="ph-bold ph-lightbulb"></i>
                <span>Need a hint?</span>
              </button>
              <p id="hintBox2" class="text-xs text-roseMist bg-nightVelvet/80 p-3 rounded-xl border border-roseMist/30 italic mt-3 hidden text-center transition-all">
                "If you need answer, You need to give me Sandwich! 🥪🍍"
              </p>
            </div>
          </div>
        </div>

        <!-- UNLOCKED VIEW: COMPLETE 13-CHAPTER POETRY MANUSCRIPT -->
        <div id="unlockedView2" class="hidden glass-surface rounded-3xl p-5 sm:p-10 border border-champagne/30 text-left relative">
          
          <!-- Top Header & Reading Toolbar -->
          <div class="flex flex-col md:flex-row md:items-center justify-between pb-6 border-b border-pearlWhite/10 gap-4">
            <div>
              <span class="text-[11px] uppercase tracking-widest text-champagne font-semibold flex items-center gap-1.5">
                <i class="ph-fill ph-book-open-text"></i> Complete 13 Chapters
              </span>
              <h3 class="font-serif text-2xl sm:text-3xl text-pearlWhite mt-1">Our Story — A Poem for Ishika</h3>
              <p class="text-xs text-pearlWhite/50 font-serif italic">"Written with all my heart — for Ishika"</p>
            </div>

            <!-- Reading Toolbar: Jump chapter, font size, ambient read -->
            <div class="flex items-center flex-wrap gap-2">
              <div class="relative">
                <select id="chapterNavSelect" onchange="jumpToChapter(this.value)" class="bg-nightVelvet border border-champagne/30 text-champagneLight text-xs rounded-xl px-3 py-2 pr-7 appearance-none focus:outline-none focus:border-champagne cursor-pointer">
                  <option value="section-intro">Opening Reflection</option>
                  <option value="section-ch1">Ch. I: 12th Grade Gaze</option>
                  <option value="section-ch2">Ch. II: Farewell Photograph</option>
                  <option value="section-ch3">Ch. III: The Glowing Screen</option>
                  <option value="section-ch4">Ch. IV: Endless Nights</option>
                  <option value="section-ch5">Ch. V: The Unspoken Weight</option>
                  <option value="section-ch6">Ch. VI: Crossing The Line</option>
                  <option value="section-ch7">Ch. VII: November Storm</option>
                  <option value="section-ch8">Ch. VIII: Clashing & Trusting</option>
                  <option value="section-ch9">Ch. IX: Phir Kya Hua?</option>
                  <option value="section-ch10">Ch. X: College Gates & 2025</option>
                  <option value="section-ch11">Ch. XI: Zoroko & First Kiss</option>
                  <option value="section-ch12">Ch. XII: Indore Evenings</option>
                  <option value="section-ch13">Ch. XIII: Forever Yours</option>
                </select>
                <i class="ph-bold ph-caret-down text-[10px] text-champagne absolute right-2.5 top-3 pointer-events-none"></i>
              </div>

              <!-- Font Size Buttons -->
              <div class="flex items-center border border-pearlWhite/15 rounded-xl overflow-hidden bg-obsidian/60">
                <button onclick="adjustPoemFontSize(-1)" title="Smaller text" class="px-2.5 py-1.5 text-xs text-pearlWhite/70 hover:text-champagne transition-colors">A-</button>
                <button onclick="adjustPoemFontSize(1)" title="Larger text" class="px-2.5 py-1.5 text-xs text-pearlWhite/70 hover:text-champagne transition-colors">A+</button>
              </div>

              <!-- Ambient Melody Toggle -->
              <button onclick="document.getElementById('audioToggleBtn').click()" class="px-3 py-1.5 rounded-xl border border-roseMist/30 bg-crimsonVelvet/20 text-roseMist hover:bg-crimsonVelvet/40 text-xs flex items-center gap-1.5 transition-all">
                <i class="ph-fill ph-music-notes"></i>
                <span class="hidden sm:inline">Soft Melody</span>
              </button>
            </div>
          </div>

          <!-- Quick Navigation Pill Bar -->
          <div class="flex items-center gap-2 overflow-x-auto py-3.5 no-scrollbar border-b border-pearlWhite/5 text-[11px] text-pearlWhite/60 whitespace-nowrap">
            <span class="text-champagne font-semibold text-[10px] uppercase tracking-wider pr-1">Jump to:</span>
            <button onclick="jumpToChapter('section-intro')" class="px-2.5 py-1 rounded-full bg-obsidian/70 hover:text-champagne hover:bg-nightVelvet border border-pearlWhite/10 transition-colors">Intro</button>
            <button onclick="jumpToChapter('section-ch1')" class="px-2.5 py-1 rounded-full bg-obsidian/70 hover:text-champagne hover:bg-nightVelvet border border-pearlWhite/10 transition-colors">I. Gaze</button>
            <button onclick="jumpToChapter('section-ch2')" class="px-2.5 py-1 rounded-full bg-obsidian/70 hover:text-champagne hover:bg-nightVelvet border border-pearlWhite/10 transition-colors">II. Farewell</button>
            <button onclick="jumpToChapter('section-ch6')" class="px-2.5 py-1 rounded-full bg-obsidian/70 hover:text-champagne hover:bg-nightVelvet border border-pearlWhite/10 transition-colors">VI. Confession</button>
            <button onclick="jumpToChapter('section-ch9')" class="px-2.5 py-1 rounded-full bg-obsidian/70 hover:text-champagne hover:bg-nightVelvet border border-pearlWhite/10 transition-colors">IX. Phir Kya Hua?</button>
            <button onclick="jumpToChapter('section-ch11')" class="px-2.5 py-1 rounded-full bg-obsidian/70 hover:text-champagne hover:bg-nightVelvet border border-pearlWhite/10 transition-colors">XI. First Kiss</button>
            <button onclick="jumpToChapter('section-ch12')" class="px-2.5 py-1 rounded-full bg-obsidian/70 hover:text-champagne hover:bg-nightVelvet border border-pearlWhite/10 transition-colors">XII. Indore</button>
            <button onclick="jumpToChapter('section-ch13')" class="px-2.5 py-1 rounded-full bg-obsidian/70 hover:text-champagne hover:bg-nightVelvet border border-pearlWhite/10 transition-colors">XIII. Forever</button>
          </div>

          <!-- POEM TEXT CONTAINER -->
          <div id="fullPoemManuscript" class="font-serif text-pearlWhite/90 leading-relaxed sm:leading-loose text-lg py-6 max-h-[640px] overflow-y-auto pr-2 sm:pr-4 space-y-12 transition-all">

            <!-- Opening Reflection -->
            <article id="section-intro" class="p-5 sm:p-6 rounded-2xl bg-nightVelvet/50 border border-champagne/15 relative">
              <span class="text-[10px] uppercase font-mono tracking-widest text-champagne">Opening Reflection</span>
              <p class="italic mt-2 text-roseMist/95">
                We fight, we fall, we heal, we stay,<br>
                Yet why does love still drift away?<br>
                Each wound we mend, each tear we dry,<br>
                Still, storms return — do you wonder why?<br>
                We hold on tight, refuse to part,<br>
                But are we healing or just pressing restart?<br>
                Let's dive beneath the words we say,<br>
                And find the cracks that beg to stay.
              </p>
            </article>

            <!-- Chapter I -->
            <article id="section-ch1" class="border-l-2 border-champagne/40 pl-4 sm:pl-6 space-y-3">
              <div class="flex items-center gap-2">
                <span class="w-6 h-6 rounded-full bg-champagne/20 text-champagne text-xs font-mono flex items-center justify-center font-bold">1</span>
                <h4 class="font-serif text-2xl text-champagneLight font-normal">CHAPTER I — THE TWELFTH GRADE GAZE</h4>
              </div>
              <p class="text-xs uppercase tracking-wider text-pearlWhite/40 font-sans italic">
                "Well, This story is about a person, whom I saw for the first time in my 12th standard..."
              </p>
              <p class="italic text-pearlWhite/90">
                I saw her first in twelfth-grade light,<br>
                Drifting through desks, left and right.<br>
                Each one whispered, "She looks at me,"<br>
                I laughed — how strange could this all be?<br><br>
                Then my eyes met hers at last,<br>
                Deep and dark, so still, so vast.<br>
                No wonder all had felt her stare,<br>
                Her gaze was everywhere and nowhere.<br><br>
                I thought to tell her, share the jest,<br>
                But something held me, let it rest.<br>
                A moment gone, a chance slipped by,<br>
                And to this day, I don't know why.
              </p>
            </article>

            <!-- Chapter II -->
            <article id="section-ch2" class="border-l-2 border-champagne/40 pl-4 sm:pl-6 space-y-3">
              <div class="flex items-center gap-2">
                <span class="w-6 h-6 rounded-full bg-champagne/20 text-champagne text-xs font-mono flex items-center justify-center font-bold">2</span>
                <h4 class="font-serif text-2xl text-champagneLight font-normal">CHAPTER II — THE FAREWELL PHOTOGRAPH</h4>
              </div>
              <p class="text-xs uppercase tracking-wider text-pearlWhite/40 font-sans italic">
                "Now a wise man is saying: 'Always expect the unexpected!'"
              </p>
              <p class="italic text-pearlWhite/90">
                The days had passed, the time had flown,<br>
                A silent story left unknown.<br>
                Not once had words between us spun,<br>
                Yet fate had plans — its work undone.<br><br>
                With farewell near, I made a vow,<br>
                To step beyond my silence now.<br>
                A picture with all, a memory bright,<br>
                To leave with joy, not lost in night.<br><br>
                And then, as if the stars had schemed,<br>
                She stood before me like a dream.<br>
                One final chance, the very last day,<br>
                To cast my fears and words convey.<br><br>
                A timid "hello," a breath so deep,<br>
                A moment time had sworn to keep.<br>
                The shutter clicked, the echoes stayed,<br>
                A frozen frame the past had made.<br><br>
                Not just a picture, not just a glance,<br>
                But courage found in fleeting chance.<br>
                A chapter closed, yet hearts still know,<br>
                Some stories end, yet never go.
              </p>
            </article>

            <!-- Chapter III -->
            <article id="section-ch3" class="border-l-2 border-champagne/40 pl-4 sm:pl-6 space-y-3">
              <div class="flex items-center gap-2">
                <span class="w-6 h-6 rounded-full bg-champagne/20 text-champagne text-xs font-mono flex items-center justify-center font-bold">3</span>
                <h4 class="font-serif text-2xl text-champagneLight font-normal">CHAPTER III — THE GLOWING SCREEN</h4>
              </div>
              <p class="text-xs uppercase tracking-wider text-pearlWhite/40 font-sans italic">
                "Sometimes what appears to be an END is not actually THE END..."
              </p>
              <p class="italic text-pearlWhite/90">
                The end was not an end at all,<br>
                But where the stars began to call.<br>
                For in the night, when silence grew,<br>
                A message came soft, yet true.<br><br>
                Her name appeared, my heart took flight,<br>
                A whisper sent through glowing light.<br>
                She asked for a picture, a memory framed,<br>
                One that another hand had claimed.<br><br>
                I promised to send it, waited in vain,<br>
                For a photograph lost in a filter's reign.<br>
                When it arrived, not quite the same,<br>
                Colors shifted, yet fate still came.<br>
                Perhaps she ruined what past had drawn,<br>
                But in that blur, the future was born.
              </p>
            </article>

            <!-- Chapter IV -->
            <article id="section-ch4" class="border-l-2 border-champagne/40 pl-4 sm:pl-6 space-y-3">
              <div class="flex items-center gap-2">
                <span class="w-6 h-6 rounded-full bg-champagne/20 text-champagne text-xs font-mono flex items-center justify-center font-bold">4</span>
                <h4 class="font-serif text-2xl text-champagneLight font-normal">CHAPTER IV — ENDLESS NIGHTS & PLAYFUL DUELS</h4>
              </div>
              <p class="text-xs uppercase tracking-wider text-pearlWhite/40 font-sans italic">
                "Dramatic reference of further story..."
              </p>
              <p class="italic text-pearlWhite/90">
                From a single text to endless nights,<br>
                We talked and talked under moonlit lights.<br>
                Day by day, she felt less unknown,<br>
                A stranger once, now a bond had grown.<br><br>
                Most of our words held no real theme,<br>
                Yet I stretched each chat like a fragile dream.<br>
                Nonsense, laughter, playful fights,<br>
                Yet I clung to them with all my might.<br><br>
                I teased her, poked at her pride,<br>
                Said she's not a girl — just to see her fiery side.<br>
                Or dropped a name she might secretly admire,<br>
                Watching her rage, setting heart on fire.<br><br>
                She'd argue, she'd scowl, she'd call me a fool,<br>
                Yet somehow, I cherished each little duel.<br>
                I don't know why, I can't explain,<br>
                But talking to her feels like a home in the rain.
              </p>
            </article>

            <!-- Chapter V -->
            <article id="section-ch5" class="border-l-2 border-champagne/40 pl-4 sm:pl-6 space-y-3">
              <div class="flex items-center gap-2">
                <span class="w-6 h-6 rounded-full bg-champagne/20 text-champagne text-xs font-mono flex items-center justify-center font-bold">5</span>
                <h4 class="font-serif text-2xl text-champagneLight font-normal">CHAPTER V — THE UNSPOKEN WEIGHT</h4>
              </div>
              <p class="text-xs uppercase tracking-wider text-pearlWhite/40 font-sans italic">
                "It feels so heavy whenever she talks about others..."
              </p>
              <p class="italic text-pearlWhite/90">
                Maybe it's true, maybe it's real,<br>
                This growing weight I start to feel.<br>
                I never meant for this to be,<br>
                Yet here I am, lost at sea.<br><br>
                I tease, I joke, I play around,<br>
                Yet my heart beats loud, an unspoken sound.<br>
                I never told her, never tried,<br>
                That every time a part of me died.<br><br>
                Whenever she laughs, talking his name,<br>
                I smile, I nod, but it's not the same.<br>
                A quiet fire, a hidden sting,<br>
                A war within that words don't bring.<br><br>
                I hate it, yet I never show,<br>
                She'll never ask, she'll never know.<br>
                So I keep talking, hold her near,<br>
                Hiding truth behind a jeer.
              </p>
            </article>

            <!-- Chapter VI -->
            <article id="section-ch6" class="border-l-2 border-champagne/40 pl-4 sm:pl-6 space-y-3">
              <div class="flex items-center gap-2">
                <span class="w-6 h-6 rounded-full bg-champagne/20 text-champagne text-xs font-mono flex items-center justify-center font-bold">6</span>
                <h4 class="font-serif text-2xl text-champagneLight font-normal">CHAPTER VI — CROSSING THE LINE</h4>
              </div>
              <p class="text-xs uppercase tracking-wider text-pearlWhite/40 font-sans italic">
                "So this is how I confessed her my feelings..."
              </p>
              <p class="italic text-pearlWhite/90">
                Every guy in her life, a villain to me,<br>
                A shadow cast on the love I can't free.<br>
                I made a vow, silent and strong,<br>
                To bury my feelings, to prove myself wrong.<br><br>
                She sees me as a friend, nothing more nothing less,<br>
                So I lock my heart, let it sink, suppress.<br>
                Yet on my birthday, her presence shone bright,<br>
                A moment so simple, yet it felt so right.<br><br>
                Deep inside, I made a decree,<br>
                To never hurt her, to let her be.<br>
                To guard her joy, to keep her safe,<br>
                Even if love meant my heart's own grave.<br><br>
                But then came a spark, a whisper, a sign,<br>
                Her friend's words nudged me to cross the line.<br>
                A feeling, a hint, a chance so slight,<br>
                That maybe, just maybe, she felt it right.<br><br>
                For once, I stood against my own tide,<br>
                Pushed past the walls where my fears reside.<br>
                And with a strength I rarely knew,<br>
                I confessed — heart open, raw and true.<br><br>
                Would I have dared, without divine grace?<br>
                Without Lord Krishna's guiding embrace?<br>
                Perhaps not, but fate had aligned,<br>
                A moment where love no longer confined.
              </p>
            </article>

            <!-- Chapter VII -->
            <article id="section-ch7" class="border-l-2 border-champagne/40 pl-4 sm:pl-6 space-y-3">
              <div class="flex items-center gap-2">
                <span class="w-6 h-6 rounded-full bg-champagne/20 text-champagne text-xs font-mono flex items-center justify-center font-bold">7</span>
                <h4 class="font-serif text-2xl text-champagneLight font-normal">CHAPTER VII — THE NOVEMBER STORM & THE TURN OF FATE</h4>
              </div>
              <p class="text-xs uppercase tracking-wider text-pearlWhite/40 font-sans italic">
                "Wondering what happened after I confessed? It's even more dramatic..."
              </p>
              <p class="italic text-pearlWhite/90">
                I laid it all bare, no walls, no disguise,<br>
                Every thought, every feeling, no more lies.<br>
                But silence lingered, stretching so long,<br>
                Each second a battle, each moment felt wrong.<br><br>
                We talked still, as if nothing had changed,<br>
                Yet my heart knew — we weren't the same.<br>
                I got angry, confused, lost in the haze,<br>
                Why not just tell me and end these days?<br><br>
                Mixed signals, hope tangled with doubt,<br>
                One day she's near, the next she's out.<br>
                Then came November, cold and cruel,<br>
                A night that shattered my every rule.<br><br>
                She finally spoke, broke the thread,<br>
                With words that turned my heart to lead.<br>
                She didn't feel the way I did,<br>
                And in that moment, my soul slid.<br><br>
                Tears fell fast, blame hit deep,<br>
                I lost her twice — love and friendship to keep.<br>
                Two days of silence, empty and long,<br>
                I swore I was done, I had to be strong.<br><br>
                But then, like fate had flipped the page,<br>
                On the 4th, she returned to the stage.<br>
                One simple line, one sudden light,<br>
                And somehow, she made my darkest night bright.
              </p>
            </article>

            <!-- Chapter VIII -->
            <article id="section-ch8" class="border-l-2 border-champagne/40 pl-4 sm:pl-6 space-y-3">
              <div class="flex items-center gap-2">
                <span class="w-6 h-6 rounded-full bg-champagne/20 text-champagne text-xs font-mono flex items-center justify-center font-bold">8</span>
                <h4 class="font-serif text-2xl text-champagneLight font-normal">CHAPTER VIII — CLASHING, TRUSTING & GROWING</h4>
              </div>
              <p class="text-xs uppercase tracking-wider text-pearlWhite/40 font-sans italic">
                "How everything is going on..."
              </p>
              <p class="italic text-pearlWhite/90">
                From that day on, everything felt right,<br>
                Though fights would come, like day and night.<br>
                At least once a month, we'd clash and collide,<br>
                Yet somehow, we'd always stand side by side.<br><br>
                No one's perfect, that much is true,<br>
                But through it all, I still trust you.<br>
                And I hope you trust me just the same,<br>
                Through every storm, through joy and pain.<br><br>
                I remember our first fight, your birthday night,<br>
                I thought you lied — maybe I wasn't right.<br>
                We were silly, don't you think?<br>
                Yet even then, we didn't sink.<br><br>
                Lies are common, they come and go,<br>
                But between us, I want truth to flow.<br>
                No hiding, no secrets, nothing to fear,<br>
                That's how we'll grow, year by year.<br><br>
                Maybe I'm possessive, though I don't show,<br>
                But if you're mine, then the world should know.<br>
                I won't change, I'll stay the same,<br>
                I just hope you feel my flame.<br><br>
                We fight, yes, but that's okay,<br>
                As long as we find our way.<br>
                Through every fall, through every test,<br>
                Sorting it out — that's what makes us best.
              </p>
            </article>

            <!-- Chapter IX -->
            <article id="section-ch9" class="border-l-2 border-champagne/40 pl-4 sm:pl-6 space-y-3">
              <div class="flex items-center gap-2">
                <span class="w-6 h-6 rounded-full bg-champagne/20 text-champagne text-xs font-mono flex items-center justify-center font-bold">9</span>
                <h4 class="font-serif text-2xl text-champagneLight font-normal">CHAPTER IX — PHIR KYA HUA? HAND IN HAND</h4>
              </div>
              <p class="text-xs uppercase tracking-wider text-pearlWhite/40 font-sans italic">
                "Sorry for the delay in writing. Let's start... Phir? Phir Kya hua??"
              </p>
              <p class="italic text-pearlWhite/90">
                The months rolled on, the seasons turned,<br>
                A steady fire inside us burned.<br>
                Through heavy books and endless grind,<br>
                You were the peace I sought to find.<br>
                No longer guessing where we stand,<br>
                Just walking closely, hand in hand.<br><br>
                Late-night talks and quiet grace,<br>
                Finding our home in every space.<br>
                You learned my flaws, I learned your ways,<br>
                Through busy nights and heavy days.<br>
                Real and raw, without a mask,<br>
                Loving you, never feels like a task.<br><br>
                A communication gap we didn't need,<br>
                Yet through the distance, love took heed.<br>
                Surrounded by your Mosi, Mama near,<br>
                With Vami right beside you, drawing clear,<br>
                You still carved out the time to talk to me,<br>
                I see the effort, rare and true,<br>
                And I'm so glad, and grateful, it was you.<br><br>
                Things didn't go the way they should have gone,<br>
                When your Didi left, our peace was gone.<br>
                You said you'd leave, your heart was deeply hurt,<br>
                And parting words began to stir and blur.<br>
                I'm sorry for the pain I caused you then,<br>
                Please, don't ever say those words again.<br>
                Through every fight, I want you right with me,<br>
                Just stay, and let our love run wild and free.<br><br>
                We really enjoyed the month we met,<br>
                November moments I won't forget.<br>
                On the 4th I said, "You have to come,"<br>
                And suddenly our hearts beat as one.<br>
                The strongest cake you gave me on my day,<br>
                And celebrating yours in our special way.<br>
                For the first time, walking hand in hand,<br>
                To the Gurudwara, just as unplanned.
              </p>
            </article>

            <!-- Chapter X -->
            <article id="section-ch10" class="border-l-2 border-champagne/40 pl-4 sm:pl-6 space-y-3">
              <div class="flex items-center gap-2">
                <span class="w-6 h-6 rounded-full bg-champagne/20 text-champagne text-xs font-mono flex items-center justify-center font-bold">10</span>
                <h4 class="font-serif text-2xl text-champagneLight font-normal">CHAPTER X — COLLEGE GATES & 2025</h4>
              </div>
              <p class="text-xs uppercase tracking-wider text-pearlWhite/40 font-sans italic">
                "Leaving 2025 Behind..."
              </p>
              <p class="italic text-pearlWhite/90">
                I really enjoyed our days back then,<br>
                Meeting outside your college gate again.<br>
                Taking you home, reluctant to say goodbye,<br>
                As 2025 slipped under the sky.<br>
                I wasn't ready to let that year depart,<br>
                Unaware of what 2026 held in its heart.
              </p>
            </article>

            <!-- Chapter XI -->
            <article id="section-ch11" class="border-l-2 border-champagne/40 pl-4 sm:pl-6 space-y-3">
              <div class="flex items-center gap-2">
                <span class="w-6 h-6 rounded-full bg-champagne/20 text-champagne text-xs font-mono flex items-center justify-center font-bold">11</span>
                <h4 class="font-serif text-2xl text-champagneLight font-normal">CHAPTER XI — THE FIRST ROSE & FIRST KISS</h4>
              </div>
              <p class="text-xs uppercase tracking-wider text-pearlWhite/40 font-sans italic">
                "~ Zoroko, Charisma, and the First Kiss"
              </p>
              <p class="italic text-pearlWhite/90">
                The very first day at Zoroko we met,<br>
                You were busy on your phone, ignoring me yet.<br>
                Sitting beside you, I gave you a rose,<br>
                Hope you liked it, despite how it shows.<br>
                Sorry for the little taunt I had to make,<br>
                A little tease for old times' sake.<br><br>
                Then came a surprise I hadn't planned at all —<br>
                A sudden kiss that made me softly fall.<br>
                Lost in that moment, I don't know how or when,<br>
                And into Charisma we stepped right then.<br>
                We enjoyed every day, a core memory so bright,<br>
                Carried through my life like a guiding light.<br>
                We've kissed many times, and I love them all,<br>
                But that very first one holds my heart in thrall.
              </p>
            </article>

            <!-- Chapter XII -->
            <article id="section-ch12" class="border-l-2 border-champagne/40 pl-4 sm:pl-6 space-y-3">
              <div class="flex items-center gap-2">
                <span class="w-6 h-6 rounded-full bg-champagne/20 text-champagne text-xs font-mono flex items-center justify-center font-bold">12</span>
                <h4 class="font-serif text-2xl text-champagneLight font-normal">CHAPTER XII — THE INDORE EVENINGS</h4>
              </div>
              <p class="text-xs uppercase tracking-wider text-pearlWhite/40 font-sans italic">
                "The Internship Days..."
              </p>
              <p class="italic text-pearlWhite/90">
                I don't know how fast the days had passed,<br>
                Those internship weeks went by too fast.<br>
                Dropping you home was all I wanted then,<br>
                Wishing those rides wouldn't end.<br>
                Through every moment, crazy and true,<br>
                I really love you... my crazy love, Yep it's you.
              </p>
            </article>

            <!-- Chapter XIII -->
            <article id="section-ch13" class="border-l-2 border-champagne/40 pl-4 sm:pl-6 space-y-4">
              <div class="flex items-center gap-2">
                <span class="w-6 h-6 rounded-full bg-champagne/20 text-champagne text-xs font-mono flex items-center justify-center font-bold">13</span>
                <h4 class="font-serif text-2xl text-champagneLight font-normal">CHAPTER XIII — FOREVER YOURS</h4>
              </div>
              <p class="text-xs uppercase tracking-wider text-pearlWhite/40 font-sans italic">
                "My Wish For You & Forever Yours..."
              </p>
              <p class="italic text-pearlWhite/90">
                I wanted you to stay right here with me,<br>
                Though wishing for your dreams was meant to be.<br>
                I liked you close in Indore, yet felt your pain,<br>
                When colleges didn't grant what you hoped to gain.<br><br>
                I'm sorry, Ishika, for the times I lost my way,<br>
                Buried in audits when I should have had more to say.<br>
                I swear I'll make sure that it won't repeat,<br>
                Your heart and comfort make my life complete.<br><br>
                Whatever you wanted, I prayed you'd find,<br>
                Leaving all the heavy doubts behind.<br>
                Whatever I did, my truth stands clear —<br>
                I am yours, forever yours, year after year.<br><br>
                Another year, another test,<br>
                With you is where my heart finds rest.<br>
                From twelfth-grade shade to light so clear,<br>
                I look at you and find my year.<br>
                No matter what the world may say,<br>
                I chose you then... I choose today.
              </p>

              <!-- Final Grand P.S. -->
              <div class="pt-6 border-t border-champagne/20 text-center">
                <span class="font-serif text-2xl sm:text-3xl text-transparent bg-clip-text bg-gradient-to-r from-champagneLight via-roseMist to-crimsonGlow font-semibold tracking-wide">
                  P.S. I Love You!! ❤️
                </span>
                <p class="text-xs font-sans tracking-widest text-champagne/80 mt-2 uppercase">
                  — Always & Eternally Yours, Ayush
                </p>
              </div>
            </article>

          </div>

          <!-- Bottom Footer within Poem Card -->
          <div class="pt-6 border-t border-pearlWhite/10 flex flex-col sm:flex-row items-center justify-between gap-4 text-xs">
            <span class="text-pearlWhite/50">13 Chapters of Our Unstoppable Story</span>
            <div class="flex items-center gap-3">
              <button onclick="scrollToTopPoem()" class="text-champagneLight hover:underline flex items-center gap-1">
                <i class="ph-bold ph-arrow-up"></i>
                <span>Back to Top of Poem</span>
              </button>
              <button onclick="triggerPetalConfetti()" class="px-3 py-1.5 rounded-full bg-champagne/15 text-champagne border border-champagne/30 hover:bg-champagne hover:text-obsidian transition-all">
                Shower Petals
              </button>
            </div>
          </div>

        </div>

      </div>
    </section>

    <!-- CHAPTER 3: THE EDITS & SHORT VIDEOS VAULT -->
    <section id="chapter-3" class="py-20 px-4 sm:px-6 max-w-6xl mx-auto scroll-mt-24">
      <div class="flex items-center justify-between mb-8">
        <div>
          <span class="text-xs uppercase tracking-widest text-champagne font-semibold flex items-center gap-1.5 mb-1">
            <i class="ph-fill ph-number-circle-three"></i> Chapter Three
          </span>
          <h2 class="font-serif text-3xl sm:text-4xl text-pearlWhite">Captured Reels & Edits</h2>
        </div>
        <div id="statusBadge3" class="px-3 py-1 rounded-full text-xs font-medium border border-roseMist/20 text-roseMist bg-nightVelvet flex items-center gap-1.5">
          <i class="ph-bold ph-lock text-xs"></i> <span>Locked</span>
        </div>
      </div>

      <div class="relative rounded-3xl overflow-hidden min-h-[380px] transition-all duration-700" id="cardContainer3">
        
        <!-- LOCKED OVERLAY VIEW (STRICT INPUT LOCK) -->
        <div id="lockView3" class="glass-surface-lock p-8 sm:p-14 text-center rounded-3xl flex flex-col items-center justify-center min-h-[380px]">
          <div class="w-16 h-16 rounded-full bg-crimsonVelvet/30 border border-crimsonGlow/40 flex items-center justify-center text-champagneLight text-2xl mb-4 shadow-inner animate-pulse-glow">
            <i class="ph-fill ph-video-camera"></i>
          </div>
          <h3 class="font-serif text-2xl sm:text-3xl text-pearlWhite mb-2">Our Highlights & Cutdowns</h3>
          <p class="text-champagneLight font-serif italic text-base sm:text-lg max-w-lg mb-6">
            "What was the date of our First Kiss? 💋"
          </p>

          <!-- Strict Answer Form -->
          <div class="w-full max-w-md space-y-3">
            <div class="relative">
              <input type="text" id="answerInput3" placeholder="Type our unforgettable date..." class="w-full bg-obsidian/90 border border-pearlWhite/20 focus:border-champagne rounded-xl px-4 py-3 text-sm text-pearlWhite pr-24 focus:outline-none transition-colors" onkeydown="if(event.key === 'Enter') submitDirectAnswer(3)">
              <button onclick="submitDirectAnswer(3)" class="absolute right-1.5 top-1.5 bottom-1.5 px-4 rounded-lg bg-gradient-to-r from-champagne to-champagneLight text-obsidian text-xs font-bold hover:scale-105 transition-transform flex items-center gap-1 shadow-sm">
                <i class="ph-bold ph-key"></i>
                <span>Unlock</span>
              </button>
            </div>
            
            <div id="feedbackText3" class="text-xs font-medium min-h-[1.25rem]"></div>

            <div class="pt-1">
              <button onclick="toggleHint(3)" class="text-xs text-pearlWhite/60 hover:text-champagneLight underline flex items-center justify-center gap-1 mx-auto transition-colors">
                <i class="ph-bold ph-lightbulb"></i>
                <span>Need a hint?</span>
              </button>
              <p id="hintBox3" class="text-xs text-roseMist bg-nightVelvet/80 p-3 rounded-xl border border-roseMist/30 italic mt-3 hidden text-center transition-all">
                "I owe 1 kiss, if you can't Answer this! 💋🙈"
              </p>
            </div>
          </div>
        </div>

        <!-- UNLOCKED VIEW: THE EDITS MASONRY/GRID -->
        <div id="unlockedView3" class="hidden glass-surface rounded-3xl p-6 sm:p-8 border border-champagne/30">
          
          <div class="flex flex-col sm:flex-row sm:items-center justify-between pb-6 border-b border-pearlWhite/10 mb-6 gap-4">
            <div>
              <span class="text-[10px] uppercase tracking-widest text-champagne font-semibold flex items-center gap-1.5">
                <i class="ph-fill ph-film-strip"></i> Our Journey in Motion
              </span>
              <h3 class="font-serif text-xl sm:text-2xl text-pearlWhite mt-1">Eight Moments of Us</h3>
              <p class="text-xs text-pearlWhite/60">Powered by Google Drive. Tap any reel to play the memory.</p>
            </div>
            <div class="flex items-center gap-2 self-start sm:self-auto">
              <button onclick="openBulkDriveModal()" class="px-3 py-1.5 rounded-xl bg-champagne/15 hover:bg-champagne/25 text-champagneLight text-xs flex items-center gap-1.5 border border-champagne/30 transition-colors">
                <i class="ph-fill ph-google-drive-logo text-sm text-champagne"></i>
                <span>Set Drive Links</span>
              </button>
              <span class="text-[11px] text-pearlWhite/50 font-mono">Reels I – VIII</span>
            </div>
          </div>

          <!-- Chronological Story Timeline Grid for the 8 Edits -->
          <div id="editsVaultGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-5">
            <!-- Dynamic 8 story-linked edit cards loaded via JS -->
          </div>

        </div>

      </div>
    </section>

    <!-- CHAPTER 4: THE FINAL 3D LOVE LETTER & SECRET -->
    <section id="chapter-4" class="py-20 px-4 sm:px-6 max-w-4xl mx-auto scroll-mt-24">
      <div class="flex items-center justify-between mb-8">
        <div>
          <span class="text-xs uppercase tracking-widest text-champagne font-semibold flex items-center gap-1.5 mb-1">
            <i class="ph-fill ph-number-circle-four"></i> Chapter Four
          </span>
          <h2 class="font-serif text-3xl sm:text-4xl text-pearlWhite">The Final Secret</h2>
        </div>
        <div id="statusBadge4" class="px-3 py-1 rounded-full text-xs font-medium border border-roseMist/20 text-roseMist bg-nightVelvet flex items-center gap-1.5">
          <i class="ph-bold ph-lock text-xs"></i> <span>Locked</span>
        </div>
      </div>

      <div class="relative rounded-3xl overflow-hidden min-h-[380px] transition-all duration-700" id="cardContainer4">
        
        <!-- LOCKED OVERLAY VIEW (STRICT INPUT LOCK) -->
        <div id="lockView4" class="glass-surface-lock p-8 sm:p-14 text-center rounded-3xl flex flex-col items-center justify-center min-h-[380px]">
          <div class="w-16 h-16 rounded-full bg-crimsonVelvet/30 border border-crimsonGlow/40 flex items-center justify-center text-champagneLight text-2xl mb-4 shadow-inner animate-pulse-glow">
            <i class="ph-fill ph-envelope-simple-heart"></i>
          </div>
          <h3 class="font-serif text-2xl sm:text-3xl text-pearlWhite mb-2">The Sealed Vow</h3>
          <p class="text-champagneLight font-serif italic text-base sm:text-lg max-w-lg mb-6">
            "Name the place we Often Visit Together? 🍕"
          </p>

          <!-- Strict Answer Form -->
          <div class="w-full max-w-md space-y-3">
            <div class="relative">
              <input type="text" id="answerInput4" placeholder="Type our favorite spot..." class="w-full bg-obsidian/90 border border-pearlWhite/20 focus:border-champagne rounded-xl px-4 py-3 text-sm text-pearlWhite pr-24 focus:outline-none transition-colors" onkeydown="if(event.key === 'Enter') submitDirectAnswer(4)">
              <button onclick="submitDirectAnswer(4)" class="absolute right-1.5 top-1.5 bottom-1.5 px-4 rounded-lg bg-gradient-to-r from-champagne to-champagneLight text-obsidian text-xs font-bold hover:scale-105 transition-transform flex items-center gap-1 shadow-sm">
                <i class="ph-bold ph-key"></i>
                <span>Unlock</span>
              </button>
            </div>
            
            <div id="feedbackText4" class="text-xs font-medium min-h-[1.25rem]"></div>

            <div class="pt-1">
              <button onclick="toggleHint(4)" class="text-xs text-pearlWhite/60 hover:text-champagneLight underline flex items-center justify-center gap-1 mx-auto transition-colors">
                <i class="ph-bold ph-lightbulb"></i>
                <span>Need a hint?</span>
              </button>
              <p id="hintBox4" class="text-xs text-roseMist bg-nightVelvet/80 p-3 rounded-xl border border-roseMist/30 italic mt-3 hidden text-center transition-all">
                "Lets go one more date at that place! 🍕✨"
              </p>
            </div>
          </div>
        </div>

        <!-- UNLOCKED VIEW: THE INTERACTIVE 3D ENVELOPE -->
        <div id="unlockedView4" class="hidden glass-surface rounded-3xl p-6 sm:p-12 border border-champagne/30 text-center">
          
          <div class="mb-6">
            <span class="inline-flex items-center gap-1.5 px-3 py-1 rounded-full bg-emerald-500/20 text-emerald-300 text-xs font-medium border border-emerald-500/30 mb-2">
              <i class="ph-fill ph-check-circle"></i> Complete Quest Unlocked
            </span>
            <h3 class="font-serif text-3xl sm:text-4xl text-pearlWhite">A Letter Sealed For Eternity</h3>
            <p class="text-xs sm:text-sm text-pearlWhite/65 max-w-md mx-auto mt-2">
              Tap on the envelope below to break the wax seal and unfold my private letter to you.
            </p>
          </div>

          <!-- 3D Flipping Envelope Wrapper -->
          <div class="max-w-lg mx-auto envelope-3d-wrap my-4">
            <div id="envelopeFlipCard" class="envelope-card glass-surface rounded-3xl p-8 cursor-pointer relative shadow-2xl border border-champagne/40 hover:border-champagne transition-all" onclick="toggleEnvelopeFlip()">
              
              <!-- Front of Sealed Envelope -->
              <div class="envelope-front flex flex-col items-center justify-center py-6">
                <!-- Wax Seal Graphic -->
                <div class="w-16 h-16 rounded-full bg-gradient-to-tr from-crimsonVelvet to-crimsonGlow flex items-center justify-center text-champagneLight text-2xl shadow-lg shadow-crimsonVelvet/50 border border-champagne/40 mb-4 animate-bounce">
                  <i class="ph-fill ph-heart"></i>
                </div>
                <h4 class="font-serif text-2xl text-pearlWhite mb-1">To My Forever Person</h4>
                <p class="text-xs text-pearlWhite/50 mb-6 font-mono">CONFIDENTIAL & SACRED</p>
                <span class="px-4 py-2 rounded-full bg-champagne/15 border border-champagne/30 text-champagneLight text-xs tracking-wider uppercase font-semibold">
                  Tap to Break Seal
                </span>
              </div>

              <!-- Unfolded Letter (Back Face) -->
              <div class="envelope-back absolute inset-0 p-6 sm:p-8 flex flex-col justify-between bg-nightVelvet rounded-3xl border border-champagne/30 text-left overflow-y-auto">
                <div>
                  <div class="flex items-center justify-between pb-3 border-b border-pearlWhite/10 mb-4 text-xs text-champagneLight">
                    <span class="font-serif italic text-base">Dearest Ishika,</span>
                    <i class="ph-fill ph-infinity text-lg text-roseMist"></i>
                  </div>
                  <p class="text-pearlWhite/90 text-xs sm:text-sm leading-relaxed font-serif italic mb-4">
                    "From the boy who sat quietly in 12th grade wondering why everyone said you were looking at him, to the person who now cherishes every Indore evening and every late-night phone call... there isn't a single memory of you that I take for granted."
                  </p>
                  <p class="text-pearlWhite/80 text-xs sm:text-sm leading-relaxed font-serif italic">
                    "I am sorry for the audit days when work got loud, and for every time I hurt you without knowing. You are my home in the rain, my first kiss at Zoroko, and my favorite date at La Pino'z. No matter what the future tests us with, I chose you then, and I choose you today."
                  </p>
                </div>
                <div class="pt-4 border-t border-pearlWhite/10 text-right">
                  <span class="text-xs tracking-widest text-champagne uppercase font-sans font-semibold">P.S. I Love You Ishika!</span>
                </div>
              </div>

            </div>
          </div>

          <p class="text-[11px] text-pearlWhite/40 tracking-wider uppercase mt-4">
            Tap the letter anytime to fold it back
          </p>

        </div>

      </div>
    </section>

  </main>

  <!-- LUXURIOUS FOOTER -->
  <footer class="border-t border-pearlWhite/10 bg-obsidian py-14 px-4 text-center relative z-10">
    <div class="max-w-2xl mx-auto flex flex-col items-center gap-4">
      <div class="w-10 h-10 rounded-full bg-nightVelvet border border-champagne/30 flex items-center justify-center text-champagne shadow-inner">
        <i class="ph-fill ph-infinity text-xl"></i>
      </div>
      <p class="font-serif text-xl sm:text-2xl text-pearlWhite font-light">
        "I loved you yesterday, I love you still, I always have, I always will."
      </p>
      <div class="flex items-center gap-3 text-xs text-pearlWhite/45">
        <span>Ayush & Ishika</span>
        <span>•</span>
        <button onclick="resetAllProgress()" class="hover:text-roseMist text-pearlWhite/40 hover:underline transition-colors">
          Reset Locks (For Ayush to test)
        </button>
      </div>
    </div>
  </footer>

  <!-- ================= MODALS ================= -->
  <!-- 2. MAIN VIDEO UPLOAD / URL MODAL -->
  <div id="videoUploadModal" class="fixed inset-0 bg-obsidian/85 backdrop-blur-xl z-50 flex items-center justify-center p-4 hidden">
    <div class="glass-surface w-full max-w-lg rounded-3xl p-6 sm:p-8 border border-champagne/40 relative shadow-2xl">
      <button onclick="document.getElementById('videoUploadModal').classList.add('hidden')" class="absolute top-5 right-5 text-pearlWhite/60 hover:text-pearlWhite text-xl">
        <i class="ph-bold ph-x"></i>
      </button>

      <div class="flex items-center gap-2.5 mb-2">
        <i class="ph-bold ph-video-camera text-xl text-champagneLight"></i>
        <h3 class="font-serif text-2xl text-pearlWhite">Load Your Recorded Video</h3>
      </div>
      <p class="text-xs text-pearlWhite/60 mb-5">
        Select your actual MP4 / MOV file directly from your device, or paste a video link.
      </p>

      <!-- Local File Upload Input -->
      <div class="mb-4">
        <label class="block text-xs uppercase tracking-wider text-pearlWhite/70 mb-2 font-medium">1. Choose Video From Your Device</label>
        <div class="border border-dashed border-pearlWhite/20 hover:border-champagne/50 rounded-2xl p-5 text-center cursor-pointer bg-nightVelvet/50 hover:bg-nightVelvet transition-colors" onclick="document.getElementById('mainVideoFileInput').click()">
          <i class="ph-light ph-upload-simple text-3xl text-champagneLight mb-1"></i>
          <p class="text-xs text-pearlWhite/90 font-medium">Click to select recorded video</p>
          <span class="text-[10px] text-pearlWhite/40">MP4, WebM, MOV supported (Runs locally in your browser)</span>
          <input type="file" id="mainVideoFileInput" accept="video/*" class="hidden" onchange="handleMainVideoFile(event)">
        </div>
      </div>

      <div class="flex items-center my-3">
        <div class="flex-grow border-t border-pearlWhite/10"></div>
        <span class="px-3 text-[10px] text-pearlWhite/40 uppercase tracking-widest">Or Use Video URL</span>
        <div class="flex-grow border-t border-pearlWhite/10"></div>
      </div>

      <!-- URL Input -->
      <div class="space-y-3">
        <div>
          <label class="block text-xs uppercase tracking-wider text-pearlWhite/70 mb-1">Video Title</label>
          <input type="text" id="inputCustomVideoTitle" placeholder="e.g. My Favorite Girl in the World" class="w-full bg-obsidian border border-pearlWhite/15 rounded-xl px-4 py-2 text-xs text-pearlWhite focus:border-champagne">
        </div>
        <div>
          <label class="block text-xs uppercase tracking-wider text-pearlWhite/70 mb-1">Direct Video URL</label>
          <input type="url" id="inputCustomVideoUrl" placeholder="https://example.com/video.mp4" class="w-full bg-obsidian border border-pearlWhite/15 rounded-xl px-4 py-2 text-xs text-pearlWhite focus:border-champagne">
        </div>
      </div>

      <div class="flex justify-end gap-3 mt-5">
        <button onclick="document.getElementById('videoUploadModal').classList.add('hidden')" class="px-4 py-2 text-xs text-pearlWhite/60 hover:text-pearlWhite">Cancel</button>
        <button onclick="applyMainVideoUrl()" class="px-5 py-2.5 rounded-xl bg-champagne text-obsidian text-xs font-semibold shadow-md">Apply Video</button>
      </div>
    </div>
  </div>

  <!-- 3. ADD NEW EDIT MODAL -->
  <div id="newEditModal" class="fixed inset-0 bg-obsidian/85 backdrop-blur-xl z-50 flex items-center justify-center p-4 hidden">
    <div class="glass-surface w-full max-w-md rounded-3xl p-6 sm:p-8 border border-champagne/40 relative shadow-2xl">
      <button onclick="document.getElementById('newEditModal').classList.add('hidden')" class="absolute top-5 right-5 text-pearlWhite/60 hover:text-pearlWhite text-xl">
        <i class="ph-bold ph-x"></i>
      </button>

      <div class="flex items-center gap-2 mb-2">
        <i class="ph-bold ph-film-strip text-xl text-champagneLight"></i>
        <h3 class="font-serif text-2xl text-pearlWhite">Add New Memory Edit</h3>
      </div>
      <p class="text-xs text-pearlWhite/60 mb-5">
        Add another short video edit, montage, or funny candid memory.
      </p>

      <div class="space-y-3">
        <div>
          <label class="block text-xs uppercase tracking-wider text-pearlWhite/70 mb-1">Edit Title</label>
          <input type="text" id="newEditTitle" placeholder="e.g. Zoroko Memories" class="w-full bg-obsidian border border-pearlWhite/15 rounded-xl px-4 py-2 text-xs text-pearlWhite focus:border-champagne">
        </div>
        <div>
          <label class="block text-xs uppercase tracking-wider text-pearlWhite/70 mb-1">Vibe Tag</label>
          <input type="text" id="newEditTag" placeholder="e.g. Aesthetic, Cute, Date" class="w-full bg-obsidian border border-pearlWhite/15 rounded-xl px-4 py-2 text-xs text-pearlWhite focus:border-champagne">
        </div>
        <div>
          <label class="block text-xs uppercase tracking-wider text-pearlWhite/70 mb-1">Choose Local Video File</label>
          <input type="file" id="newEditFile" accept="video/*" class="w-full text-xs text-pearlWhite/70 file:mr-3 file:py-1.5 file:px-3 file:rounded-xl file:border-0 file:text-xs file:font-semibold file:bg-champagne/20 file:text-champagneLight hover:file:bg-champagne/30 cursor-pointer">
        </div>
        <div>
          <label class="block text-xs uppercase tracking-wider text-pearlWhite/70 mb-1">Or Direct Video URL</label>
          <input type="url" id="newEditUrl" placeholder="https://...mp4" class="w-full bg-obsidian border border-pearlWhite/15 rounded-xl px-4 py-2 text-xs text-pearlWhite focus:border-champagne">
        </div>
      </div>

      <div class="flex justify-end gap-3 mt-6">
        <button onclick="document.getElementById('newEditModal').classList.add('hidden')" class="px-4 py-2 text-xs text-pearlWhite/60 hover:text-pearlWhite">Cancel</button>
        <button onclick="saveNewVaultEdit()" class="px-5 py-2.5 rounded-xl bg-champagne text-obsidian text-xs font-semibold shadow-md">Add Edit</button>
      </div>
    </div>
  </div>

  <!-- 4. EDIT PREVIEW MODAL -->
  <div id="previewEditModal" class="fixed inset-0 bg-obsidian/90 backdrop-blur-2xl z-50 flex items-center justify-center p-4 sm:p-8 hidden" onclick="closeEditPreview(event)">
    <div class="max-w-4xl w-full glass-surface rounded-3xl overflow-hidden border border-champagne/40 relative shadow-2xl" onclick="event.stopPropagation()">
      <div class="flex items-center justify-between p-4 border-b border-pearlWhite/10 bg-nightVelvet">
        <h4 id="previewEditTitle" class="font-serif text-lg text-pearlWhite">Memory Edit</h4>
        <button onclick="closeEditPreview()" class="text-pearlWhite/60 hover:text-pearlWhite text-xl">
          <i class="ph-bold ph-x"></i>
        </button>
      </div>
      <!-- Dual Engine Player: Supports Google Drive Embed Preview & Direct HTML5 Video -->
      <div class="aspect-video bg-black flex items-center justify-center relative" id="previewPlayerContainer">
        <iframe id="previewDriveIframe" class="w-full h-full border-0 hidden" allow="autoplay; fullscreen" allowfullscreen></iframe>
        <video id="previewEditPlayer" playsinline controls class="w-full h-full object-contain hidden"></video>
      </div>
    </div>
  </div>

  <!-- 5. GOOGLE DRIVE BULK MANAGER MODAL -->
  <div id="bulkDriveModal" class="fixed inset-0 bg-obsidian/85 backdrop-blur-xl z-50 flex items-center justify-center p-4 hidden">
    <div class="glass-surface w-full max-w-2xl rounded-3xl p-6 sm:p-8 border border-champagne/40 relative shadow-2xl max-h-[90vh] flex flex-col">
      <button onclick="document.getElementById('bulkDriveModal').classList.add('hidden')" class="absolute top-5 right-5 text-pearlWhite/60 hover:text-pearlWhite text-xl">
        <i class="ph-bold ph-x"></i>
      </button>

      <div class="flex items-center gap-2.5 mb-2">
        <i class="ph-fill ph-google-drive-logo text-2xl text-champagneLight"></i>
        <h3 class="font-serif text-2xl text-pearlWhite">Google Drive Reels Manager</h3>
      </div>
      <p class="text-xs text-pearlWhite/65 mb-4">
        Paste your Google Drive share links below. Ensure your Drive files are set to 
        <strong class="text-champagneLight">"Anyone with the link can view"</strong>.
      </p>

      <div id="driveInputsList" class="space-y-2.5 overflow-y-auto pr-2 my-2 flex-1">
        <!-- Rendered inputs for Reels 1 to 8 -->
      </div>

      <div class="flex items-center justify-between pt-4 border-t border-pearlWhite/10 mt-2">
        <span class="text-[11px] text-pearlWhite/50 italic">Auto-converts view links to clean embeds</span>
        <div class="flex items-center gap-3">
          <button onclick="document.getElementById('bulkDriveModal').classList.add('hidden')" class="px-4 py-2 text-xs text-pearlWhite/60 hover:text-pearlWhite">Cancel</button>
          <button onclick="saveAllDriveLinks()" class="px-5 py-2.5 rounded-xl bg-champagne text-obsidian text-xs font-semibold shadow-md">Save All Links</button>
        </div>
      </div>
    </div>
  </div>

  <!-- ================= ROBUST LOGIC ================= -->
  <script>
    /* -------------------------------------------------------------
       0. MASTER PRIVACY GATE (ONLY ISHIKA CAN ENTER)
       Accepted key: "241105"
    -------------------------------------------------------------- */
    const ACCEPTED_MASTER_KEYS = ['241105'];

    function checkMasterPrivacy() {
      const isAlreadyUnlocked = sessionStorage.getItem('sanctuaryMasterUnlocked') === 'true';
      const screen = document.getElementById('masterPrivacyScreen');
      if (isAlreadyUnlocked && screen) {
        screen.classList.add('opacity-0', 'pointer-events-none');
        setTimeout(() => screen.classList.add('hidden'), 700);
      }
    }

    function unlockMasterPrivacy() {
      const input = document.getElementById('masterPasscodeInput');
      const feedback = document.getElementById('masterPassFeedback');
      const screen = document.getElementById('masterPrivacyScreen');
      if (!input) return;

      const cleaned = cleanAnswerString(input.value);
      if (ACCEPTED_MASTER_KEYS.includes(cleaned)) {
        if (feedback) {
          feedback.className = "text-xs font-semibold text-emerald-400 min-h-[1.25rem]";
          feedback.innerText = "Welcome home, Ishika... ✨";
        }
        sessionStorage.setItem('sanctuaryMasterUnlocked', 'true');
        playUnlockChime();
        triggerPetalConfetti();

        setTimeout(() => {
          if (screen) {
            screen.classList.add('opacity-0', 'pointer-events-none');
            setTimeout(() => screen.classList.add('hidden'), 700);
          }
        }, 600);
      } else {
        if (feedback) {
          feedback.className = "text-xs font-semibold text-crimsonGlow min-h-[1.25rem]";
          feedback.innerText = "Access denied. Only Ishika holds the key. 🌹";
        }
        input.value = '';
        const box = screen.querySelector('.glass-surface-lock');
        if (box) {
          box.classList.add('animate-bounce');
          setTimeout(() => box.classList.remove('animate-bounce'), 800);
        }
      }
    }

    /* -------------------------------------------------------------
       1. RELIABLE DATA & ULTRA-FLEXIBLE MATCHER
    -------------------------------------------------------------- */
    const CHAPTER_DATA = {
      1: {
        title: "Chapter One: The Recorded Film",
        hint: "If you don't get this, call me and say 'I Love You, I forgot the date, I owe you 1 Movie Date' 🎬❤️",
        // Target: 8 Feb 2025
        check: function(cleanInput) {
          if (!cleanInput) return false;
          // Must match 8 feb or variations
          const keywords = [
            '8feb2025', '8feb', '8february2025', '8february', 
            '8thfeb2025', '8thfeb', '8thfebruary2025', '8thfebruary',
            '08022025', '822025', '0802', '82'
          ];
          return keywords.some(k => cleanInput.includes(k) || k === cleanInput);
        }
      },
      2: {
        title: "Chapter Two: Our Story - A Poem for Ishika",
        hint: "If you need answer, You need to give me Sandwich! 🥪🍍",
        // Target: Pina Colada
        check: function(cleanInput) {
          if (!cleanInput) return false;
          const keywords = ['pinacolada', 'colada', 'pina'];
          return keywords.some(k => cleanInput.includes(k));
        }
      },
      3: {
        title: "Chapter Three: Captured Reels & Edits",
        hint: "I owe 1 kiss, if you can't Answer this! 💋🙈",
        // Target: 4 Jan 2026
        check: function(cleanInput) {
          if (!cleanInput) return false;
          const keywords = [
            '4jan2026', '4jan', '4january2026', '4january',
            '4thjan2026', '4thjan', '4thjanuary2026', '4thjanuary',
            '04012026', '412026', '0401', '41'
          ];
          return keywords.some(k => cleanInput.includes(k) || k === cleanInput);
        }
      },
      4: {
        title: "Chapter Four: The Final Secret & Letter",
        hint: "Lets go one more date at that place! 🍕✨",
        // Target: La Pino'z
        check: function(cleanInput) {
          if (!cleanInput) return false;
          const keywords = ['lapinoz', 'pinoz', 'lapino', 'pino'];
          return keywords.some(k => cleanInput.includes(k));
        }
      }
    };

    // Clean input function: lowercase, trim, remove all special characters, quotes, accents and spaces
    function cleanAnswerString(str) {
      if (!str) return '';
      return str
        .toLowerCase()
        .normalize("NFD").replace(/[\u0300-\u036f]/g, "") // remove accents (ñ -> n)
        .replace(/[^a-z0-9]/g, '') // strip all punctuation, spaces, quotes
        .trim();
    }

    // State
    let unlockedState = JSON.parse(localStorage.getItem('loveQuestUnlocked_v2')) || {
      ch1: false,
      ch2: false,
      ch3: false,
      ch4: false
    };

    function saveState() {
      localStorage.setItem('loveQuestUnlocked_v2', JSON.stringify(unlockedState));
      updateUI();
    }

    /* -------------------------------------------------------------
       2. DIRECT ANSWER SUBMISSION & HINT TOGGLING
    -------------------------------------------------------------- */
    function toggleHint(chapterNum) {
      const hintBox = document.getElementById(`hintBox${chapterNum}`);
      if (hintBox) {
        hintBox.classList.toggle('hidden');
      }
    }

    function submitDirectAnswer(chapterNum) {
      const input = document.getElementById(`answerInput${chapterNum}`);
      const feedback = document.getElementById(`feedbackText${chapterNum}`);
      const card = document.getElementById(`cardContainer${chapterNum}`);
      if (!input) return;

      const cleaned = cleanAnswerString(input.value);
      const chapter = CHAPTER_DATA[chapterNum];

      if (chapter && chapter.check(cleaned)) {
        // Correct Answer
        unlockedState[`ch${chapterNum}`] = true;
        saveState();

        if (feedback) {
          feedback.className = "text-xs font-semibold text-emerald-400 min-h-[1.25rem]";
          feedback.innerText = "Correct, my love! Unlocking chapter... ✨";
        }

        playUnlockChime();
        triggerPetalConfetti();

        // Smooth scroll to chapter
        setTimeout(() => {
          const el = document.getElementById(`chapter-${chapterNum}`);
          if (el) el.scrollIntoView({ behavior: 'smooth' });
        }, 300);
      } else {
        // Wrong Answer
        if (feedback) {
          feedback.className = "text-xs font-semibold text-crimsonGlow min-h-[1.25rem]";
          feedback.innerText = "Oops! Not quite, my love... Check the hint! 😉";
        }

        // Auto-reveal hint on failure
        const hintBox = document.getElementById(`hintBox${chapterNum}`);
        if (hintBox) hintBox.classList.remove('hidden');

        // Shake animation
        if (card) {
          card.classList.add('animate-bounce');
          setTimeout(() => card.classList.remove('animate-bounce'), 800);
        }
      }
    }

    function updateUI() {
      let count = 0;
      for (let i = 1; i <= 4; i++) {
        const isUnlocked = unlockedState[`ch${i}`];
        if (isUnlocked) count++;

        const lockView = document.getElementById(`lockView${i}`);
        const unlockedView = document.getElementById(`unlockedView${i}`);
        const badge = document.getElementById(`statusBadge${i}`);
        const chip = document.getElementById(`progChip${i}`);

        if (isUnlocked) {
          if (lockView) lockView.classList.add('hidden');
          if (unlockedView) unlockedView.classList.remove('hidden');
          if (badge) {
            badge.className = "px-3 py-1 rounded-full text-xs font-medium border border-emerald-500/30 text-emerald-400 bg-nightVelvet flex items-center gap-1.5";
            badge.innerHTML = `<i class="ph-fill ph-lock-key-open text-xs"></i> <span>Unlocked</span>`;
          }
          if (chip) {
            chip.className = "flex items-center gap-1 px-2.5 py-1 rounded-full bg-emerald-500/10 border border-emerald-500/30 text-emerald-300 font-medium";
            chip.querySelector('i').className = "ph-fill ph-check-circle text-[10px]";
          }
        } else {
          if (lockView) lockView.classList.remove('hidden');
          if (unlockedView) unlockedView.classList.add('hidden');
          if (badge) {
            badge.className = "px-3 py-1 rounded-full text-xs font-medium border border-roseMist/20 text-roseMist bg-nightVelvet flex items-center gap-1.5";
            badge.innerHTML = `<i class="ph-bold ph-lock text-xs"></i> <span>Locked</span>`;
          }
          if (chip) {
            chip.className = "flex items-center gap-1 px-2.5 py-1 rounded-full bg-obsidian border border-pearlWhite/10 text-pearlWhite/40";
            chip.querySelector('i').className = "ph-bold ph-lock text-[10px]";
          }
        }
      }

      // Progress bar
      const percent = (count / 4) * 100;
      document.getElementById('questProgressBar').style.width = percent + '%';
      document.getElementById('progressText').innerText = `${count} / 4 Unlocked`;
    }

    /* -------------------------------------------------------------
       5. EDITS VAULT: 8-PART CHRONOLOGICAL STORYLINE WITH DRIVE
    -------------------------------------------------------------- */
    // Helper function: Extracts Google Drive File ID from ANY link format
    function parseGoogleDriveId(url) {
      if (!url) return null;
      // Matches /d/{id}, id={id}, or direct file IDs
      const match = url.match(/(?:\/d\/|id=)([a-zA-Z0-9_-]{25,})/);
      return match ? match[1] : null;
    }

    // Convert link to playable embed or direct URL
    function formatDriveMedia(url) {
      const driveId = parseGoogleDriveId(url);
      if (driveId) {
        return {
          type: 'drive',
          embedUrl: `https://drive.google.com/file/d/${driveId}/preview?autoplay=1`,
          directUrl: `https://drive.google.com/uc?export=download&id=${driveId}`,
          id: driveId
        };
      }
      return {
        type: 'standard',
        url: url
      };
    }

    // Load custom drive links saved in localStorage if any
    const savedDriveLinks = JSON.parse(localStorage.getItem('ayushIshikaDriveReels') || '{}');

    let vaultEdits = [
      {
        id: 1,
        part: "Reel I",
        quote: "“Each one whispered, 'She looks at me'...”",
        driveUrl: savedDriveLinks[1] || "https://drive.google.com/file/d/1a0ZzBeQ4jAbGLMKC-TITYFCLFEuZuvuw/view?usp=drive_link",
        defaultFile: "edit1.mp4",
        url: "./edit1.mp4",
        thumb: "https://images.unsplash.com/photo-1529333166437-7750a6dd5a70?auto=format&fit=crop&w=700&q=80"
      },
      {
        id: 2,
        part: "Reel II",
        quote: "“A whisper sent through glowing light...”",
        driveUrl: savedDriveLinks[2] || "https://drive.google.com/file/d/1ESJ2WWaBI9u3mW62Vg99-q7FKgbofxm2/view?usp=drive_link",
        defaultFile: "edit2.mp4",
        url: "./edit2.mp4",
        thumb: "https://images.unsplash.com/photo-1516589178581-6cd7833ae3b2?auto=format&fit=crop&w=700&q=80"
      },
      {
        id: 3,
        part: "Reel III",
        quote: "“On the 4th, she returned to stage...”",
        driveUrl: savedDriveLinks[3] || "https://drive.google.com/file/d/1QlfxRAmqtn-bM_Dq1Y30aAqvfNUzcKfk/view?usp=drive_link",
        defaultFile: "edit3.mp4",
        url: "./edit3.mp4",
        thumb: "https://images.unsplash.com/photo-1518199266791-5375a83190b7?auto=format&fit=crop&w=700&q=80"
      },
      {
        id: 4,
        part: "Reel IV",
        quote: "“Sitting beside you, I gave you a rose...”",
        driveUrl: savedDriveLinks[4] || "https://drive.google.com/file/d/1w5-imJWXm_km2Lza3Lrrnen_ykfPy-EY/view?usp=drive_link",
        defaultFile: "edit4.mp4",
        url: "./edit4.mp4",
        thumb: "https://images.unsplash.com/photo-1492562080023-ab3db95bfbce?auto=format&fit=crop&w=700&q=80"
      },
      {
        id: 5,
        part: "Reel V",
        quote: "“A sudden kiss that made me softly fall...”",
        driveUrl: savedDriveLinks[5] || "https://drive.google.com/file/d/1WntNDyYSIG81ffQJ8XNfRzmW2N_Qbpdv/view?usp=drive_link",
        defaultFile: "edit5.mp4",
        url: "./edit5.mp4",
        thumb: "https://images.unsplash.com/photo-1511671782779-c97d3d27a1d4?auto=format&fit=crop&w=700&q=80"
      },
      {
        id: 6,
        part: "Reel VI",
        quote: "“Dropping you home was all I wanted then...”",
        driveUrl: savedDriveLinks[6] || "https://drive.google.com/file/d/1qpb7kwpB_pyWsP1j7nuZfzRWt3AI0uKT/view?usp=drive_link",
        defaultFile: "edit6.mp4",
        url: "./edit6.mp4",
        thumb: "https://images.unsplash.com/photo-1509198397868-475647b2a1e5?auto=format&fit=crop&w=700&q=80"
      },
      {
        id: 7,
        part: "Reel VII",
        quote: "“Sorting it out, that's what makes us best...”",
        driveUrl: savedDriveLinks[7] || "https://drive.google.com/file/d/1vT9LjjyOybKwUHWvTfclgWKZs8x9iSRc/view?usp=drive_link",
        defaultFile: "edit7.mp4",
        url: "./edit7.mp4",
        thumb: "https://images.unsplash.com/photo-1522673607200-164d1b6ce486?auto=format&fit=crop&w=700&q=80"
      },
      {
        id: 8,
        part: "Reel VIII",
        quote: "“I chose you then... I choose today.”",
        driveUrl: savedDriveLinks[8] || "https://drive.google.com/file/d/15X1rme81oW6pjCDVuzvn6rIFBqoGEHJO/view?usp=drive_link",
        defaultFile: "edit8.mp4",
        url: "./edit8.mp4",
        thumb: "https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=700&q=80"
      }
    ];

    function renderVaultEdits() {
      const grid = document.getElementById('editsVaultGrid');
      if (!grid) return;
      grid.innerHTML = '';

      vaultEdits.forEach((item, index) => {
        const isDriveLinked = Boolean(item.driveUrl && parseGoogleDriveId(item.driveUrl));
        const card = document.createElement('div');
        card.className = "glass-surface rounded-2xl overflow-hidden group border border-pearlWhite/10 hover:border-champagne/50 transition-all hover:-translate-y-1.5 flex flex-col justify-between";

        card.innerHTML = `
          <div>
            <div class="relative aspect-video overflow-hidden bg-obsidian cursor-pointer" onclick="openEditPreviewByIndex(${index})">
              <img src="${item.thumb}" alt="${item.part}" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700 opacity-75" onerror="this.src='https://placehold.co/600x400/120d18/d4af37?text=${item.part}'">
              <div class="absolute inset-0 bg-gradient-to-t from-obsidian via-obsidian/30 to-transparent"></div>
              
              <!-- Subtle Roman Numeral Badge -->
              <div class="absolute top-2.5 left-2.5 px-2.5 py-0.5 rounded-full text-[10px] font-mono tracking-widest uppercase font-bold bg-nightVelvet/90 border border-champagne/40 text-champagneLight backdrop-blur-md flex items-center gap-1">
                ${isDriveLinked ? '<i class="ph-fill ph-google-drive-logo text-emerald-400"></i>' : ''}
                <span>${item.part}</span>
              </div>

              <!-- Hover Play Button -->
              <div class="absolute inset-0 m-auto w-10 h-10 rounded-full bg-champagne/30 backdrop-blur-md border border-champagne text-pearlWhite flex items-center justify-center text-lg opacity-0 group-hover:opacity-100 transition-opacity shadow-lg">
                <i class="ph-fill ph-play ml-0.5"></i>
              </div>
            </div>

            <!-- Card Content: Intimate Quote Only -->
            <div class="p-3.5">
              <p class="text-xs font-serif italic text-pearlWhite/90 border-l border-champagne/30 pl-2 leading-relaxed">
                ${item.quote}
              </p>
            </div>
          </div>

          <!-- Drive Link & Local Pick Footer -->
          <div class="p-3 pt-0 border-t border-pearlWhite/5 mt-2 flex items-center justify-between gap-1 text-[10px]">
            <button onclick="promptSingleDriveLink(${index})" class="text-champagneLight hover:underline flex items-center gap-1">
              <i class="ph-fill ph-google-drive-logo text-xs"></i>
              <span>${isDriveLinked ? 'Edit Drive' : 'Set Drive'}</span>
            </button>
            <label class="text-pearlWhite/40 hover:text-pearlWhite cursor-pointer flex items-center gap-1">
              <i class="ph-bold ph-folder-open"></i>
              <span>Local</span>
              <input type="file" accept="video/*" class="hidden" onchange="handleSingleEditUpload(event, ${index})">
            </label>
          </div>
        `;
        grid.appendChild(card);
      });
    }

    function openEditPreviewByIndex(index) {
      const item = vaultEdits[index];
      const modal = document.getElementById('previewEditModal');
      const player = document.getElementById('previewEditPlayer');
      const iframe = document.getElementById('previewDriveIframe');
      
      document.getElementById('previewEditTitle').innerText = `${item.part}`;

      const activeUrl = item.driveUrl || item.url;
      const media = formatDriveMedia(activeUrl);

      if (media.type === 'drive') {
        // Use Google Drive iframe preview stream with autoplay
        if (player) {
          player.pause();
          player.src = '';
          player.classList.add('hidden');
        }
        iframe.src = media.embedUrl;
        iframe.classList.remove('hidden');
      } else {
        // Standard HTML5 video
        if (iframe) {
          iframe.src = '';
          iframe.classList.add('hidden');
        }
        player.src = activeUrl;
        player.classList.remove('hidden');
        player.load();
        
        // Autoplay on click with user gesture context
        const playPromise = player.play();
        if (playPromise !== undefined) {
          playPromise.catch(() => {
            // If browser autoplay policy requires mute first, retry muted then prompt
            player.muted = true;
            player.play().catch(() => {});
          });
        }
      }

      modal.classList.remove('hidden');
    }

    function promptSingleDriveLink(index) {
      const current = vaultEdits[index].driveUrl || "";
      const url = prompt(`Paste Google Drive sharing link for ${vaultEdits[index].part}:`, current);
      if (url !== null) {
        vaultEdits[index].driveUrl = url.trim();
        savedDriveLinks[index + 1] = url.trim();
        localStorage.setItem('ayushIshikaDriveReels', JSON.stringify(savedDriveLinks));
        renderVaultEdits();
        if (url.trim()) {
          triggerPetalConfetti();
          openEditPreviewByIndex(index);
        }
      }
    }

    function openBulkDriveModal() {
      const container = document.getElementById('driveInputsList');
      container.innerHTML = '';

      vaultEdits.forEach((edit, idx) => {
        const row = document.createElement('div');
        row.className = "flex flex-col sm:flex-row sm:items-center gap-2 p-2 rounded-xl bg-nightVelvet/60 border border-pearlWhite/10";
        row.innerHTML = `
          <div class="sm:w-28 text-xs font-mono font-semibold text-champagneLight flex items-center gap-1.5">
            <span class="w-5 h-5 rounded-full bg-champagne/20 flex items-center justify-center text-[10px]">${idx + 1}</span>
            <span>${edit.part}</span>
          </div>
          <input type="text" id="driveInputRow_${idx}" value="${edit.driveUrl || ''}" placeholder="https://drive.google.com/file/d/.../view?usp=sharing" class="flex-1 bg-obsidian border border-pearlWhite/15 rounded-lg px-3 py-1.5 text-xs text-pearlWhite focus:border-champagne focus:outline-none">
        `;
        container.appendChild(row);
      });

      document.getElementById('bulkDriveModal').classList.remove('hidden');
    }

    function saveAllDriveLinks() {
      vaultEdits.forEach((edit, idx) => {
        const inp = document.getElementById(`driveInputRow_${idx}`);
        if (inp) {
          const val = inp.value.trim();
          edit.driveUrl = val;
          savedDriveLinks[idx + 1] = val;
        }
      });
      localStorage.setItem('ayushIshikaDriveReels', JSON.stringify(savedDriveLinks));
      renderVaultEdits();
      document.getElementById('bulkDriveModal').classList.add('hidden');
      triggerPetalConfetti();
    }

    function closeEditPreview() {
      const player = document.getElementById('previewEditPlayer');
      const iframe = document.getElementById('previewDriveIframe');
      if (player) { 
        player.pause(); 
        player.currentTime = 0;
        player.src = ''; 
      }
      if (iframe) { 
        iframe.src = ''; 
      }
      const modal = document.getElementById('previewEditModal');
      if (modal) modal.classList.add('hidden');
    }

    function handleSingleEditUpload(event, index) {
      const file = event.target.files[0];
      if (file) {
        vaultEdits[index].url = URL.createObjectURL(file);
        vaultEdits[index].driveUrl = "";
        renderVaultEdits();
        triggerPetalConfetti();
        openEditPreviewByIndex(index);
      }
    }

    function promptEditLink(index) {
      const current = vaultEdits[index].url;
      const url = prompt(`Paste video URL for Reel ${index + 1}:`, current);
      if (url && url.trim()) {
        vaultEdits[index].url = url.trim();
        renderVaultEdits();
        openEditPreviewByIndex(index);
      }
    }

    function resetAllProgress() {
      unlockedState = { ch1: false, ch2: false, ch3: false, ch4: false };
      saveState();
      for (let i = 1; i <= 4; i++) {
        const inp = document.getElementById(`answerInput${i}`);
        if (inp) inp.value = '';
        const fb = document.getElementById(`feedbackText${i}`);
        if (fb) fb.innerText = '';
        const hb = document.getElementById(`hintBox${i}`);
        if (hb) hb.classList.add('hidden');
      }
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    /* -------------------------------------------------------------
       3. POEM NAVIGATION & FONT RESIZING
    -------------------------------------------------------------- */
    let poemFontSizeRem = 1.125;

    function adjustPoemFontSize(delta) {
      poemFontSizeRem = Math.max(0.9, Math.min(1.45, poemFontSizeRem + (delta * 0.08)));
      const manuscript = document.getElementById('fullPoemManuscript');
      if (manuscript) {
        manuscript.style.fontSize = `${poemFontSizeRem}rem`;
      }
    }

    function jumpToChapter(sectionId) {
      const target = document.getElementById(sectionId);
      const container = document.getElementById('fullPoemManuscript');
      if (target && container) {
        const topPos = target.offsetTop - container.offsetTop;
        container.scrollTo({ top: topPos - 10, behavior: 'smooth' });
        const select = document.getElementById('chapterNavSelect');
        if (select) select.value = sectionId;
      }
    }

    function scrollToTopPoem() {
      const container = document.getElementById('fullPoemManuscript');
      if (container) container.scrollTo({ top: 0, behavior: 'smooth' });
    }

    /* -------------------------------------------------------------
       4. VIDEO MANAGEMENT
    -------------------------------------------------------------- */
    function handleMainVideoFile(e) {
      const file = e.target.files[0];
      if (file) {
        const blobUrl = URL.createObjectURL(file);
        const heroVideo = document.getElementById('heroVideoElement');
        const heroSource = document.getElementById('heroVideoSource');
        const heroIframe = document.getElementById('heroDriveIframe');

        if (heroIframe) heroIframe.classList.add('hidden');
        if (heroVideo) {
          heroVideo.classList.remove('hidden');
          heroSource.src = blobUrl;
          heroVideo.load();
          heroVideo.play().catch(() => {});
        }
        document.getElementById('mainVideoHeading').innerText = file.name.replace(/\.[^/.]+$/, "");
        document.getElementById('videoUploadModal').classList.add('hidden');
        triggerPetalConfetti();
      }
    }

    function applyMainVideoUrl() {
      const url = document.getElementById('inputCustomVideoUrl').value.trim();
      const title = document.getElementById('inputCustomVideoTitle').value.trim();
      if (url) {
        const heroVideo = document.getElementById('heroVideoElement');
        const heroSource = document.getElementById('heroVideoSource');
        const heroIframe = document.getElementById('heroDriveIframe');

        const driveId = parseGoogleDriveId(url);
        if (driveId) {
          if (heroVideo) {
            heroVideo.pause();
            heroVideo.classList.add('hidden');
          }
          if (heroIframe) {
            heroIframe.src = `https://drive.google.com/file/d/${driveId}/preview?autoplay=1`;
            heroIframe.classList.remove('hidden');
          }
        } else {
          if (heroIframe) {
            heroIframe.src = '';
            heroIframe.classList.add('hidden');
          }
          if (heroVideo) {
            heroVideo.classList.remove('hidden');
            heroSource.src = url;
            heroVideo.load();
            heroVideo.play().catch(() => {});
          }
        }
        if (title) document.getElementById('mainVideoHeading').innerText = title;
        document.getElementById('videoUploadModal').classList.add('hidden');
        triggerPetalConfetti();
      }
    }

    function saveNewVaultEdit() {
      const title = document.getElementById('newEditTitle').value.trim() || "Memory Edit";
      const tag = document.getElementById('newEditTag').value.trim() || "Romantic";
      const urlInput = document.getElementById('newEditUrl').value.trim();
      const localFile = document.getElementById('newEditFile').files[0];

      let finalUrl = "https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/ForBiggerBlazes.mp4";
      if (localFile) {
        finalUrl = URL.createObjectURL(localFile);
      } else if (urlInput) {
        finalUrl = urlInput;
      }

      vaultEdits.unshift({
        id: Date.now(),
        part: `Reel ${vaultEdits.length + 1}`,
        title: title,
        subtitle: "A special moment together",
        quote: "“Loving you never feels like a task...”",
        tag: tag,
        defaultFile: localFile ? localFile.name : "custom.mp4",
        url: finalUrl,
        thumb: "https://images.unsplash.com/photo-1516589178581-6cd7833ae3b2?auto=format&fit=crop&w=700&q=80"
      });

      renderVaultEdits();
      document.getElementById('newEditModal').classList.add('hidden');
      triggerPetalConfetti();
    }

    /* -------------------------------------------------------------
       6. 3D LOVE LETTER FLIP
    -------------------------------------------------------------- */
    function toggleEnvelopeFlip() {
      const card = document.getElementById('envelopeFlipCard');
      card.classList.toggle('is-open');
      triggerPetalConfetti();
    }

    /* -------------------------------------------------------------
       7. AMBIENT PARTICLES (CANVAS)
    -------------------------------------------------------------- */
    const canvas = document.getElementById('starsCanvas');
    const ctx = canvas.getContext('2d');
    let width, height;
    let particles = [];

    function resizeCanvas() {
      width = canvas.width = window.innerWidth;
      height = canvas.height = window.innerHeight;
    }
    window.addEventListener('resize', resizeCanvas);
    resizeCanvas();

    class Particle {
      constructor() { this.reset(); }
      reset() {
        this.x = Math.random() * width;
        this.y = Math.random() * height;
        this.size = Math.random() * 2.5 + 1;
        this.speedX = Math.random() * 0.4 - 0.2;
        this.speedY = Math.random() * 0.5 + 0.2;
        this.opacity = Math.random() * 0.5 + 0.2;
        this.isGold = Math.random() > 0.45;
      }
      update() {
        this.x += this.speedX;
        this.y -= this.speedY;
        if (this.y < -10 || this.x < -10 || this.x > width + 10) {
          this.y = height + 10;
          this.x = Math.random() * width;
        }
      }
      draw() {
        ctx.beginPath();
        ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
        ctx.fillStyle = this.isGold ? `rgba(212, 175, 55, ${this.opacity})` : `rgba(232, 62, 92, ${this.opacity * 0.8})`;
        ctx.fill();
      }
    }

    for (let i = 0; i < 45; i++) particles.push(new Particle());

    function renderParticles() {
      ctx.clearRect(0, 0, width, height);
      particles.forEach(p => { p.update(); p.draw(); });
      requestAnimationFrame(renderParticles);
    }
    renderParticles();

    /* -------------------------------------------------------------
       8. GENTLE WEB AUDIO CHIME
    -------------------------------------------------------------- */
    let audioCtx = null;
    let isMelodyPlaying = false;
    let melodyTimer = null;
    const pentatonicScales = [261.63, 293.66, 329.63, 392.00, 440.00, 523.25, 659.25];

    function playMusicBoxChime(freq) {
      if (!audioCtx) return;
      try {
        const osc = audioCtx.createOscillator();
        const gain = audioCtx.createGain();
        osc.type = 'sine';
        osc.frequency.setValueAtTime(freq, audioCtx.currentTime);

        gain.gain.setValueAtTime(0.0001, audioCtx.currentTime);
        gain.gain.exponentialRampToValueAtTime(0.05, audioCtx.currentTime + 0.3);
        gain.gain.exponentialRampToValueAtTime(0.0001, audioCtx.currentTime + 2.8);

        osc.connect(gain);
        gain.connect(audioCtx.destination);

        osc.start();
        osc.stop(audioCtx.currentTime + 2.9);
      } catch (err) {}
    }

    function playUnlockChime() {
      if (!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
      if (audioCtx.state === 'suspended') audioCtx.resume();
      [523.25, 659.25, 783.99, 1046.50].forEach((freq, idx) => {
        setTimeout(() => playMusicBoxChime(freq), idx * 120);
      });
    }

    function toggleAudio() {
      if (!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
      if (audioCtx.state === 'suspended') audioCtx.resume();

      const btn = document.getElementById('audioToggleBtn');
      const icon = document.getElementById('audioIcon');
      const label = document.getElementById('audioLabel');

      if (!isMelodyPlaying) {
        isMelodyPlaying = true;
        icon.className = "ph-fill ph-speaker-high text-champagne animate-pulse";
        label.innerText = "Playing";
        melodyTimer = setInterval(() => {
          const note = pentatonicScales[Math.floor(Math.random() * pentatonicScales.length)];
          playMusicBoxChime(note);
        }, 1600);
      } else {
        isMelodyPlaying = false;
        clearInterval(melodyTimer);
        icon.className = "ph-bold ph-speaker-simple-slash";
        label.innerText = "Music";
      }
    }
    document.getElementById('audioToggleBtn').addEventListener('click', toggleAudio);

    /* -------------------------------------------------------------
       9. FALLBACK-SAFE CONFETTI
    -------------------------------------------------------------- */
    function triggerPetalConfetti() {
      if (window.confetti) {
        window.confetti({
          particleCount: 40,
          spread: 70,
          origin: { y: 0.75 },
          colors: ['#d4af37', '#fae392', '#e83e5c', '#fdfbf7']
        });
      }
    }

    // Init
    window.addEventListener('DOMContentLoaded', () => {
      checkMasterPrivacy();
      renderVaultEdits();
      updateUI();
    });
  </script>
</body>
</html>
