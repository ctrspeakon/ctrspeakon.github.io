
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <title>@ctrspeakon</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com "></script>
  <style>
    body.dark {
      --tw-bg-opacity: 1;
      background-color: #1a1a1a;
      --tw-text-opacity: 1;
      color: #f3f3f3;
    }

    body.dark .bg-red-800 {
      background-color: #2d2d2d !important;
    }

    body.dark .bg-red-700 {
      background-color: #444 !important;
    }

    body.dark .text-gray-300 {
      color: #ccc !important;
    }

    .hover\:scale-105:hover {
      transform: scale(1.02);
    }

    .transition-all {
      transition-property: all;
      transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
      transition-duration: 300ms;
    }

    /* Animación de entrada */
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .fade-in {
      animation: fadeIn 1s ease forwards;
      opacity: 0;
    }

    .delay-1 {
      animation-delay: 0.3s;
    }

    .delay-2 {
      animation-delay: 0.5s;
    }

    .delay-3 {
      animation-delay: 0.7s;
    }
  </style>
</head>
<body class="min-h-screen flex items-center justify-center p-4 bg-red-900 text-white dark:bg-gray-900 dark:text-white">

  <!-- Botones de control -->
  <div class="absolute top-3 left-3 space-x-2 z-10 fade-in delay-1">
    <button onclick="toggleLang()" id="langBtn" class="bg-gray-800 text-white px-3 py-1 rounded-full text-sm hover:bg-gray-700 transition-transform">ES / EN</button>
    <button onclick="toggleDarkMode()" id="darkBtn" class="bg-gray-800 text-white px-3 py-1 rounded-full text-sm hover:bg-gray-700 transition-transform">🌙 Modo Oscuro</button>
  </div>

  <!-- Contenedor principal -->
  <div class="max-w-md w-full rounded-2xl overflow-hidden shadow-xl bg-red-800 dark:bg-gray-800 transition-all duration-300 transform hover:scale-105 fade-in delay-2">

    <!-- Avatar -->
    <div class="flex justify-center pt-6 fade-in delay-1">
      <img 
        src="https://i.postimg.cc/9FKJsqzq/logo.png "
        alt="Perfil"
        class="w-24 h-24 rounded-full border-4 border-white object-cover shadow-lg"
      />
    </div>

    <!-- Información -->
    <div class="px-6 pt-4 pb-6 text-center fade-in delay-2">
      <h1 class="text-2xl font-bold">@ctrspeakon</h1>
      <p id="bio" class="mt-1 text-gray-300">Bienvenidos a mi mundo digital 👀</p>

      <!-- Botón teléfono -->
      <button onclick="mostrarTelefono()" id="phoneBtn" class="mt-4 py-2 px-4 rounded-xl bg-red-700 text-white inline-block text-sm hover:bg-red-600 hover:scale-105 transition-transform duration-300 fade-in delay-3">
        📞 Mostrar Teléfono
      </button>

      <!-- Número de teléfono oculto por defecto -->
      <div id="telefono" class="hidden mt-2 py-2 px-4 rounded-xl bg-red-700 dark:bg-gray-700 text-white inline-block mx-auto hover:scale-105 transition-transform duration-300">
        +solo de emergencia
      </div>

      <!-- Enlaces sociales - Ordenados alfabéticamente -->
      <div class="mt-6 space-y-3 fade-in delay-3">

        <!-- Instagram -->
        <a href="https://instagram.com/ctrtorrez " target="_blank" rel="noopener noreferrer" class="block py-3 px-4 rounded-xl font-medium text-white text-center no-underline bg-gradient-to-r from-pink-500 via-red-500 to-yellow-500 hover:scale-105 hover:shadow-md transition-all duration-300">
          <svg viewBox="0 0 24 24" class="w-6 h-6 inline mr-2 fill-current">
            <circle cx="12" cy="12" r="10" fill="#E1306C" />
            <path d="M12 7.5a4.5 4.5 0 100 9 4.5 4.5 0 000-9z" fill="white" />
            <circle cx="18" cy="6" r="1" fill="white" />
          </svg>
          Instagram
        </a>

        <!-- Facebook -->
        <a href="https://facebook.com/ctrtorrez " target="_blank" rel="noopener noreferrer" class="block py-3 px-4 rounded-xl font-medium text-white text-center no-underline bg-blue-700 hover:bg-blue-800 hover:scale-105 hover:shadow-md transition-all duration-300">
          <svg viewBox="0 0 24 24" class="w-6 h-6 inline mr-2 fill-current" fill="white">
            <path d="M24 12.073c0-6.627-5.373-12-12-12S0 5.446 0 12.073c0 5.99 4.388 10.954 10.106 11.852V16.16H7.15v-3.46h2.955V9.85c0-2.906 1.72-4.513 4.4-4.513 1.26 0 2.653.22 2.653.22V8.27H15.8c-1.486 0-1.813.92-1.813 1.793v2.21h3.627l-.589 3.46V24C19.612 19.4 24 14.025 24 12.073z" />
          </svg>
          Facebook
        </a>

        <!-- Telegram -->
        <a href="https://t.me/ctrspeakon " target="_blank" rel="noopener noreferrer" class="block py-3 px-4 rounded-xl font-medium text-white text-center no-underline bg-blue-500 hover:bg-blue-600 hover:scale-105 hover:shadow-md transition-all duration-300">
          <svg viewBox="0 0 24 24" class="w-6 h-6 inline mr-2 fill-current" fill="white">
            <path d="M20.5 9.17a.5.5 0 0 0-.31-.12c-4.3-1.4-10.6-3.3-10.6-3.3a.5.5 0 0 0-.25.23l-3.18 10.6a.5.5 0 0 0 .2.62l.03.02a.5.5 0 0 0 .16.08c4.3 1.4 8.1 2.6 8.1 2.6a.5.5 0 0 0 .4-.15l5.7-4.1a.5.5 0 0 0 .09-.78l-.02-.02a.5.5 0 0 0-.15-.1z" fill="white" />
          </svg>
          Telegram
        </a>

        <!-- TikTok -->
        <a href="https://tiktok.com/@ctrtorrez" target="_blank" rel="noopener noreferrer" class="block py-3 px-4 rounded-xl font-medium text-white text-center no-underline bg-black hover:bg-gray-900 hover:scale-105 hover:shadow-md transition-all duration-300">
          <svg viewBox="0 0 24 24" class="w-6 h-6 inline mr-2 fill-current" fill="white">
            <path d="M12.52 0c1.31 0 2.61.01 3.91.02-.01 1.53-.62 3.09-1.78 4.17-1.15 1.11-2.75 1.71-4.34 1.71v4.03c1.89 0 3.79-.72 5.25-2.18.98-.98 1.7-2.19 2.29-3.44l.13-.32 3.97.42-3.92 5.14c.25.35.44.74.77 1.03.34.29.77.42 1.22.39.41-.03.86-.21 1.16-.51.32-.31.45-.72.5-1.16l-.62-6.8c-.06-.57-.11-1.14-.11-1.72 0-.58.05-1.15.11-1.71l.61-6.76c.06-.61.13-1.21.24-1.81.12-.64.31-1.26.55-1.86.25-.64.59-1.22 1.06-1.7l1.03-1.05c.06-.06.11-.12.21-.24-.12 0-.24 0-.35-.02-.32-.02-.65-.01-.97-.01zm-6.99 6.46c.02 1.9-1.54 3.43-3.44 3.45-1.89.02-3.42-1.5-3.44-3.4-.02-1.88 1.51-3.41 3.4-3.44 1.89-.02 3.43 1.48 3.46 3.39z" fill="white" />
          </svg>
          TikTok
        </a>

        <!-- Twitter / X -->
        <a href="https://x.com/ctrspeakon " target="_blank" rel="noopener noreferrer" class="block py-3 px-4 rounded-xl font-medium text-white text-center no-underline bg-black hover:bg-gray-900 hover:scale-105 hover:shadow-md transition-all duration-300">
          <svg viewBox="0 0 24 24" class="w-6 h-6 inline mr-2 fill-current" fill="currentColor">
            <path d="M23.954 4.569c-.885.389-1.83.654-2.825.775 1.014-.611 1.794-1.574 2.163-2.723-.951.555-2.005.959-3.127 1.184-.896-.959-2.173-1.559-3.591-1.559-2.717 0-4.92 2.203-4.92 4.917 0 .39.045.765.127 1.124C7.691 8.094 4.066 6.13 1.64 3.161c-.427.722-.666 1.561-.666 2.475 0 1.71.87 3.213 2.188 4.096-.807-.026-1.566-.248-2.228-.616v.061c0 2.385 1.693 4.374 3.946 4.827-.413.111-.849.171-1.296.171-.314 0-.615-.03-.916-.086.631 1.953 2.445 3.377 4.604 3.417-1.68 1.319-3.809 2.105-6.102 2.105-.39 0-.779-.023-1.17-.067 2.189 1.394 4.768 2.209 7.557 2.209 9.054 0 13.999-7.496 13.999-13.986 0-.209 0-.42-.015-.63.961-.689 1.8-1.56 2.46-2.548l-.047-.02z" />
          </svg>
          Twitter / X
        </a>

        <!-- YouTube -->
        <a href="https://youtube.com/@ctrspeakon" target="_blank" rel="noopener noreferrer" class="block py-3 px-4 rounded-xl font-medium text-white text-center no-underline bg-red-600 hover:bg-red-700 hover:scale-105 hover:shadow-md transition-all duration-300">
          <svg viewBox="0 0 24 24" class="w-6 h-6 inline mr-2 fill-current" fill="currentColor">
            <path d="M23.498 6.186a3.016 3.016 0 0 0-2.122-2.136C19.505 3.545 12 3.545 12 3.545S4.495 3.545 2.625 4.05A3.017 3.017 0 0 0 .502 6.186C0 8.07 0 12 0 12s.502 3.93 1.424 5.814a3.016 3.016 0 0 0 2.122 2.136c1.871.505 9.376.505 9.376.505s7.505 0 9.377-.505a3.015 3.015 0 0 0 2.122-2.136C24 15.93 24 12 24 12s0-3.93-.502-5.814zM9.545 15.568V8.432L15.818 12l-6.273 3.568z" fill="currentColor" />
          </svg>
          YouTube
        </a>

      </div>

      <!-- Footer -->
      <footer class="mt-6 text-center text-sm text-gray-400 border-t border-red-900 pt-3">
        &copy; 2025 CTRSPEAKON. Todos los derechos reservados.
      </footer>
    </div>
  </div>


<!-- Script funcional -->
<script>
  const texts = {
    es: {
      bio: "Bienvenidos a mi mundo digital 👀",
      showPhoneBtn: "📞 Mostrar Teléfono",
      hidePhoneBtn: "❌ Ocultar Teléfono"
    },
    en: {
      bio: "Welcome to my digital world 👀",
      showPhoneBtn: "📞 Show Phone",
      hidePhoneBtn: "❌ Hide Phone"
    }
  };

  let currentLang = 'es';

  function toggleLang() {
    currentLang = currentLang === 'es' ? 'en' : 'es';
    document.getElementById('bio').textContent = texts[currentLang].bio;
    document.getElementById('phoneBtn').textContent = document.getElementById('telefono').style.display === 'block'
      ? texts[currentLang].hidePhoneBtn
      : texts[currentLang].showPhoneBtn;
    document.getElementById('langBtn').textContent = currentLang === 'es' ? 'EN / ES' : 'ES / EN';
  }

  function mostrarTelefono() {
    const telefono = document.getElementById('telefono');
    const btn = document.getElementById('phoneBtn');

    if (telefono.style.display === 'block') {
      telefono.style.display = 'none';
      btn.textContent = texts[currentLang].showPhoneBtn;
    } else {
      telefono.style.display = 'block';
      btn.textContent = texts[currentLang].hidePhoneBtn;
    }
  }

  function toggleDarkMode() {
    document.body.classList.toggle('dark');
    const isDark = document.body.classList.contains('dark');
    document.getElementById('darkBtn').textContent = isDark ? '☀️ Modo Claro' : '🌙 Modo Oscuro';
  }
</script>
</body>
