```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>Russo Read — The Art of Digital Reading</title>
  
  <!-- Tailwind CSS & FontAwesome Icons -->
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
  
  <!-- PDF.js Engine -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.min.js"></script>

  <!-- Google Fonts: Editorial Serif (Newsreader & Cinzel) + Modern Sans (Plus Jakarta Sans) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@500;600;700;800&family=Newsreader:ital,opsz,wght@0,6..72,300..700;1,6..72,300..600&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          fontFamily: {
            sans: ['"Plus Jakarta Sans"', 'sans-serif'],
            serif: ['"Newsreader"', 'Georgia', 'serif'],
            display: ['"Cinzel"', 'serif']
          },
          colors: {
            russo: {
              gold: '#C5A059',
              goldHover: '#D4AF37',
              noir: '#0D0E11',
              charcoal: '#17191E',
              card: '#1F2229',
              sand: '#F7F4EE',
              sepiaBg: '#F3EDE0',
              sepiaCard: '#FAF6EE',
              sepiaText: '#3B3024',
              sageBg: '#E9EFE9',
              sageCard: '#F2F6F2',
              sageText: '#1E2B20'
            }
          }
        }
      }
    };
  </script>

  <style>
    /* Custom Scrollbars */
    ::-webkit-scrollbar {
      width: 5px;
      height: 5px;
    }
    ::-webkit-scrollbar-track {
      background: transparent;
    }
    ::-webkit-scrollbar-thumb {
      background: rgba(140, 140, 140, 0.25);
      border-radius: 9999px;
    }
    ::-webkit-scrollbar-thumb:hover {
      background: rgba(140, 140, 140, 0.45);
    }

    /* Dynamic Theme Variables */
    body.theme-white {
      --bg-reader: #F9FAFB;
      --bg-page: #FFFFFF;
      --text-main: #18191C;
      --text-muted: #64748B;
      --border-color: rgba(0, 0, 0, 0.08);
      --toolbar-bg: rgba(255, 255, 255, 0.88);
      --card-shadow: 0 16px 36px -12px rgba(0, 0, 0, 0.08), 0 0 1px rgba(0, 0, 0, 0.12);
    }
    body.theme-sepia {
      --bg-reader: #EFE8DA;
      --bg-page: #FAF5E9;
      --text-main: #382D20;
      --text-muted: #7E6C58;
      --border-color: rgba(90, 70, 40, 0.12);
      --toolbar-bg: rgba(239, 232, 218, 0.92);
      --card-shadow: 0 16px 36px -12px rgba(60, 45, 20, 0.12), 0 0 1px rgba(60, 45, 20, 0.18);
    }
    body.theme-sage {
      --bg-reader: #DFE8E0;
      --bg-page: #ECF2ED;
      --text-main: #1D2B1F;
      --text-muted: #566E5A;
      --border-color: rgba(30, 50, 30, 0.1);
      --toolbar-bg: rgba(223, 232, 224, 0.92);
      --card-shadow: 0 16px 36px -12px rgba(30, 50, 30, 0.1), 0 0 1px rgba(30, 50, 30, 0.15);
    }
    body.theme-dark {
      --bg-reader: #131418;
      --bg-page: #1C1E24;
      --text-main: #E2E6EF;
      --text-muted: #8E96A6;
      --border-color: rgba(255, 255, 255, 0.08);
      --toolbar-bg: rgba(19, 20, 24, 0.9);
      --card-shadow: 0 20px 40px -10px rgba(0, 0, 0, 0.6);
    }
    body.theme-black {
      --bg-reader: #000000;
      --bg-page: #0B0B0C;
      --text-main: #D4D4D8;
      --text-muted: #71717A;
      --border-color: rgba(255, 255, 255, 0.05);
      --toolbar-bg: rgba(10, 10, 10, 0.95);
      --card-shadow: 0 20px 45px -10px rgba(0, 0, 0, 0.9);
    }

    /* Page Rendering Visuals */
    .pdf-page-card {
      background-color: var(--bg-page);
      box-shadow: var(--card-shadow);
      border: 1px solid var(--border-color);
      transition: box-shadow 0.3s ease, transform 0.2s ease;
    }
    .theme-dark .pdf-page-card canvas,
    .theme-black .pdf-page-card canvas {
      filter: invert(0.92) hue-rotate(180deg) brightness(0.95) contrast(0.92);
    }
    .theme-sepia .pdf-page-card canvas {
      filter: sepia(0.22) contrast(1.02);
    }
    .theme-sage .pdf-page-card canvas {
      filter: hue-rotate(20deg) brightness(0.98) sepia(0.12);
    }

    /* Chrome Animations */
    .reader-toolbar {
      transition: transform 0.32s cubic-bezier(0.16, 1, 0.3, 1), opacity 0.3s ease;
    }
    .reader-toolbar.is-hidden-top {
      transform: translateY(-110%);
      opacity: 0;
      pointer-events: none;
    }
    .reader-toolbar.is-hidden-bottom {
      transform: translateY(110%);
      opacity: 0;
      pointer-events: none;
    }

    /* Tap Margin Zones */
    .turn-zone {
      position: absolute;
      top: 60px;
      bottom: 70px;
      width: 14%;
      z-index: 25;
      cursor: pointer;
      opacity: 0;
      transition: opacity 0.2s ease;
    }
    .turn-zone:hover {
      opacity: 0.08;
      background: #000;
    }
  </style>
</head>

<body class="font-sans antialiased text-stone-900 bg-stone-50 select-none overflow-x-hidden transition-colors duration-300">

  <!-- Toast Center -->
  <div id="toast-deck" class="fixed top-5 right-5 z-[100] flex flex-col gap-2.5 pointer-events-none"></div>

  <!-- Confirmation Modal (Zero Native Alerts) -->
  <div id="confirm-modal" class="fixed inset-0 z-[110] hidden flex items-center justify-center bg-black/60 backdrop-blur-sm p-4 animate-in fade-in duration-200">
    <div class="bg-stone-900 border border-stone-800 text-stone-100 max-w-sm w-full p-6 rounded-3xl shadow-2xl space-y-4">
      <div class="w-12 h-12 rounded-2xl bg-amber-500/10 border border-amber-500/20 text-amber-400 flex items-center justify-center text-lg">
        <i class="fa-solid fa-triangle-exclamation"></i>
      </div>
      <div>
        <h4 id="confirm-title" class="font-serif text-lg font-bold text-white tracking-wide">Confirm Action</h4>
        <p id="confirm-desc" class="text-xs text-stone-400 mt-1 leading-relaxed">Are you sure you want to perform this action?</p>
      </div>
      <div class="flex items-center justify-end gap-3 pt-2">
        <button id="btn-confirm-cancel" class="px-4 py-2 rounded-xl text-xs font-semibold text-stone-400 hover:text-white hover:bg-stone-800 transition">Cancel</button>
        <button id="btn-confirm-ok" class="px-4 py-2 rounded-xl text-xs font-semibold bg-rose-600 hover:bg-rose-500 text-white transition shadow-lg shadow-rose-900/30">Delete</button>
      </div>
    </div>
  </div>

  <div id="app-viewport" class="min-h-screen flex flex-col relative">

    <!-- ======================================================== -->
    <!-- VIEW 1: RUSSO READ LIBRARY (THE CURATED SHELF)           -->
    <!-- ======================================================== -->
    <div id="view-library" class="flex-1 flex flex-col bg-[#0F1014] text-stone-200">
      
      <!-- Top Sophisticated Header -->
      <header class="border-b border-white/5 bg-[#0F1014]/90 backdrop-blur-md sticky top-0 z-30">
        <div class="max-w-7xl mx-auto px-4 sm:px-8 h-20 flex items-center justify-between">
          
          <!-- Logo & Brand Mark -->
          <div class="flex items-center gap-3.5">
            <div class="w-10 h-10 rounded-2xl bg-gradient-to-br from-amber-400 to-amber-600 flex items-center justify-center text-stone-950 font-serif font-black text-xl shadow-lg shadow-amber-500/20">
              R
            </div>
            <div>
              <span class="font-display text-lg font-bold tracking-widest uppercase text-stone-100 block leading-tight">Russo Read</span>
              <span class="text-[10px] tracking-widest text-amber-400/90 uppercase font-mono">Bibliotheque Edition</span>
            </div>
          </div>

          <!-- Header Actions -->
          <div class="flex items-center gap-3">
            <button id="btn-demo-book" class="hidden sm:inline-flex items-center gap-2 px-4 py-2 rounded-xl text-xs font-semibold bg-white/5 hover:bg-white/10 text-stone-300 border border-white/10 transition">
              <i class="fa-solid fa-sparkles text-amber-400"></i>
              <span>Classic Sample</span>
            </button>
            <label class="cursor-pointer inline-flex items-center gap-2 px-5 py-2.5 rounded-xl text-xs font-semibold bg-gradient-to-r from-amber-500 to-amber-600 hover:from-amber-400 hover:to-amber-500 text-stone-950 transition shadow-lg shadow-amber-500/20">
              <i class="fa-solid fa-feather-pointed"></i>
              <span>Add PDF</span>
              <input type="file" id="input-pdf-file" accept="application/pdf" class="hidden">
            </label>
          </div>
        </div>
      </header>

      <main class="flex-1 max-w-7xl w-full mx-auto px-4 sm:px-8 py-10">
        
        <!-- Hero Statement & Reading Stats -->
        <div class="relative overflow-hidden rounded-3xl p-8 sm:p-10 border border-white/10 bg-gradient-to-br from-[#16181F] via-[#121318] to-[#0A0B0E] mb-10 shadow-2xl">
          <div class="relative z-10 max-w-2xl">
            <span class="text-amber-400 font-mono text-[11px] tracking-widest uppercase font-semibold">Your Private Salon of Letters</span>
            <h1 class="font-serif text-3xl sm:text-4xl lg:text-5xl text-white font-medium tracking-tight mt-2 leading-[1.15]">
              Read without distractions, anywhere on earth.
            </h1>
            <p class="text-stone-400 text-xs sm:text-sm mt-3 leading-relaxed font-light">
              Russo Read preserves your documents inside your browser's private vault with automatic offline storage, customizable paper typography, and text-to-speech narrations.
            </p>
          </div>

          <div class="relative z-10 mt-8 flex flex-wrap items-center gap-4 text-xs">
            <div class="bg-white/5 border border-white/10 backdrop-blur-md px-5 py-3 rounded-2xl flex items-center gap-3">
              <i class="fa-solid fa-book-bookmark text-amber-400 text-base"></i>
              <div>
                <div id="stat-count-badge" class="font-bold text-white text-sm">0</div>
                <div class="text-[10px] text-stone-400 uppercase tracking-wider">Volumes In Library</div>
              </div>
            </div>
            <button id="btn-export-manifest" class="bg-white/5 hover:bg-white/10 border border-white/10 text-stone-300 px-4 py-3 rounded-2xl flex items-center gap-2 transition">
              <i class="fa-solid fa-download text-stone-400 text-xs"></i>
              <span>Export Catalog Info</span>
            </button>
          </div>

          <!-- Decorative Ambient Watermark -->
          <div class="absolute -right-12 -bottom-14 font-serif text-[180px] font-black text-white/[0.02] pointer-events-none select-none">
            RUSSO
          </div>
        </div>

        <!-- Filter & Search Controls -->
        <div class="flex flex-col sm:flex-row items-center justify-between gap-4 mb-8">
          <div class="relative w-full sm:w-96">
            <i class="fa-solid fa-magnifying-glass absolute left-4 top-1/2 -translate-y-1/2 text-stone-500 text-xs"></i>
            <input type="text" id="filter-search" placeholder="Search title or keywords..." class="w-full pl-10 pr-4 py-2.5 rounded-2xl bg-white/5 border border-white/10 text-xs text-white placeholder-stone-500 focus:outline-none focus:border-amber-400/50 transition">
          </div>
          
          <div class="flex items-center gap-2 self-end sm:self-auto text-xs text-stone-400">
            <span class="text-[11px] uppercase tracking-wider font-mono">Sort:</span>
            <select id="filter-sort" class="bg-white/5 border border-white/10 rounded-xl px-3 py-1.5 text-xs text-stone-300 focus:outline-none focus:border-amber-400">
              <option value="recent">Recently Read</option>
              <option value="title">Alphabetical</option>
              <option value="progress">Reading Progress</option>
            </select>
          </div>
        </div>

        <div id="grid-bookshelf" class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5 gap-6 sm:gap-8">
          <!-- Dynamically Injected Book Cards -->
        </div>

        <!-- Empty State Screen -->
        <div id="empty-state-card" class="hidden flex-col items-center justify-center py-20 text-center border border-dashed border-white/10 rounded-3xl bg-white/[0.02]">
          <div class="w-16 h-16 rounded-2xl bg-amber-400/10 border border-amber-400/20 text-amber-400 flex items-center justify-center text-2xl mb-4">
            <i class="fa-solid fa-book-open-reader"></i>
          </div>
          <h3 class="font-serif text-xl font-bold text-white">Your Reading Gallery Awaits</h3>
          <p class="text-xs text-stone-400 max-w-sm mt-1.5 leading-relaxed mb-6">
            Drop any PDF publication, literary essay, or book here to begin reading in pure editorial luxury.
          </p>
          <label class="cursor-pointer inline-flex items-center gap-2 px-5 py-2.5 rounded-xl text-xs font-semibold bg-amber-500 hover:bg-amber-400 text-stone-950 transition shadow-lg shadow-amber-500/20">
            <i class="fa-solid fa-plus"></i>
            <span>Select PDF Document</span>
            <input type="file" id="empty-file-input" accept="application/pdf" class="hidden">
          </label>
        </div>
      </main>
    </div>

    <!-- ======================================================== -->
    <!-- VIEW 2: IMMERSIVE SOPHISTICATED READER                   -->
    <!-- ======================================================== -->
    <div id="view-reader" class="hidden fixed inset-0 z-50 flex flex-col overflow-hidden select-none" style="background-color: var(--bg-reader);">

      <!-- TOP READER CHROME TOOLBAR -->
      <header id="reader-toolbar-top" class="reader-toolbar fixed top-0 left-0 right-0 z-50 h-16 border-b flex items-center justify-between px-4 sm:px-8 backdrop-blur-xl transition-all" style="background-color: var(--toolbar-bg); border-color: var(--border-color); color: var(--text-main);">
        
        <!-- Left: Back Button & Title -->
        <div class="flex items-center gap-3 overflow-hidden pr-4">
          <button id="btn-reader-back" class="w-9 h-9 rounded-xl flex items-center justify-center hover:bg-black/5 dark:hover:bg-white/10 transition" title="Return to Shelf (Esc)">
            <i class="fa-solid fa-arrow-left text-sm"></i>
          </button>
          <div class="truncate">
            <h2 id="reader-title-label" class="font-serif font-semibold text-sm sm:text-base truncate tracking-tight">Book Title</h2>
            <div id="reader-meta-label" class="text-[11px] opacity-60 font-mono tracking-tight">Page 1 of 1</div>
          </div>
        </div>

        <!-- Right Action Controls -->
        <div class="flex items-center gap-1 sm:gap-2">
          
          <!-- Fullscreen Toggle -->
          <button id="btn-fullscreen-toggle" class="p-2.5 rounded-xl hover:bg-black/5 dark:hover:bg-white/10 transition text-sm relative" title="Toggle Fullscreen (F)">
            <i id="fullscreen-icon" class="fa-solid fa-expand"></i>
          </button>

          <!-- TTS Read Aloud -->
          <button id="btn-tts-toggle" class="p-2.5 rounded-xl hover:bg-black/5 dark:hover:bg-white/10 transition text-sm relative" title="Listen Aloud (Speech)">
            <i id="tts-state-icon" class="fa-solid fa-volume-high"></i>
          </button>

          <!-- Bookmark Toggle -->
          <button id="btn-bookmark-toggle" class="p-2.5 rounded-xl hover:bg-black/5 dark:hover:bg-white/10 transition text-sm" title="Bookmark Page">
            <i id="reader-bookmark-icon" class="fa-regular fa-bookmark"></i>
          </button>

          <!-- Index & Chapters -->
          <button id="btn-toc-toggle" class="p-2.5 rounded-xl hover:bg-black/5 dark:hover:bg-white/10 transition text-sm" title="Chapters & Bookmarks">
            <i class="fa-solid fa-bars-staggered"></i>
          </button>

          <!-- Aesthetic & Layout Settings -->
          <button id="btn-settings-toggle" class="p-2.5 rounded-xl hover:bg-black/5 dark:hover:bg-white/10 transition text-sm" title="Typography & Palettes">
            <i class="fa-solid fa-sliders"></i>
          </button>
        </div>
      </header>

      <!-- Tap Zones for Flipping without showing toolbar -->
      <div id="zone-prev" class="turn-zone left-0" title="Previous Page"></div>
      <div id="zone-next" class="turn-zone right-0" title="Next Page"></div>

      <!-- Main Canvas Canvas Container -->
      <main id="reader-stage" class="flex-1 w-full overflow-y-auto overflow-x-hidden flex flex-col items-center justify-start py-20 px-2 sm:px-6 relative focus:outline-none" tabindex="0">
        
        <!-- Continuous or Single/Double Wrapper -->
        <div id="canvas-mount" class="flex flex-wrap items-center justify-center gap-6 max-w-full my-auto transition-transform duration-200">
          <!-- Dynamic Canvases -->
        </div>

        <!-- Sophisticated Page Loader -->
        <div id="canvas-loader" class="hidden absolute inset-0 flex items-center justify-center bg-black/15 backdrop-blur-[2px] z-30">
          <div class="px-5 py-3 rounded-2xl bg-stone-950/90 text-stone-100 text-xs font-semibold flex items-center gap-3 border border-white/10 shadow-2xl">
            <i class="fa-solid fa-compass fa-spin text-amber-400 text-sm"></i>
            <span>Rendering Page...</span>
          </div>
        </div>
      </main>

      <!-- Floating Audio Player Bar (active when speaking) -->
      <div id="tts-floater" class="hidden fixed top-20 left-1/2 -translate-x-1/2 z-50 bg-stone-900/95 border border-stone-800 text-stone-200 backdrop-blur-xl px-5 py-2.5 rounded-full shadow-2xl items-center gap-4 text-xs animate-in fade-in slide-in-from-top-4">
        <div class="flex items-center gap-2">
          <span class="w-2 h-2 rounded-full bg-amber-400 animate-ping"></span>
          <span class="font-mono text-[11px] text-amber-400 uppercase tracking-wider">Reading Aloud</span>
        </div>
        <div class="h-4 w-px bg-stone-700"></div>
        <button id="btn-tts-speed" class="font-mono text-[11px] text-stone-300 hover:text-white px-2 py-0.5 rounded bg-white/5 border border-white/10">1.0x</button>
        <button id="btn-tts-pause" class="hover:text-amber-400 transition" title="Pause / Resume">
          <i id="btn-tts-pause-icon" class="fa-solid fa-pause"></i>
        </button>
        <button id="btn-tts-close" class="hover:text-rose-400 transition" title="Stop Audio">
          <i class="fa-solid fa-xmark"></i>
        </button>
      </div>

      <!-- BOTTOM READER CHROME SCRUBBER -->
      <footer id="reader-toolbar-bottom" class="reader-toolbar fixed bottom-0 left-0 right-0 z-50 h-20 border-t flex flex-col justify-center px-4 sm:px-10 backdrop-blur-xl transition-all" style="background-color: var(--toolbar-bg); border-color: var(--border-color); color: var(--text-main);">
        <div class="max-w-2xl w-full mx-auto flex items-center gap-4">
          <button id="btn-prev-page" class="w-8 h-8 rounded-xl flex items-center justify-center hover:bg-black/5 dark:hover:bg-white/10 text-xs transition" title="Previous Page">
            <i class="fa-solid fa-chevron-left"></i>
          </button>

          <!-- Range Scrubber -->
          <div class="flex-1 flex flex-col justify-center">
            <input type="range" id="scrubber-slider" min="1" max="100" value="1" class="w-full accent-amber-500 cursor-pointer h-1.5 bg-black/10 rounded-lg appearance-none">
            <div class="flex justify-between items-center text-[10px] font-mono opacity-70 mt-1.5">
              <span id="scrubber-label-cur">Page 1</span>
              <span id="scrubber-label-pct" class="font-semibold text-amber-600 dark:text-amber-400">0%</span>
              <span id="scrubber-label-total">100 Pages</span>
            </div>
          </div>

          <button id="btn-next-page" class="w-8 h-8 rounded-xl flex items-center justify-center hover:bg-black/5 dark:hover:bg-white/10 text-xs transition" title="Next Page">
            <i class="fa-solid fa-chevron-right"></i>
          </button>
        </div>
      </footer>

      <!-- NAVIGATION DRAWER (Outline & Bookmarks) -->
      <aside id="drawer-contents" class="fixed top-0 bottom-0 left-0 w-80 max-w-[85vw] bg-stone-900 border-r border-stone-800 text-stone-100 z-50 transform -translate-x-full transition-transform duration-300 shadow-2xl flex flex-col">
        <div class="p-5 border-b border-stone-800 flex items-center justify-between">
          <div class="flex items-center gap-2.5">
            <i class="fa-solid fa-compass text-amber-400"></i>
            <h3 class="font-serif font-bold text-sm tracking-wide">Volume Index</h3>
          </div>
          <button id="btn-drawer-close" class="w-8 h-8 rounded-xl hover:bg-white/5 text-stone-400 hover:text-white flex items-center justify-center text-xs">
            <i class="fa-solid fa-xmark"></i>
          </button>
        </div>

        <div class="flex border-b border-stone-800 text-xs font-semibold">
          <button id="tab-toc" class="flex-1 py-3 text-center text-amber-400 border-b-2 border-amber-400">Contents</button>
          <button id="tab-bookmarks" class="flex-1 py-3 text-center text-stone-400 hover:text-white">Bookmarks</button>
        </div>

        <div class="flex-1 overflow-y-auto p-4">
          <div id="list-toc" class="space-y-1 text-xs">
            <p class="text-stone-500 text-center py-8">No structural table of contents found in this volume.</p>
          </div>
          <div id="list-bookmarks" class="hidden space-y-2 text-xs">
            <p class="text-stone-500 text-center py-8">No bookmarks yet.<br>Click the bookmark icon during reading to save key pages.</p>
          </div>
        </div>
      </aside>

      <!-- SETTINGS & DISPLAY DIALOG -->
      <div id="dialog-display" class="hidden fixed top-20 right-4 sm:right-8 w-80 bg-stone-900 border border-stone-800 text-stone-100 rounded-3xl shadow-2xl z-50 p-5 space-y-5 animate-in fade-in zoom-in-95 duration-150">
        <div class="flex items-center justify-between border-b border-stone-800 pb-3">
          <span class="text-[11px] font-mono uppercase tracking-widest text-stone-400">Typography & Atmosphere</span>
          <button id="btn-settings-close" class="text-stone-500 hover:text-white text-xs">
            <i class="fa-solid fa-xmark"></i>
          </button>
        </div>

        <!-- Themes -->
        <div>
          <label class="block text-xs font-medium text-stone-400 mb-2">Paper Hue</label>
          <div class="grid grid-cols-5 gap-2">
            <button data-theme="white" class="btn-theme-pill h-10 rounded-2xl bg-white border border-stone-200 text-stone-900 font-serif font-bold text-xs shadow-sm flex items-center justify-center">Aa</button>
            <button data-theme="sepia" class="btn-theme-pill h-10 rounded-2xl bg-[#FAF5E9] border border-[#E0D5BE] text-[#382D20] font-serif font-bold text-xs shadow-sm flex items-center justify-center">Aa</button>
            <button data-theme="sage" class="btn-theme-pill h-10 rounded-2xl bg-[#ECF2ED] border border-[#CCD8CD] text-[#1D2B1F] font-serif font-bold text-xs shadow-sm flex items-center justify-center">Aa</button>
            <button data-theme="dark" class="btn-theme-pill h-10 rounded-2xl bg-[#1C1E24] border border-stone-700 text-stone-200 font-serif font-bold text-xs shadow-sm flex items-center justify-center">Aa</button>
            <button data-theme="black" class="btn-theme-pill h-10 rounded-2xl bg-[#0B0B0C] border border-stone-800 text-stone-400 font-serif font-bold text-xs shadow-sm flex items-center justify-center">Aa</button>
          </div>
        </div>

        <!-- Layout Mode -->
        <div>
          <label class="block text-xs font-medium text-stone-400 mb-2">Layout Spacing</label>
          <div class="grid grid-cols-3 gap-1.5 p-1 bg-stone-950 rounded-2xl text-xs font-medium border border-stone-800">
            <button id="mode-single" class="py-2 rounded-xl bg-stone-800 text-white shadow-sm flex items-center justify-center gap-1.5">
              <i class="fa-regular fa-file"></i> 1-Up
            </button>
            <button id="mode-double" class="py-2 rounded-xl text-stone-400 hover:text-white flex items-center justify-center gap-1.5">
              <i class="fa-solid fa-book-open"></i> 2-Up
            </button>
            <button id="mode-scroll" class="py-2 rounded-xl text-stone-400 hover:text-white flex items-center justify-center gap-1.5">
              <i class="fa-solid fa-arrows-up-down"></i> Scroll
            </button>
          </div>
        </div>

        <!-- Scale / Zoom -->
        <div>
          <div class="flex justify-between items-center mb-1.5 text-xs">
            <label class="font-medium text-stone-400">Magnification</label>
            <span id="zoom-feedback" class="font-mono text-amber-400 font-bold">100%</span>
          </div>
          <div class="flex items-center gap-2">
            <button id="btn-zoom-out" class="w-8 h-8 rounded-xl bg-stone-800 hover:bg-stone-700 text-xs font-bold flex items-center justify-center">
              <i class="fa-solid fa-minus"></i>
            </button>
            <input type="range" id="zoom-range" min="50" max="250" value="100" step="5" class="flex-1 accent-amber-500 h-1.5 bg-stone-800 rounded-lg">
            <button id="btn-zoom-in" class="w-8 h-8 rounded-xl bg-stone-800 hover:bg-stone-700 text-xs font-bold flex items-center justify-center">
              <i class="fa-solid fa-plus"></i>
            </button>
            <button id="btn-zoom-auto" class="px-2.5 py-1.5 bg-stone-800 hover:bg-stone-700 rounded-xl text-[10px] font-semibold text-amber-400">Fit</button>
          </div>
        </div>
      </div>

      <!-- Backdrop Overlay -->
      <div id="drawer-backdrop" class="hidden fixed inset-0 bg-black/60 backdrop-blur-sm z-40 transition-opacity"></div>
    </div>
  </div>

  <script>
    /* PDF.js Global Worker Binding */
    pdfjsLib.GlobalWorkerOptions.workerSrc = 'https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.worker.min.js';

    /* Database Constants */
    const DB_NAME = 'RussoReadDB';
    const DB_VERSION = 1;
    const STORE_BOOKS = 'shelf';
    const STORE_BINARIES = 'binaries';

    let db = null;

    /* IndexedDB Init */
    function openDatabase() {
      return new Promise((resolve, reject) => {
        const req = indexedDB.open(DB_NAME, DB_VERSION);
        req.onupgradeneeded = (e) => {
          const d = e.target.result;
          if (!d.objectStoreNames.contains(STORE_BOOKS)) {
            d.createObjectStore(STORE_BOOKS, { keyPath: 'id' });
          }
          if (!d.objectStoreNames.contains(STORE_BINARIES)) {
            d.createObjectStore(STORE_BINARIES, { keyPath: 'id' });
          }
        };
        req.onsuccess = (e) => {
          db = e.target.result;
          resolve(db);
        };
        req.onerror = (e) => reject(e);
      });
    }

    async function storeBookRecord(meta, buffer) {
      return new Promise((resolve, reject) => {
        const tx = db.transaction([STORE_BOOKS, STORE_BINARIES], 'readwrite');
        tx.objectStore(STORE_BOOKS).put(meta);
        tx.objectStore(STORE_BINARIES).put({ id: meta.id, data: buffer });
        tx.oncomplete = () => resolve(true);
        tx.onerror = (e) => reject(e);
      });
    }

    async function fetchShelfRecords() {
      return new Promise((resolve, reject) => {
        const tx = db.transaction([STORE_BOOKS], 'readonly');
        const req = tx.objectStore(STORE_BOOKS).getAll();
        req.onsuccess = () => resolve(req.result || []);
        req.onerror = (e) => reject(e);
      });
    }

    async function fetchBinaryRecord(id) {
      return new Promise((resolve, reject) => {
        const tx = db.transaction([STORE_BINARIES], 'readonly');
        const req = tx.objectStore(STORE_BINARIES).get(id);
        req.onsuccess = () => resolve(req.result ? req.result.data : null);
        req.onerror = (e) => reject(e);
      });
    }

    async function updateBookMetaRecord(meta) {
      return new Promise((resolve, reject) => {
        const tx = db.transaction([STORE_BOOKS], 'readwrite');
        tx.objectStore(STORE_BOOKS).put(meta);
        tx.oncomplete = () => resolve(true);
        tx.onerror = (e) => reject(e);
      });
    }

    async function deleteBookRecord(id) {
      return new Promise((resolve, reject) => {
        const tx = db.transaction([STORE_BOOKS, STORE_BINARIES], 'readwrite');
        tx.objectStore(STORE_BOOKS).delete(id);
        tx.objectStore(STORE_BINARIES).delete(id);
        tx.oncomplete = () => resolve(true);
        tx.onerror = (e) => reject(e);
      });
    }

    const state = {
      shelf: [],
      activeBook: null,
      pdf: null,
      page: 1,
      total: 0,
      zoom: 1.0,
      autoFit: true,
      layout: 'single', // 'single', 'double', 'scroll'
      theme: 'sepia',
      outline: [],
      chromeVisible: true,
      isFullscreen: false,
      speech: {
        active: false,
        paused: false,
        rate: 1.0,
        utterance: null
      },
      touch: { startX: 0, startY: 0 }
    };

    /* Non-Intrusive Toast System */
    function notify(text, variant = 'info') {
      const deck = document.getElementById('toast-deck');
      const toast = document.createElement('div');
      
      const badge = {
        success: 'fa-circle-check text-amber-400',
        error: 'fa-circle-xmark text-rose-400',
        info: 'fa-bookmark text-amber-400'
      }[variant] || 'fa-circle-info text-amber-400';

      toast.className = 'pointer-events-auto flex items-center gap-3 px-4 py-3 rounded-2xl bg-stone-900 border border-stone-800 text-stone-100 text-xs font-medium shadow-2xl transition-all duration-300 translate-y-3 opacity-0';
      toast.innerHTML = `<i class="fa-solid ${badge}"></i> <span>${text}</span>`;
      
      deck.appendChild(toast);
      requestAnimationFrame(() => toast.classList.remove('translate-y-3', 'opacity-0'));

      setTimeout(() => {
        toast.classList.add('translate-y-3', 'opacity-0');
        setTimeout(() => toast.remove(), 320);
      }, 3400);
    }

    /* Custom Confirm Dialog (Replaces confirm()) */
    let confirmCallback = null;
    function promptConfirm(title, desc, onConfirm) {
      const modal = document.getElementById('confirm-modal');
      document.getElementById('confirm-title').textContent = title;
      document.getElementById('confirm-desc').textContent = desc;
      confirmCallback = onConfirm;
      modal.classList.remove('hidden');
    }

    async function processUploadedPdf(file) {
      if (!file || file.type !== 'application/pdf') {
        notify("Please provide a valid PDF volume", "error");
        return;
      }

      notify(`Importing "${file.name}"...`, "info");

      try {
        const buffer = await file.arrayBuffer();
        const loadTask = pdfjsLib.getDocument({ data: buffer.slice(0) });
        const doc = await loadTask.promise;
        const total = doc.numPages;

        // Generate Cover Snapshot from Page 1
        const p1 = await doc.getPage(1);
        const viewport = p1.getViewport({ scale: 0.35 });
        const canvas = document.createElement('canvas');
        const ctx = canvas.getContext('2d');
        canvas.width = viewport.width;
        canvas.height = viewport.height;
        await p1.render({ canvasContext: ctx, viewport }).promise;
        const coverUrl = canvas.toDataURL('image/jpeg', 0.82);

        const cleanTitle = file.name.replace(/\.pdf$/i, '').replace(/[_-]/g, ' ');

        const meta = {
          id: 'russo_' + Date.now() + '_' + Math.random().toString(36).substr(2, 6),
          title: cleanTitle,
          fileName: file.name,
          fileSize: (file.size / (1024 * 1024)).toFixed(1) + ' MB',
          totalPages: total,
          currentPage: 1,
          progress: 0,
          cover: coverUrl,
          bookmarks: [],
          updatedAt: Date.now()
        };

        await storeBookRecord(meta, buffer);
        await refreshShelf();
        notify(`Added "${cleanTitle}" to Russo Read`, "success");
        openReader(meta.id);
      } catch (err) {
        console.error("PDF Parsing failure:", err);
        notify("Unable to render this PDF file", "error");
      }
    }

    async function refreshShelf() {
      state.shelf = await fetchShelfRecords();
      const grid = document.getElementById('grid-bookshelf');
      const emptyState = document.getElementById('empty-state-card');
      const countBadge = document.getElementById('stat-count-badge');

      countBadge.textContent = state.shelf.length;

      if (state.shelf.length === 0) {
        grid.innerHTML = '';
        emptyState.classList.remove('hidden');
        emptyState.classList.add('flex');
        return;
      }

      emptyState.classList.add('hidden');
      emptyState.classList.remove('flex');

      const sortVal = document.getElementById('filter-sort').value;
      const searchVal = document.getElementById('filter-search').value.toLowerCase().trim();

      let books = state.shelf.filter(b => b.title.toLowerCase().includes(searchVal));

      if (sortVal === 'recent') {
        books.sort((a, b) => (b.updatedAt || 0) - (a.updatedAt || 0));
      } else if (sortVal === 'title') {
        books.sort((a, b) => a.title.localeCompare(b.title));
      } else if (sortVal === 'progress') {
        books.sort((a, b) => (b.progress || 0) - (a.progress || 0));
      }

      grid.innerHTML = books.map(b => `
        <div class="group relative flex flex-col bg-[#16181F] rounded-3xl border border-white/5 hover:border-amber-400/30 shadow-xl hover:-translate-y-1.5 transition-all duration-300 overflow-hidden cursor-pointer" onclick="openReader('${b.id}')">
          <div class="relative w-full aspect-[3/4.2] bg-[#111216] overflow-hidden flex items-center justify-center">
            ${b.cover 
              ? `<img src="${b.cover}" alt="${b.title}" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105">`
              : `<div class="p-6 text-center text-stone-600"><i class="fa-solid fa-book-bookmark text-3xl mb-2"></i><div class="text-[10px] uppercase font-mono">No Preview</div></div>`
            }

            <!-- Delete Trigger -->
            <button onclick="event.stopPropagation(); requestBookRemoval('${b.id}', '${sanitizeQuotes(b.title)}')" class="absolute top-3 right-3 w-8 h-8 rounded-full bg-stone-900/80 hover:bg-rose-600 text-stone-300 hover:text-white backdrop-blur-md opacity-0 group-hover:opacity-100 transition-all flex items-center justify-center text-xs shadow-lg" title="Delete volume">
              <i class="fa-solid fa-trash-can"></i>
            </button>

            <!-- Progress Tag -->
            <div class="absolute bottom-3 left-3 px-2.5 py-1 rounded-full bg-stone-950/80 backdrop-blur-md border border-white/10 text-[10px] font-mono text-amber-400">
              ${b.progress || 0}% read
            </div>
          </div>

          <div class="p-4 flex flex-col flex-1 justify-between">
            <div>
              <h4 class="font-serif font-semibold text-stone-200 text-sm line-clamp-2 leading-snug group-hover:text-amber-400 transition-colors">
                ${b.title}
              </h4>
              <p class="text-[11px] font-mono text-stone-500 mt-1 flex items-center gap-1.5">
                <span>${b.totalPages}p</span>
                <span>•</span>
                <span>${b.fileSize || 'PDF'}</span>
              </p>
            </div>

            <!-- Reading progress bar -->
            <div class="mt-4 w-full bg-stone-800 rounded-full h-1 overflow-hidden">
              <div class="bg-amber-400 h-1 rounded-full transition-all duration-300" style="width: ${b.progress || 0}%"></div>
            </div>
          </div>
        </div>
      `).join('');
    }

    function sanitizeQuotes(str) {
      return (str || '').replace(/'/g, "\\'").replace(/"/g, '&quot;');
    }

    function requestBookRemoval(id, title) {
      promptConfirm(
        "Remove Volume",
        `Do you wish to remove "${title}" from your personal shelf?`,
        async () => {
          await deleteBookRecord(id);
          notify("Book removed from library", "info");
          refreshShelf();
        }
      );
    }

    async function openReader(bookId) {
      const book = state.shelf.find(b => b.id === bookId);
      if (!book) return;

      state.activeBook = book;
      state.page = book.currentPage || 1;

      document.getElementById('view-library').classList.add('hidden');
      document.getElementById('view-reader').classList.remove('hidden');
      applyTheme(state.theme);

      document.getElementById('reader-title-label').textContent = book.title;
      toggleLoader(true);

      try {
        const binary = await fetchBinaryRecord(bookId);
        if (!binary) throw new Error("Binary stream missing");

        const loadingTask = pdfjsLib.getDocument({ data: binary });
        state.pdf = await loadingTask.promise;
        state.total = state.pdf.numPages;

        // Extract TOC Outline
        try {
          state.outline = (await state.pdf.getOutline()) || [];
          renderOutlineTree();
        } catch(e) {
          state.outline = [];
        }

        renderBookmarksList();
        updateBookmarkIndicator();

        const scrubber = document.getElementById('scrubber-slider');
        scrubber.min = 1;
        scrubber.max = state.total;
        scrubber.value = state.page;

        await renderPageSpread();
      } catch (err) {
        console.error("Reader boot error:", err);
        notify("Failed to initialize PDF reader", "error");
        exitReader();
      } finally {
        toggleLoader(false);
      }
    }

    function exitReader() {
      haltAudioSpeech();
      if (state.activeBook) {
        state.activeBook.currentPage = state.page;
        state.activeBook.progress = Math.round((state.page / state.total) * 100);
        state.activeBook.updatedAt = Date.now();
        updateBookMetaRecord(state.activeBook);
      }

      if (document.fullscreenElement) {
        document.exitFullscreen().catch(() => {});
      }

      document.getElementById('view-reader').classList.add('hidden');
      document.getElementById('view-library').classList.remove('hidden');
      state.pdf = null;
      state.activeBook = null;
      refreshShelf();
    }

    async function renderPageSpread() {
      if (!state.pdf) return;
      const mount = document.getElementById('canvas-mount');
      mount.innerHTML = '';
      toggleLoader(true);

      try {
        if (state.layout === 'scroll') {
          const maxToLoad = Math.min(state.total, 35);
          for (let i = 1; i <= maxToLoad; i++) {
            await renderSinglePageCanvas(i, mount);
          }
        } else if (state.layout === 'double' && window.innerWidth >= 900) {
          let p1 = state.page;
          let p2 = (state.page + 1 <= state.total) ? state.page + 1 : null;
          await renderSinglePageCanvas(p1, mount);
          if (p2) await renderSinglePageCanvas(p2, mount);
        } else {
          await renderSinglePageCanvas(state.page, mount);
        }

        updateScrubberMetrics();
      } catch (err) {
        console.error("Rendering error:", err);
      } finally {
        toggleLoader(false);
      }
    }

    async function renderSinglePageCanvas(pageNumber, target) {
      const page = await state.pdf.getPage(pageNumber);
      const stageWidth = document.getElementById('reader-stage').clientWidth;
      const originalViewport = page.getViewport({ scale: 1.0 });

      let scale = state.zoom;
      if (state.autoFit) {
        let availableWidth = stageWidth - 56;
        if (state.layout === 'double' && window.innerWidth >= 900) {
          availableWidth = (availableWidth / 2) - 28;
        }
        scale = Math.min((availableWidth / originalViewport.width), 1.65);
        state.zoom = scale;
        document.getElementById('zoom-range').value = Math.round(scale * 100);
        document.getElementById('zoom-feedback').textContent = Math.round(scale * 100) + '%';
      }

      const viewport = page.getViewport({ scale });
      const dpr = window.devicePixelRatio || 1;

      const card = document.createElement('div');
      card.className = 'pdf-page-card rounded-2xl relative overflow-hidden flex flex-col items-center';
      card.id = `page-card-${pageNumber}`;

      const canvas = document.createElement('canvas');
      const ctx = canvas.getContext('2d');

      canvas.width = Math.floor(viewport.width * dpr);
      canvas.height = Math.floor(viewport.height * dpr);
      canvas.style.width = `${Math.floor(viewport.width)}px`;
      canvas.style.height = `${Math.floor(viewport.height)}px`;

      const renderCtx = {
        canvasContext: ctx,
        transform: [dpr, 0, 0, dpr, 0, 0],
        viewport: viewport
      };

      await page.render(renderCtx).promise;

      const folio = document.createElement('div');
      folio.className = 'text-[10px] font-mono py-2 opacity-50 tracking-wider';
      folio.textContent = `${pageNumber}`;

      card.appendChild(canvas);
      card.appendChild(folio);
      target.appendChild(card);
    }

    function updateScrubberMetrics() {
      const cur = state.page;
      const total = state.total;
      const pct = Math.round((cur / total) * 100);

      document.getElementById('reader-meta-label').textContent = `Page ${cur} of ${total} • ${pct}%`;
      document.getElementById('scrubber-label-cur').textContent = `Page ${cur}`;
      document.getElementById('scrubber-label-pct').textContent = `${pct}% Read`;
      document.getElementById('scrubber-label-total').textContent = `${total} Pages`;
      document.getElementById('scrubber-slider').value = cur;

      if (state.activeBook) {
        state.activeBook.currentPage = cur;
        state.activeBook.progress = pct;
        updateBookMetaRecord(state.activeBook);
      }

      updateBookmarkIndicator();
    }

    function toggleLoader(visible) {
      const el = document.getElementById('canvas-loader');
      if (visible) el.classList.remove('hidden');
      else el.classList.add('hidden');
    }

    function advancePage() {
      const inc = (state.layout === 'double' && window.innerWidth >= 900) ? 2 : 1;
      if (state.page + inc <= state.total) {
        state.page += inc;
        renderPageSpread();
      } else if (state.page < state.total) {
        state.page = state.total;
        renderPageSpread();
      }
    }

    function retreatPage() {
      const dec = (state.layout === 'double' && window.innerWidth >= 900) ? 2 : 1;
      if (state.page - dec >= 1) {
        state.page -= dec;
        renderPageSpread();
      } else if (state.page > 1) {
        state.page = 1;
        renderPageSpread();
      }
    }

    function jumpToPage(num) {
      const p = parseInt(num, 10);
      if (p >= 1 && p <= state.total) {
        state.page = p;
        renderPageSpread();
      }
    }

    function toggleFullscreenMode() {
      const icon = document.getElementById('fullscreen-icon');
      if (!document.fullscreenElement) {
        document.documentElement.requestFullscreen().then(() => {
          state.isFullscreen = true;
          icon.className = 'fa-solid fa-compress';
          notify("Fullscreen enabled", "info");
        }).catch(() => {
          notify("Fullscreen not permitted by browser", "error");
        });
      } else {
        document.exitFullscreen().then(() => {
          state.isFullscreen = false;
          icon.className = 'fa-solid fa-expand';
        }).catch(() => {});
      }
    }

    function applyTheme(name) {
      state.theme = name;
      document.body.className = document.body.className.replace(/theme-\w+/g, '');
      document.body.classList.add(`theme-${name}`);

      document.querySelectorAll('.btn-theme-pill').forEach(btn => {
        if (btn.dataset.theme === name) {
          btn.classList.add('ring-2', 'ring-amber-500', 'ring-offset-2', 'ring-offset-stone-900');
        } else {
          btn.classList.remove('ring-2', 'ring-amber-500', 'ring-offset-2', 'ring-offset-stone-900');
        }
      });
    }

    function toggleChromeBars(force) {
      state.chromeVisible = (force !== undefined) ? force : !state.chromeVisible;
      const topBar = document.getElementById('reader-toolbar-top');
      const bottomBar = document.getElementById('reader-toolbar-bottom');

      if (state.chromeVisible) {
        topBar.classList.remove('is-hidden-top');
        bottomBar.classList.remove('is-hidden-bottom');
      } else {
        topBar.classList.add('is-hidden-top');
        bottomBar.classList.add('is-hidden-bottom');
        document.getElementById('dialog-display').classList.add('hidden');
      }
    }

    function updateBookmarkIndicator() {
      const icon = document.getElementById('reader-bookmark-icon');
      const isBookmarked = state.activeBook && state.activeBook.bookmarks && state.activeBook.bookmarks.includes(state.page);
      if (isBookmarked) {
        icon.className = 'fa-solid fa-bookmark text-amber-500';
      } else {
        icon.className = 'fa-regular fa-bookmark';
      }
    }

    function toggleBookmarkRecord() {
      if (!state.activeBook) return;
      if (!state.activeBook.bookmarks) state.activeBook.bookmarks = [];

      const idx = state.activeBook.bookmarks.indexOf(state.page);
      if (idx > -1) {
        state.activeBook.bookmarks.splice(idx, 1);
        notify(`Bookmark cleared from page ${state.page}`, "info");
      } else {
        state.activeBook.bookmarks.push(state.page);
        state.activeBook.bookmarks.sort((a, b) => a - b);
        notify(`Bookmarked page ${state.page}`, "success");
      }

      updateBookmarkIndicator();
      renderBookmarksList();
      updateBookMetaRecord(state.activeBook);
    }

    function renderBookmarksList() {
      const list = document.getElementById('list-bookmarks');
      const marks = (state.activeBook && state.activeBook.bookmarks) || [];

      if (marks.length === 0) {
        list.innerHTML = `<p class="text-stone-500 text-center py-8">No bookmarks yet.<br>Click the bookmark icon during reading to save key pages.</p>`;
        return;
      }

      list.innerHTML = marks.map(p => `
        <div class="flex items-center justify-between p-3 rounded-2xl bg-white/5 hover:bg-white/10 transition cursor-pointer" onclick="jumpToPage(${p}); toggleDrawer(false);">
          <div class="flex items-center gap-2.5">
            <i class="fa-solid fa-bookmark text-amber-400"></i>
            <span class="font-medium text-stone-200">Page ${p}</span>
          </div>
          <button onclick="event.stopPropagation(); removeBookmarkIndex(${p})" class="text-stone-500 hover:text-rose-400 p-1">
            <i class="fa-solid fa-xmark"></i>
          </button>
        </div>
      `).join('');
    }

    function removeBookmarkIndex(p) {
      if (!state.activeBook) return;
      state.activeBook.bookmarks = state.activeBook.bookmarks.filter(b => b !== p);
      updateBookmarkIndicator();
      renderBookmarksList();
      updateBookMetaRecord(state.activeBook);
    }

    function renderOutlineTree() {
      const container = document.getElementById('list-toc');
      if (!state.outline || state.outline.length === 0) {
        container.innerHTML = `<p class="text-stone-500 text-center py-8">No structural table of contents found in this volume.</p>`;
        return;
      }

      function buildNodes(items) {
        return items.map(item => `
          <div class="py-0.5">
            <button class="w-full text-left py-2 px-3 rounded-xl hover:bg-white/5 text-stone-300 font-medium text-xs flex items-center justify-between transition" onclick="jumpToOutline('${item.dest}'); toggleDrawer(false);">
              <span class="truncate pr-2">${item.title}</span>
              <i class="fa-solid fa-chevron-right text-[10px] text-stone-600"></i>
            </button>
            ${item.items && item.items.length > 0 ? `<div class="pl-3 border-l border-stone-800 ml-3 mt-1">${buildNodes(item.items)}</div>` : ''}
          </div>
        `).join('');
      }

      container.innerHTML = buildNodes(state.outline);
    }

    async function jumpToOutline(dest) {
      if (!dest || !state.pdf) return;
      try {
        let target = dest;
        if (typeof dest === 'string') {
          target = await state.pdf.getDestination(dest);
        }
        if (Array.isArray(target) && target.length > 0) {
          const pageIdx = await state.pdf.getPageIndex(target[0]);
          jumpToPage(pageIdx + 1);
        }
      } catch(e) {
        console.error("Outline leap error:", e);
      }
    }

    function toggleDrawer(force) {
      const drawer = document.getElementById('drawer-contents');
      const backdrop = document.getElementById('drawer-backdrop');
      const isOpen = !drawer.classList.contains('-translate-x-full');
      const show = (force !== undefined) ? force : !isOpen;

      if (show) {
        drawer.classList.remove('-translate-x-full');
        backdrop.classList.remove('hidden');
      } else {
        drawer.classList.add('-translate-x-full');
        backdrop.classList.add('hidden');
      }
    }

    async function toggleTextToSpeech() {
      if (state.speech.active) {
        haltAudioSpeech();
        notify("Audio narrative stopped", "info");
        return;
      }

      if (!('speechSynthesis' in window)) {
        notify("Text-to-Speech unsupported on this browser", "error");
        return;
      }

      notify("Synthesizing page content...", "info");

      try {
        const page = await state.pdf.getPage(state.page);
        const textContent = await page.getTextContent();
        const extracted = textContent.items.map(i => i.str).join(' ');

        if (!extracted.trim()) {
          notify("No selectable text on page (may be a scanned image)", "error");
          return;
        }

        haltAudioSpeech();

        const utterance = new SpeechSynthesisUtterance(extracted);
        utterance.rate = state.speech.rate;
        utterance.pitch = 1.0;

        utterance.onstart = () => {
          state.speech.active = true;
          state.speech.paused = false;
          document.getElementById('tts-state-icon').className = 'fa-solid fa-volume-high text-amber-500 fa-beat-fade';
          document.getElementById('tts-floater').classList.remove('hidden');
          document.getElementById('tts-floater').classList.add('flex');
          document.getElementById('btn-tts-pause-icon').className = 'fa-solid fa-pause';
        };

        utterance.onend = () => haltAudioSpeech();
        utterance.onerror = () => haltAudioSpeech();

        state.speech.utterance = utterance;
        window.speechSynthesis.speak(utterance);
      } catch(e) {
        console.error("Audio failure:", e);
        notify("Audio playback encountered an issue", "error");
        haltAudioSpeech();
      }
    }

    function haltAudioSpeech() {
      if (window.speechSynthesis) {
        window.speechSynthesis.cancel();
      }
      state.speech.active = false;
      state.speech.paused = false;
      document.getElementById('tts-state-icon').className = 'fa-solid fa-volume-high';
      document.getElementById('tts-floater').classList.add('hidden');
      document.getElementById('tts-floater').classList.remove('flex');
    }

    function makeSamplePdfDocument() {
      const source = `%PDF-1.4
1 0 obj << /Type /Catalog /Pages 2 0 R >> endobj
2 0 obj << /Type /Pages /Kids [3 0 R 4 0 R 5 0 R] /Count 3 >> endobj
3 0 obj << /Type /Page /Parent 2 0 R /MediaBox [0 0 612 792] /Resources << /Font << /F1 6 0 R >> >> /Contents 7 0 R >> endobj
4 0 obj << /Type /Page /Parent 2 0 R /MediaBox [0 0 612 792] /Resources << /Font << /F1 6 0 R >> >> /Contents 8 0 R >> endobj
5 0 obj << /Type /Page /Parent 2 0 R /MediaBox [0 0 612 792] /Resources << /Font << /F1 6 0 R >> >> /Contents 9 0 R >> endobj
6 0 obj << /Type /Font /Subtype /Type1 /BaseFont /Times-Roman >> endobj
7 0 obj << /Length 300 >> stream
BT
/F1 28 Tf
70 700 Td
(Russo Read) Tj
/F1 14 Tf
0 -36 Td
(The Sophisticated Reader for Modern Scholars) Tj
/F1 11 Tf
0 -40 Td
(Welcome to Russo Read, an editorial e-reading environment.) Tj
0 -22 Td
(Designed for deep focus, typography appreciation, and private storage.) Tj
0 -30 Td
(Features at your fingertips:) Tj
0 -20 Td
(1. Press 'F' or click the maximize icon to enter distraction-free Fullscreen.) Tj
0 -20 Td
(2. Switch between Paper White, Warm Sepia, Sage, Charcoal, and OLED Black.) Tj
0 -20 Td
(3. Listen to any page aloud using the built-in Text-To-Speech narration.) Tj
0 -20 Td
(4. Your books remain 100% saved on your computer or phone privately.) Tj
0 -35 Td
(Turn the page to continue reading.) Tj
ET
endstream endobj
8 0 obj << /Length 260 >> stream
BT
/F1 20 Tf
70 700 Td
(Chapter I: The Sanctuary of Letters) Tj
/F1 11 Tf
0 -35 Td
(To read is to fly: it is to soar to a point of vantage which gives a view) Tj
0 -20 Td
(over wide terrains of history, human thought, and poetic invention.) Tj
0 -30 Td
(Russo Read has been crafted with zero dependencies on external servers.) Tj
0 -20 Td
(You can host this standalone file on GitHub Pages and use it forever,) Tj
0 -20 Td
(synchronizing your readings on mobile, desktop, and tablet devices.) Tj
ET
endstream endobj
9 0 obj << /Length 230 >> stream
BT
/F1 20 Tf
70 700 Td
(Chapter II: Keyboard Navigation Guide) Tj
/F1 11 Tf
0 -35 Td
(- Right Arrow / Spacebar / J: Advance page) Tj
0 -20 Td
(- Left Arrow / K: Return to previous page) Tj
0 -20 Td
(- F: Enter and exit Fullscreen) Tj
0 -20 Td
(- Escape: Return to your bookshelf) Tj
0 -20 Td
(- Center Click: Hide and show toolbars) Tj
0 -35 Td
(Happy Reading with Russo Read.) Tj
ET
endstream endobj
xref
0 10
0000000000 65535 f 
0000000010 00000 n 
0000000060 00000 n 
0000000135 00000 n 
0000000257 00000 n 
0000000379 00000 n 
0000000501 00000 n 
0000000572 00000 n 
0000000925 00000 n 
0000001238 00000 n 
trailer << /Size 10 /Root 1 0 R >>
startxref
1521
%%EOF`;
      const enc = new TextEncoder();
      return enc.encode(source).buffer;
    }

    async function loadSampleBook() {
      notify("Generating Russo Read sample volume...", "info");
      const buffer = makeSamplePdfDocument();
      const blob = new Blob([buffer], { type: 'application/pdf' });
      const sampleFile = new File([blob], "Russo_Read_Handbook.pdf", { type: 'application/pdf' });
      await processUploadedPdf(sampleFile);
    }

    function initializeInteractions() {
      // Ingestion Listeners
      const inputPrimary = document.getElementById('input-pdf-file');
      const inputEmpty = document.getElementById('empty-file-input');

      inputPrimary.addEventListener('change', (e) => {
        if (e.target.files[0]) processUploadedPdf(e.target.files[0]);
      });
      inputEmpty.addEventListener('change', (e) => {
        if (e.target.files[0]) processUploadedPdf(e.target.files[0]);
      });

      // Sample book trigger
      document.getElementById('btn-demo-book').addEventListener('click', loadSampleBook);

      // Search & Sorting
      document.getElementById('filter-search').addEventListener('input', refreshShelf);
      document.getElementById('filter-sort').addEventListener('change', refreshShelf);

      // Reader Top Bar
      document.getElementById('btn-reader-back').addEventListener('click', exitReader);
      document.getElementById('btn-fullscreen-toggle').addEventListener('click', toggleFullscreenMode);
      document.getElementById('btn-tts-toggle').addEventListener('click', toggleTextToSpeech);
      document.getElementById('btn-bookmark-toggle').addEventListener('click', toggleBookmarkRecord);
      document.getElementById('btn-toc-toggle').addEventListener('click', () => toggleDrawer(true));
      document.getElementById('btn-drawer-close').addEventListener('click', () => toggleDrawer(false));
      document.getElementById('drawer-backdrop').addEventListener('click', () => toggleDrawer(false));

      // Settings Dialog
      document.getElementById('btn-settings-toggle').addEventListener('click', () => {
        document.getElementById('dialog-display').classList.toggle('hidden');
      });
      document.getElementById('btn-settings-close').addEventListener('click', () => {
        document.getElementById('dialog-display').classList.add('hidden');
      });

      // Confirm Modal buttons
      document.getElementById('btn-confirm-cancel').addEventListener('click', () => {
        document.getElementById('confirm-modal').classList.add('hidden');
        confirmCallback = null;
      });
      document.getElementById('btn-confirm-ok').addEventListener('click', () => {
        document.getElementById('confirm-modal').classList.add('hidden');
        if (confirmCallback) confirmCallback();
        confirmCallback = null;
      });

      // Fullscreen change listener to sync icons
      document.addEventListener('fullscreenchange', () => {
        const icon = document.getElementById('fullscreen-icon');
        if (document.fullscreenElement) {
          icon.className = 'fa-solid fa-compress';
        } else {
          icon.className = 'fa-solid fa-expand';
        }
      });

      // Scrubber and Controls
      document.getElementById('btn-prev-page').addEventListener('click', retreatPage);
      document.getElementById('btn-next-page').addEventListener('click', advancePage);
      document.getElementById('scrubber-slider').addEventListener('input', (e) => {
        document.getElementById('scrubber-label-cur').textContent = `Page ${e.target.value}`;
      });
      document.getElementById('scrubber-slider').addEventListener('change', (e) => {
        jumpToPage(e.target.value);
      });

      // Tap Zones
      document.getElementById('zone-prev').addEventListener('click', (e) => {
        e.stopPropagation();
        retreatPage();
      });
      document.getElementById('zone-next').addEventListener('click', (e) => {
        e.stopPropagation();
        advancePage();
      });

      // Canvas click hides/shows toolbars
      document.getElementById('reader-stage').addEventListener('click', (e) => {
        if (!e.target.closest('button') && !e.target.closest('input')) {
          toggleChromeBars();
        }
      });

      // Palette themes
      document.querySelectorAll('.btn-theme-pill').forEach(btn => {
        btn.addEventListener('click', () => applyTheme(btn.dataset.theme));
      });

      // Layout mode changes
      document.getElementById('mode-single').addEventListener('click', () => {
        state.layout = 'single';
        state.autoFit = true;
        renderPageSpread();
      });
      document.getElementById('mode-double').addEventListener('click', () => {
        state.layout = 'double';
        state.autoFit = true;
        renderPageSpread();
      });
      document.getElementById('mode-scroll').addEventListener('click', () => {
        state.layout = 'scroll';
        state.autoFit = true;
        renderPageSpread();
      });

      // Zoom Controls
      document.getElementById('zoom-range').addEventListener('input', (e) => {
        state.autoFit = false;
        state.zoom = parseFloat(e.target.value) / 100;
        document.getElementById('zoom-feedback').textContent = e.target.value + '%';
        renderPageSpread();
      });
      document.getElementById('btn-zoom-in').addEventListener('click', () => {
        state.autoFit = false;
        state.zoom = Math.min(state.zoom + 0.15, 2.5);
        document.getElementById('zoom-range').value = Math.round(state.zoom * 100);
        document.getElementById('zoom-feedback').textContent = Math.round(state.zoom * 100) + '%';
        renderPageSpread();
      });
      document.getElementById('btn-zoom-out').addEventListener('click', () => {
        state.autoFit = false;
        state.zoom = Math.max(state.zoom - 0.15, 0.5);
        document.getElementById('zoom-range').value = Math.round(state.zoom * 100);
        document.getElementById('zoom-feedback').textContent = Math.round(state.zoom * 100) + '%';
        renderPageSpread();
      });
      document.getElementById('btn-zoom-auto').addEventListener('click', () => {
        state.autoFit = true;
        renderPageSpread();
      });

      // Audio Floater Controls
      document.getElementById('btn-tts-close').addEventListener('click', haltAudioSpeech);
      document.getElementById('btn-tts-pause').addEventListener('click', () => {
        if (!window.speechSynthesis) return;
        if (state.speech.paused) {
          window.speechSynthesis.resume();
          state.speech.paused = false;
          document.getElementById('btn-tts-pause-icon').className = 'fa-solid fa-pause';
        } else {
          window.speechSynthesis.pause();
          state.speech.paused = true;
          document.getElementById('btn-tts-pause-icon').className = 'fa-solid fa-play';
        }
      });
      document.getElementById('btn-tts-speed').addEventListener('click', () => {
        const speeds = [1.0, 1.25, 1.5, 0.85];
        const next = speeds[(speeds.indexOf(state.speech.rate) + 1) % speeds.length];
        state.speech.rate = next;
        document.getElementById('btn-tts-speed').textContent = `${next}x`;
        if (state.speech.active) {
          haltAudioSpeech();
          toggleTextToSpeech();
        }
      });

      // TOC Tabs
      document.getElementById('tab-toc').addEventListener('click', () => {
        document.getElementById('tab-toc').className = 'flex-1 py-3 text-center text-amber-400 border-b-2 border-amber-400';
        document.getElementById('tab-bookmarks').className = 'flex-1 py-3 text-center text-stone-400 hover:text-white';
        document.getElementById('list-toc').classList.remove('hidden');
        document.getElementById('list-bookmarks').classList.add('hidden');
      });
      document.getElementById('tab-bookmarks').addEventListener('click', () => {
        document.getElementById('tab-bookmarks').className = 'flex-1 py-3 text-center text-amber-400 border-b-2 border-amber-400';
        document.getElementById('tab-toc').className = 'flex-1 py-3 text-center text-stone-400 hover:text-white';
        document.getElementById('list-bookmarks').classList.remove('hidden');
        document.getElementById('list-toc').classList.add('hidden');
      });

      // Keyboard Controls
      window.addEventListener('keydown', (e) => {
        if (document.getElementById('view-reader').classList.contains('hidden')) return;

        if (e.key === 'ArrowRight' || e.key === ' ' || e.key === 'j') {
          advancePage();
        } else if (e.key === 'ArrowLeft' || e.key === 'k') {
          retreatPage();
        } else if (e.key === 'Escape') {
          toggleDrawer(false);
          document.getElementById('dialog-display').classList.add('hidden');
        } else if (e.key === 'f' || e.key === 'F') {
          toggleFullscreenMode();
        }
      });

      // Drag and Drop
      window.addEventListener('dragover', (e) => e.preventDefault());
      window.addEventListener('drop', (e) => {
        e.preventDefault();
        if (e.dataTransfer.files && e.dataTransfer.files[0]) {
          processUploadedPdf(e.dataTransfer.files[0]);
        }
      });

      // Export catalog metadata
      document.getElementById('btn-export-manifest').addEventListener('click', () => {
        const manifest = state.shelf.map(b => ({
          title: b.title,
          fileName: b.fileName,
          totalPages: b.totalPages,
          progress: b.progress,
          bookmarks: b.bookmarks
        }));
        const blob = new Blob([JSON.stringify(manifest, null, 2)], { type: 'application/json' });
        const url = URL.createObjectURL(blob);
        const a = document.createElement('a');
        a.href = url;
        a.download = `russo_read_catalog_${new Date().toISOString().slice(0,10)}.json`;
        a.click();
        URL.revokeObjectURL(url);
        notify("Reading catalog exported", "success");
      });

      // Mobile Touch Swipes
      const view = document.getElementById('view-reader');
      view.addEventListener('touchstart', (e) => {
        state.touch.startX = e.changedTouches[0].screenX;
        state.touch.startY = e.changedTouches[0].screenY;
      }, { passive: true });

      view.addEventListener('touchend', (e) => {
        const endX = e.changedTouches[0].screenX;
        const endY = e.changedTouches[0].screenY;
        const diffX = endX - state.touch.startX;
        const diffY = endY - state.touch.startY;

        if (Math.abs(diffX) > 55 && Math.abs(diffY) < 60) {
          if (diffX < 0) advancePage();
          else retreatPage();
        }
      }, { passive: true });
    }

    window.addEventListener('DOMContentLoaded', async () => {
      try {
        await openDatabase();
        initializeInteractions();
        await refreshShelf();
        if (state.shelf.length === 0) {
          notify("Welcome to Russo Read. Select a volume or click Classic Sample to begin.", "info");
        }
      } catch(err) {
        console.error("Initialization failure:", err);
      }
    });
  </script>
</body>
</html>
```
