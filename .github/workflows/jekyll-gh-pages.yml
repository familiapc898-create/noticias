<!DOCTYPE html>
<html lang="es" class="scroll-smooth">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Radar Verificado — Noticias Fidedignas y Análisis</title>
  <meta name="description" content="Directorio curado de agencias de noticias, noticieros y medios especializados en política, economía y medio ambiente." />
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'system-ui', '-apple-system', 'sans-serif'],
            serif: ['Merriweather', 'Georgia', 'serif'],
          }
        }
      }
    }
  </script>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Merriweather:ital,wght@0,700;1,400&display=swap" rel="stylesheet">
  <style>
    .glass-panel {
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
    }
  </style>
</head>
<body class="bg-slate-50 text-slate-900 dark:bg-slate-950 dark:text-slate-100 transition-colors duration-200 min-h-screen flex flex-col">

  <!-- Barra de Administración (Solo visible en Modo Desarrollador) -->
  <div id="admin-toolbar" class="hidden sticky top-0 z-50 bg-emerald-950 text-emerald-50 border-b border-emerald-700 px-4 py-2.5 shadow-lg">
    <div class="max-w-7xl mx-auto flex flex-wrap items-center justify-between gap-3">
      <div class="flex items-center gap-2 text-sm font-medium">
        <span class="inline-flex h-2.5 w-2.5 rounded-full bg-emerald-400 animate-pulse"></span>
        <span>Modo Desarrollador Activo</span>
      </div>
      <div class="flex flex-wrap items-center gap-2">
        <button onclick="openMediaModal()" class="px-3 py-1.5 text-xs font-semibold bg-emerald-700 hover:bg-emerald-600 rounded-lg transition cursor-pointer">
          + Agregar Medio
        </button>
        <button onclick="openAffiliateModal()" class="px-3 py-1.5 text-xs font-semibold bg-amber-600 hover:bg-amber-500 text-white rounded-lg transition cursor-pointer">
          + Agregar Link Afiliado
        </button>
        <button onclick="openSecurityModal()" class="px-3 py-1.5 text-xs font-semibold bg-slate-800 hover:bg-slate-700 border border-slate-600 rounded-lg transition cursor-pointer">
          Cambiar Clave
        </button>
        <button onclick="exportStandaloneHTML()" class="px-3.5 py-1.5 text-xs font-bold bg-emerald-500 hover:bg-emerald-400 text-slate-950 rounded-lg shadow transition cursor-pointer">
          Descargar HTML Listo
        </button>
        <button onclick="logoutAdmin()" class="px-2.5 py-1.5 text-xs font-medium text-emerald-300 hover:text-white transition cursor-pointer">
          Salir
        </button>
      </div>
    </div>
  </div>

  <!-- Header Principal -->
  <header id="main-header" class="sticky top-0 z-40 bg-white/85 dark:bg-slate-900/85 glass-panel border-b border-slate-200 dark:border-slate-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
      <div class="flex items-center gap-3">
        <div class="w-9 h-9 rounded-xl bg-sky-600 flex items-center justify-center text-white font-serif font-bold text-lg shadow-sm">
          RV
        </div>
        <div>
          <span class="font-serif font-bold text-lg tracking-tight text-slate-900 dark:text-white block leading-none">
            Radar Verificado
          </span>
          <span class="text-[11px] text-slate-500 dark:text-slate-400 font-medium">
            Observatorio de Información Fidedigna
          </span>
        </div>
      </div>

      <nav class="hidden md:flex items-center gap-6 text-sm font-medium text-slate-600 dark:text-slate-300">
        <a href="#directorio" class="hover:text-sky-600 dark:hover:text-sky-400 transition">Directorio de Medios</a>
        <a href="#metodologia" class="hover:text-sky-600 dark:hover:text-sky-400 transition">Criterios de Rigor</a>
        <a href="#recursos" class="hover:text-sky-600 dark:hover:text-sky-400 transition">Recursos Recomendados</a>
      </nav>

      <div class="flex items-center gap-2">
        <button id="theme-toggle" aria-label="Cambiar tema" class="p-2 rounded-lg border border-slate-200 dark:border-slate-700 text-slate-600 dark:text-slate-300 hover:bg-slate-100 dark:hover:bg-slate-800 transition cursor-pointer">
          <svg id="sun-icon" class="w-5 h-5 hidden dark:block" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z"/>
          </svg>
          <svg id="moon-icon" class="w-5 h-5 block dark:hidden" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z"/>
          </svg>
        </button>
      </div>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="relative overflow-hidden bg-gradient-to-b from-sky-50/80 via-white to-slate-50 dark:from-slate-900 dark:via-slate-950 dark:to-slate-950 border-b border-slate-200/80 dark:border-slate-800/80 py-14 sm:py-20">
    <div class="max-w-4xl mx-auto px-4 sm:px-6 text-center">
      <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-sky-100 dark:bg-sky-950/80 text-sky-800 dark:text-sky-300 text-xs font-semibold mb-6 border border-sky-200 dark:border-sky-800">
        <span class="w-2 h-2 rounded-full bg-sky-500"></span>
        Curaduría Independiente • Sin Sensacionalismo
      </div>
      <h1 class="font-serif text-3xl sm:text-5xl font-bold text-slate-900 dark:text-white tracking-tight leading-tight mb-5">
        Encuentra las fuentes más confiables de <span class="text-sky-600 dark:text-sky-400">Política, Economía y Medio Ambiente</span>
      </h1>
      <p class="text-base sm:text-lg text-slate-600 dark:text-slate-300 max-w-2xl mx-auto leading-relaxed mb-8">
        Evita la desinformación y el ruido mediático. Reunimos en un solo lugar las agencias de noticias, canales internacionales y medios especializados con mayor rigor periodístico.
      </p>

      <!-- Buscador y Filtros -->
      <div class="max-w-2xl mx-auto space-y-4">
        <div class="relative">
          <input
            type="text"
            id="search-input"
            oninput="renderAll()"
            placeholder="Buscar medio, agencia, tema (ej. Reuters, inflación, clima, México)..."
            class="w-full pl-11 pr-4 py-3.5 rounded-xl bg-white dark:bg-slate-900 border border-slate-300 dark:border-slate-700 text-sm shadow-sm focus:outline-none focus:ring-2 focus:ring-sky-500"
          />
          <svg class="w-5 h-5 text-slate-400 absolute left-3.5 top-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"/>
          </svg>
        </div>

        <div id="category-filters" class="flex flex-wrap items-center justify-center gap-2">
          <button onclick="setCategory('all')" data-cat="all" class="cat-btn active px-4 py-1.5 rounded-full text-xs font-semibold bg-sky-600 text-white shadow-sm transition cursor-pointer">
            Todos los Medios
          </button>
          <button onclick="setCategory('politica')" data-cat="politica" class="cat-btn px-4 py-1.5 rounded-full text-xs font-semibold bg-white dark:bg-slate-800 text-slate-700 dark:text-slate-300 border border-slate-200 dark:border-slate-700 hover:border-sky-400 transition cursor-pointer">
            Política y Mundo
          </button>
          <button onclick="setCategory('economia')" data-cat="economia" class="cat-btn px-4 py-1.5 rounded-full text-xs font-semibold bg-white dark:bg-slate-800 text-slate-700 dark:text-slate-300 border border-slate-200 dark:border-slate-700 hover:border-sky-400 transition cursor-pointer">
            Economía y Finanzas
          </button>
          <button onclick="setCategory('ambiente')" data-cat="ambiente" class="cat-btn px-4 py-1.5 rounded-full text-xs font-semibold bg-white dark:bg-slate-800 text-slate-700 dark:text-slate-300 border border-slate-200 dark:border-slate-700 hover:border-sky-400 transition cursor-pointer">
            Medio Ambiente y Ciencia
          </button>
        </div>
      </div>
    </div>
  </section>

  <!-- Main Content -->
  <main class="flex-1 max-w-7xl w-full mx-auto px-4 sm:px-6 lg:px-8 py-12 space-y-16">

    <!-- Directorio de Medios -->
    <section id="directorio">
      <div class="flex flex-col sm:flex-row sm:items-end justify-between mb-6 gap-2">
        <div>
          <h2 class="font-serif text-2xl font-bold text-slate-900 dark:text-white">Canales y Fuentes Verificadas</h2>
          <p class="text-sm text-slate-500 dark:text-slate-400">Selecciona un medio para visitar su portal oficial o transmisión en vivo.</p>
        </div>
        <span id="results-count" class="text-xs font-medium text-slate-500 dark:text-slate-400"></span>
      </div>

      <div id="media-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <!-- Renderizado dinámico por JS -->
      </div>
    </section>

    <!-- Criterios de Verificación -->
    <section id="metodologia" class="bg-white dark:bg-slate-900 rounded-2xl border border-slate-200 dark:border-slate-800 p-6 sm:p-10 shadow-sm">
      <div class="max-w-3xl mb-8">
        <span class="text-xs font-bold uppercase tracking-wider text-sky-600 dark:text-sky-400">Metodología</span>
        <h2 class="font-serif text-2xl font-bold text-slate-900 dark:text-white mt-1">¿Cómo identificar información verdaderamente fidedigna?</h2>
        <p class="text-sm text-slate-600 dark:text-slate-300 mt-2">
          Basado en estándares internacionales como el <em>Digital News Report</em> del Instituto Reuters, recomendamos aplicar tres filtros antes de dar por cierta una noticia:
        </p>
      </div>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div class="p-5 rounded-xl bg-slate-50 dark:bg-slate-800/60 border border-slate-200/70 dark:border-slate-700/70">
          <div class="w-8 h-8 rounded-lg bg-sky-100 dark:bg-sky-900/50 text-sky-700 dark:text-sky-300 font-bold flex items-center justify-center mb-3">1</div>
          <h3 class="font-bold text-slate-900 dark:text-white text-base mb-1.5">Acude a la Agencia Primaria</h3>
          <p class="text-xs text-slate-600 dark:text-slate-300 leading-relaxed">
            Agencias como Reuters o AP reportan el hecho crudo antes de que los comentaristas agreguen opiniones o sesgos partidistas.
          </p>
        </div>
        <div class="p-5 rounded-xl bg-slate-50 dark:bg-slate-800/60 border border-slate-200/70 dark:border-slate-700/70">
          <div class="w-8 h-8 rounded-lg bg-emerald-100 dark:bg-emerald-900/50 text-emerald-700 dark:text-emerald-300 font-bold flex items-center justify-center mb-3">2</div>
          <h3 class="font-bold text-slate-900 dark:text-white text-base mb-1.5">Cruza Perspectivas</h3>
          <p class="text-xs text-slate-600 dark:text-slate-300 leading-relaxed">
            Contrasta medios públicos internacionales (DW, BBC) con prensa financiera especializada (El Financiero, Bloomberg) para entender el impacto real.
          </p>
        </div>
        <div class="p-5 rounded-xl bg-slate-50 dark:bg-slate-800/60 border border-slate-200/70 dark:border-slate-700/70">
          <div class="w-8 h-8 rounded-lg bg-amber-100 dark:bg-amber-900/50 text-amber-700 dark:text-amber-300 font-bold flex items-center justify-center mb-3">3</div>
          <h3 class="font-bold text-slate-900 dark:text-white text-base mb-1.5">Exige Datos y Evidencia</h3>
          <p class="text-xs text-slate-600 dark:text-slate-300 leading-relaxed">
            En temas ambientales y económicos, prioriza medios que citen estudios científicos revisados por pares o cifras oficiales de bancos centrales.
          </p>
        </div>
      </div>
    </section>

    <!-- Sección de Recursos y Links de Afiliado -->
    <section id="recursos" class="space-y-6">
      <div class="flex flex-col sm:flex-row sm:items-end justify-between gap-2 border-b border-slate-200 dark:border-slate-800 pb-4">
        <div>
          <span class="text-xs font-bold uppercase tracking-wider text-amber-600 dark:text-amber-400">Selección del Editor</span>
          <h2 class="font-serif text-2xl font-bold text-slate-900 dark:text-white mt-0.5">Recursos, Libros y Herramientas Recomendadas</h2>
        </div>
        <p class="text-[11px] text-slate-500 dark:text-slate-400">
          * Algunos enlaces pueden generar una comisión de afiliado sin costo extra para ti.
        </p>
      </div>

      <div id="affiliate-grid" class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <!-- Renderizado dinámico por JS -->
      </div>
    </section>

  </main>

  <!-- Footer -->
  <footer class="bg-white dark:bg-slate-900 border-t border-slate-200 dark:border-slate-800 mt-16">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8 flex flex-col sm:flex-row items-center justify-between gap-4 text-xs text-slate-500 dark:text-slate-400">
      <div>
        <span class="font-semibold text-slate-700 dark:text-slate-200">Radar Verificado</span> — Portal de curaduría informativa.
      </div>
      <div class="flex items-center gap-4">
        <span>Actualizado: 2026</span>
        <button onclick="triggerAdminLogin()" title="Acceso Desarrollador" class="p-1.5 rounded-md text-slate-400 hover:text-slate-700 dark:hover:text-slate-200 hover:bg-slate-100 dark:hover:bg-slate-800 transition cursor-pointer">
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"/>
          </svg>
        </button>
      </div>
    </div>
  </footer>

  <!-- Notificación Toast -->
  <div id="toast" class="fixed bottom-5 right-5 z-50 transform translate-y-20 opacity-0 transition-all duration-300 pointer-events-none">
    <div class="bg-slate-900 dark:bg-slate-800 text-white px-4 py-3 rounded-xl shadow-lg border border-slate-700 flex items-center gap-2.5 text-xs font-medium">
      <span id="toast-dot" class="w-2 h-2 rounded-full bg-emerald-400"></span>
      <span id="toast-message">Mensaje del sistema</span>
    </div>
  </div>

  <!-- Modal Login Desarrollador -->
  <div id="login-modal" class="hidden fixed inset-0 z-50 bg-slate-950/70 flex items-center justify-center p-4">
    <div class="bg-white dark:bg-slate-900 border border-slate-200 dark:border-slate-700 rounded-2xl max-w-sm w-full p-6 shadow-2xl">
      <h3 class="font-bold text-lg text-slate-900 dark:text-white mb-1">Acceso de Desarrollador</h3>
      <p class="text-xs text-slate-500 dark:text-slate-400 mb-4">Ingresa tu clave para editar medios o gestionar links de afiliado.</p>
      <form onsubmit="submitAdminLogin(event)" class="space-y-3">
        <input type="password" id="admin-pass-input" placeholder="Contraseña..." required class="w-full px-3.5 py-2.5 rounded-xl bg-slate-50 dark:bg-slate-800 border border-slate-300 dark:border-slate-700 text-sm focus:outline-none focus:ring-2 focus:ring-sky-500" />
        <div class="flex items-center justify-between text-[11px] text-slate-400">
          <span>Clave inicial: <code class="bg-slate-100 dark:bg-slate-800 px-1.5 py-0.5 rounded">admin2026</code></span>
          <button type="button" onclick="resetDefaultPassword()" class="text-sky-600 dark:text-sky-400 hover:underline cursor-pointer">Restablecer clave</button>
        </div>
        <p id="login-error" class="hidden text-xs text-rose-500 font-medium">Contraseña incorrecta.</p>
        <div class="flex justify-end gap-2 pt-2">
          <button type="button" onclick="closeModal('login-modal')" class="px-4 py-2 text-xs font-medium text-slate-600 dark:text-slate-300 hover:bg-slate-100 dark:hover:bg-slate-800 rounded-lg cursor-pointer">Cancelar</button>
          <button type="submit" class="px-4 py-2 text-xs font-bold bg-sky-600 hover:bg-sky-500 text-white rounded-lg cursor-pointer">Entrar</button>
        </div>
      </form>
    </div>
  </div>

  <!-- Modal Cambiar Contraseña -->
  <div id="security-modal" class="hidden fixed inset-0 z-50 bg-slate-950/70 flex items-center justify-center p-4">
    <div class="bg-white dark:bg-slate-900 border border-slate-200 dark:border-slate-700 rounded-2xl max-w-sm w-full p-6 shadow-2xl">
      <h3 class="font-bold text-lg text-slate-900 dark:text-white mb-1">Cambiar Clave de Desarrollador</h3>
      <p class="text-xs text-slate-500 dark:text-slate-400 mb-4">Define tu nueva contraseña secreta (mínimo 6 caracteres).</p>
      <form onsubmit="submitNewPassword(event)" class="space-y-3">
        <input type="password" id="new-pass-input" minlength="6" placeholder="Nueva contraseña..." required class="w-full px-3.5 py-2.5 rounded-xl bg-slate-50 dark:bg-slate-800 border border-slate-300 dark:border-slate-700 text-sm focus:outline-none focus:ring-2 focus:ring-emerald-500" />
        <div class="flex justify-end gap-2 pt-2">
          <button type="button" onclick="closeModal('security-modal')" class="px-4 py-2 text-xs font-medium text-slate-600 dark:text-slate-300 hover:bg-slate-100 dark:hover:bg-slate-800 rounded-lg cursor-pointer">Cancelar</button>
          <button type="submit" class="px-4 py-2 text-xs font-bold bg-emerald-600 hover:bg-emerald-500 text-white rounded-lg cursor-pointer">Actualizar Clave</button>
        </div>
      </form>
    </div>
  </div>

  <!-- Modal Confirmar Eliminación -->
  <div id="delete-modal" class="hidden fixed inset-0 z-50 bg-slate-950/70 flex items-center justify-center p-4">
    <div class="bg-white dark:bg-slate-900 border border-slate-200 dark:border-slate-700 rounded-2xl max-w-sm w-full p-6 shadow-2xl">
      <h3 class="font-bold text-lg text-slate-900 dark:text-white mb-1">Confirmar Eliminación</h3>
      <p id="delete-modal-text" class="text-xs text-slate-500 dark:text-slate-400 mb-5">¿Seguro que deseas eliminar este elemento?</p>
      <div class="flex justify-end gap-2">
        <button type="button" onclick="closeModal('delete-modal')" class="px-4 py-2 text-xs font-medium text-slate-600 dark:text-slate-300 hover:bg-slate-100 dark:hover:bg-slate-800 rounded-lg cursor-pointer">Cancelar</button>
        <button type="button" onclick="executeDelete()" class="px-4 py-2 text-xs font-bold bg-rose-600 hover:bg-rose-500 text-white rounded-lg cursor-pointer">Eliminar</button>
      </div>
    </div>
  </div>

  <!-- Modal Agregar/Editar Medio -->
  <div id="media-modal" class="hidden fixed inset-0 z-50 bg-slate-950/70 flex items-center justify-center p-4">
    <div class="bg-white dark:bg-slate-900 border border-slate-200 dark:border-slate-700 rounded-2xl max-w-md w-full p-6 shadow-2xl">
      <h3 id="media-modal-title" class="font-bold text-lg text-slate-900 dark:text-white mb-4">Agregar Nuevo Medio</h3>
      <form onsubmit="saveMediaItem(event)" class="space-y-3 text-sm">
        <input type="hidden" id="media-edit-id" />
        <div>
          <label class="block text-xs font-semibold mb-1">Nombre del Medio / Canal</label>
          <input type="text" id="media-name" required class="w-full px-3 py-2 rounded-lg bg-slate-50 dark:bg-slate-800 border border-slate-300 dark:border-slate-700" />
        </div>
        <div class="grid grid-cols-2 gap-3">
          <div>
            <label class="block text-xs font-semibold mb-1">Categoría</label>
            <select id="media-category" class="w-full px-3 py-2 rounded-lg bg-slate-50 dark:bg-slate-800 border border-slate-300 dark:border-slate-700">
              <option value="politica">Política y Mundo</option>
              <option value="economia">Economía y Finanzas</option>
              <option value="ambiente">Medio Ambiente</option>
            </select>
          </div>
          <div>
            <label class="block text-xs font-semibold mb-1">Formato</label>
            <input type="text" id="media-format" placeholder="TV / YouTube / Web" required class="w-full px-3 py-2 rounded-lg bg-slate-50 dark:bg-slate-800 border border-slate-300 dark:border-slate-700" />
          </div>
        </div>
        <div>
          <label class="block text-xs font-semibold mb-1">Etiqueta de Rigor / Tipo</label>
          <input type="text" id="media-badge" placeholder="Agencia Primaria / Especializado" required class="w-full px-3 py-2 rounded-lg bg-slate-50 dark:bg-slate-800 border border-slate-300 dark:border-slate-700" />
        </div>
        <div>
          <label class="block text-xs font-semibold mb-1">Descripción breve</label>
          <textarea id="media-desc" rows="2" required class="w-full px-3 py-2 rounded-lg bg-slate-50 dark:bg-slate-800 border border-slate-300 dark:border-slate-700"></textarea>
        </div>
        <div>
          <label class="block text-xs font-semibold mb-1">URL Oficial o Link de Afiliado</label>
          <input type="url" id="media-url" placeholder="https://..." required class="w-full px-3 py-2 rounded-lg bg-slate-50 dark:bg-slate-800 border border-slate-300 dark:border-slate-700" />
        </div>
        <div class="flex justify-end gap-2 pt-3">
          <button type="button" onclick="closeModal('media-modal')" class="px-4 py-2 text-xs font-medium text-slate-600 dark:text-slate-300 rounded-lg cursor-pointer">Cancelar</button>
          <button type="submit" class="px-4 py-2 text-xs font-bold bg-emerald-600 hover:bg-emerald-500 text-white rounded-lg cursor-pointer">Guardar Medio</button>
        </div>
      </form>
    </div>
  </div>

  <!-- Modal Agregar/Editar Producto Afiliado -->
  <div id="affiliate-modal" class="hidden fixed inset-0 z-50 bg-slate-950/70 flex items-center justify-center p-4">
    <div class="bg-white dark:bg-slate-900 border border-slate-200 dark:border-slate-700 rounded-2xl max-w-md w-full p-6 shadow-2xl">
      <h3 id="aff-modal-title" class="font-bold text-lg text-slate-900 dark:text-white mb-4">Agregar Recurso / Link Afiliado</h3>
      <form onsubmit="saveAffiliateItem(event)" class="space-y-3 text-sm">
        <input type="hidden" id="aff-edit-id" />
        <div>
          <label class="block text-xs font-semibold mb-1">Título del Recurso o Producto</label>
          <input type="text" id="aff-title" required class="w-full px-3 py-2 rounded-lg bg-slate-50 dark:bg-slate-800 border border-slate-300 dark:border-slate-700" />
        </div>
        <div>
          <label class="block text-xs font-semibold mb-1">Plataforma / Etiqueta (ej. Amazon, Hotmart, Suscripción)</label>
          <input type="text" id="aff-tag" required class="w-full px-3 py-2 rounded-lg bg-slate-50 dark:bg-slate-800 border border-slate-300 dark:border-slate-700" />
        </div>
        <div>
          <label class="block text-xs font-semibold mb-1">Descripción de valor</label>
          <textarea id="aff-desc" rows="2" required class="w-full px-3 py-2 rounded-lg bg-slate-50 dark:bg-slate-800 border border-slate-300 dark:border-slate-700"></textarea>
        </div>
        <div>
          <label class="block text-xs font-semibold mb-1">Tu Link de Afiliado (URL)</label>
          <input type="url" id="aff-url" placeholder="https://..." required class="w-full px-3 py-2 rounded-lg bg-slate-50 dark:bg-slate-800 border border-slate-300 dark:border-slate-700" />
        </div>
        <div>
          <label class="block text-xs font-semibold mb-1">Texto del Botón</label>
          <input type="text" id="aff-cta" value="Ver Recurso" required class="w-full px-3 py-2 rounded-lg bg-slate-50 dark:bg-slate-800 border border-slate-300 dark:border-slate-700" />
        </div>
        <div class="flex justify-end gap-2 pt-3">
          <button type="button" onclick="closeModal('affiliate-modal')" class="px-4 py-2 text-xs font-medium text-slate-600 dark:text-slate-300 rounded-lg cursor-pointer">Cancelar</button>
          <button type="submit" class="px-4 py-2 text-xs font-bold bg-amber-600 hover:bg-amber-500 text-white rounded-lg cursor-pointer">Guardar Link</button>
        </div>
      </form>
    </div>
  </div>

  <!-- Datos y Lógica de la Aplicación -->
  <script id="app-config-data" type="application/json">
  {
    "adminHash": "6051fc84a7a0d74c225fb18a496b09952da5642e60723ecae543298edd7d82d6",
    "mediaList": [
      {
        "id": "m1",
        "name": "Reuters en Español",
        "category": "politica",
        "format": "Portal Web / Agencia",
        "badge": "Agencia Primaria",
        "desc": "Fuente directa de hechos verificados sin editorializar. Es la agencia de referencia de la que se nutren los principales noticieros globales.",
        "url": "https://www.reuters.com/"
      },
      {
        "id": "m2",
        "name": "Associated Press (AP News)",
        "category": "politica",
        "format": "Web / App",
        "badge": "Agencia Primaria",
        "desc": "Cobertura mundial independiente y verificación de datos en tiempo real sobre política internacional, conflictos y elecciones.",
        "url": "https://apnews.com/hub/noticias"
      },
      {
        "id": "m3",
        "name": "DW Español (Deutsche Welle)",
        "category": "politica",
        "format": "YouTube / TV / Web",
        "badge": "Servicio Público Internacional",
        "desc": "Noticieros equilibrados, reportajes geopolíticos y documentales profundos libres de intereses comerciales privados.",
        "url": "https://www.dw.com/es/"
      },
      {
        "id": "m4",
        "name": "BBC News Mundo",
        "category": "politica",
        "format": "Web / YouTube",
        "badge": "Rigor Editorial",
        "desc": "Análisis explicativo de acontecimientos mundiales, ciencia y política con altos estándares de verificación periodística.",
        "url": "https://www.bbc.com/mundo"
      },
      {
        "id": "m5",
        "name": "El Financiero Bloomberg",
        "category": "economia",
        "format": "TV / YouTube / Prensa",
        "badge": "Líder Económico México",
        "desc": "Seguimiento riguroso de Banxico, tipo de cambio, finanzas públicas, mercados bursátiles y política nacional.",
        "url": "https://www.elfinanciero.com.mx/"
      },
      {
        "id": "m6",
        "name": "El Economista",
        "category": "economia",
        "format": "Prensa / Portal Web",
        "badge": "Análisis Financiero",
        "desc": "Datos macroeconómicos, indicadores de inversión, comercio exterior y análisis sectorial en México y Latinoamérica.",
        "url": "https://www.eleconomista.com.mx/"
      },
      {
        "id": "m7",
        "name": "Bloomberg Línea",
        "category": "economia",
        "format": "Web / Streaming",
        "badge": "Estándar Global",
        "desc": "Información financiera y empresarial de alto nivel sobre mercados globales, tasas de interés y corporativos.",
        "url": "https://www.bloomberglinea.com/"
      },
      {
        "id": "m8",
        "name": "Mongabay Latam",
        "category": "ambiente",
        "format": "Portal Investigativo",
        "badge": "Especializado Ambiental",
        "desc": "El medio independiente más respetado en América Latina sobre conservación, biodiversidad, deforestación y crisis climática.",
        "url": "https://es.mongabay.com/"
      },
      {
        "id": "m9",
        "name": "N+ (Foro TV) & Milenio",
        "category": "politica",
        "format": "TV Abierta / YouTube",
        "badge": "Cobertura Nacional en Vivo",
        "desc": "La mayor red de corresponsales en México para seguir acontecimientos nacionales y transmisiones de última hora.",
        "url": "https://www.nmas.com.mx/"
      }
    ],
    "affiliateList": [
      {
        "id": "a1",
        "title": "Factfulness (Factibilidad) — Hans Rosling",
        "tag": "Libro Recomendado • Amazon",
        "desc": "Guía esencial basada en datos para entender el estado real del mundo y detectar sesgos alarmistas en las noticias.",
        "url": "https://www.amazon.com.mx/",
        "cta": "Ver en Amazon"
      },
      {
        "id": "a2",
        "title": "Curso de Análisis Financiero e Inversiones",
        "tag": "Formación • Hotmart",
        "desc": "Aprende a interpretar indicadores macroeconómicos, tasas de interés y reportes financieros para proteger tu patrimonio.",
        "url": "https://hotmart.com/",
        "cta": "Explorar Curso"
      },
      {
        "id": "a3",
        "title": "Radio Portátil de Emergencia Solar / NOAA",
        "tag": "Equipamiento • Mercado Libre",
        "desc": "Mantente informado ante cortes eléctricos o emergencias climáticas con recepción AM/FM y alertas meteorológicas.",
        "url": "https://www.mercadolibre.com.mx/",
        "cta": "Ver Disponibilidad"
      }
    ]
  }
  </script>

  <script>
    // ==========================================
    // GESTIÓN DE ESTADO, DATOS Y MODO DESARROLLADOR
    // ==========================================
    const DEFAULT_ADMIN_HASH = '6051fc84a7a0d74c225fb18a496b09952da5642e60723ecae543298edd7d82d6';
    let appState = JSON.parse(document.getElementById('app-config-data').textContent);
    const localDraft = localStorage.getItem('rv_admin_draft');
    if (localDraft) {
      try {
        const parsed = JSON.parse(localDraft);
        if (parsed && typeof parsed === 'object') {
          appState = parsed;
          // Reparar automáticamente hashes corruptos o antiguos de versiones previas
          if (
            !appState.adminHash ||
            appState.adminHash === 'e36885b2c4338156f89f8384d3b034374122792045c174717a236b2c2a1f4781' ||
            appState.adminHash === '240be518fabd2724ddb6f04eeb1da5967448d7e831c08c8fa822809f74c720a9'
          ) {
            appState.adminHash = DEFAULT_ADMIN_HASH;
            localStorage.setItem('rv_admin_draft', JSON.stringify(appState));
          }
        }
      } catch (e) {}
    }

    let currentCategory = 'all';
    let isAdmin = false;
    let pendingDelete = null;

    // Implementación SHA-256 en JavaScript puro (funciona en file://, http://, https:// e iframes)
    function sha256(ascii) {
      function rightRotate(value, amount) {
        return (value >>> amount) | (value << (32 - amount));
      }
      const mathPow = Math.pow;
      const maxWord = mathPow(2, 32);
      let result = '';
      const words = [];
      const asciiBitLength = ascii.length * 8;
      const hash = [];
      const k = [];
      let primeCounter = 0;

      const isComposite = {};
      for (let candidate = 2; primeCounter < 64; candidate++) {
        if (!isComposite[candidate]) {
          for (let i = 0; i < 313; i += candidate) {
            isComposite[i] = candidate;
          }
          hash[primeCounter] = (mathPow(candidate, 0.5) * maxWord) | 0;
          k[primeCounter++] = (mathPow(candidate, 1 / 3) * maxWord) | 0;
        }
      }

      ascii += '\x80';
      while ((ascii.length % 64) - 56) ascii += '\x00';
      for (let i = 0; i < ascii.length; i++) {
        const j = ascii.charCodeAt(i);
        words[i >> 2] |= j << (((3 - i) % 4) * 8);
      }
      words[words.length] = (asciiBitLength / maxWord) | 0;
      words[words.length] = asciiBitLength;

      for (let j = 0; j < words.length; ) {
        const w = words.slice(j, (j += 16));
        const oldHash = hash.slice(0);

        for (let i = 0; i < 64; i++) {
          const w15 = w[i - 15];
          const w2 = w[i - 2];
          const a = hash[0];
          const e = hash[4];
          const temp1 =
            hash[7] +
            (rightRotate(e, 6) ^ rightRotate(e, 11) ^ rightRotate(e, 25)) +
            ((e & hash[5]) ^ (~e & hash[6])) +
            k[i] +
            (w[i] =
              i < 16
                ? w[i]
                : (w[i - 16] +
                    (rightRotate(w15, 7) ^ rightRotate(w15, 18) ^ (w15 >>> 3)) +
                    w[i - 7] +
                    (rightRotate(w2, 17) ^ rightRotate(w2, 19) ^ (w2 >>> 10))) |
                  0);
          const temp2 =
            (rightRotate(a, 2) ^ rightRotate(a, 13) ^ rightRotate(a, 22)) +
            ((a & hash[1]) ^ (a & hash[2]) ^ (hash[1] & hash[2]));

          hash.unshift((temp1 + temp2) | 0);
          hash[4] = (hash[4] + temp1) | 0;
          hash.pop();
        }

        for (let i = 0; i < 8; i++) {
          hash[i] = (hash[i] + oldHash[i]) | 0;
        }
      }

      for (let i = 0; i < 8; i++) {
        for (let j = 3; j + 1; j--) {
          const b = (hash[i] >> (j * 8)) & 255;
          result += (b < 16 ? '0' : '') + b.toString(16);
        }
      }
      return result;
    }

    function utf8Encode(str) {
      return unescape(encodeURIComponent(str));
    }

    function computePasswordHash(password) {
      return sha256(utf8Encode(password.trim()));
    }

    function resetDefaultPassword() {
      appState.adminHash = DEFAULT_ADMIN_HASH;
      saveDraft();
      document.getElementById('login-error').classList.add('hidden');
      document.getElementById('admin-pass-input').value = 'admin2026';
      showToast('Clave restablecida a admin2026.');
    }

    function triggerAdminLogin() {
      if (isAdmin) return;
      document.getElementById('login-error').classList.add('hidden');
      document.getElementById('admin-pass-input').value = '';
      document.getElementById('login-modal').classList.remove('hidden');
      setTimeout(() => document.getElementById('admin-pass-input').focus(), 50);
    }

    function submitAdminLogin(e) {
      e.preventDefault();
      const input = document.getElementById('admin-pass-input').value.trim();
      const hash = computePasswordHash(input);
      if (hash === appState.adminHash) {
        isAdmin = true;
        closeModal('login-modal');
        document.getElementById('admin-toolbar').classList.remove('hidden');
        document.getElementById('main-header').classList.remove('top-0');
        document.getElementById('main-header').classList.add('top-[44px]');
        renderAll();
        showToast('Modo Desarrollador activado.');
      } else {
        document.getElementById('login-error').classList.remove('hidden');
      }
    }

    function logoutAdmin() {
      isAdmin = false;
      document.getElementById('admin-toolbar').classList.add('hidden');
      document.getElementById('main-header').classList.add('top-0');
      document.getElementById('main-header').classList.remove('top-[44px]');
      renderAll();
      showToast('Sesión de desarrollador cerrada.');
    }

    function openSecurityModal() {
      document.getElementById('new-pass-input').value = '';
      document.getElementById('security-modal').classList.remove('hidden');
      setTimeout(() => document.getElementById('new-pass-input').focus(), 50);
    }

    function submitNewPassword(e) {
      e.preventDefault();
      const newPass = document.getElementById('new-pass-input').value.trim();
      if (newPass.length < 6) {
        showToast('La clave debe tener al menos 6 caracteres.', true);
        return;
      }
      appState.adminHash = computePasswordHash(newPass);
      saveDraft();
      closeModal('security-modal');
      showToast('Clave actualizada. Recuerda descargar el HTML listo.');
    }

    function saveDraft() {
      localStorage.setItem('rv_admin_draft', JSON.stringify(appState));
      renderAll();
    }

    function closeModal(id) {
      document.getElementById(id).classList.add('hidden');
    }

    let toastTimer;
    function showToast(msg, isError = false) {
      const toast = document.getElementById('toast');
      document.getElementById('toast-message').textContent = msg;
      document.getElementById('toast-dot').className = isError ? 'w-2 h-2 rounded-full bg-rose-400' : 'w-2 h-2 rounded-full bg-emerald-400';
      toast.classList.remove('translate-y-20', 'opacity-0');
      clearTimeout(toastTimer);
      toastTimer = setTimeout(() => {
        toast.classList.add('translate-y-20', 'opacity-0');
      }, 3500);
    }

    // Atajo de teclado Ctrl + Shift + E para abrir login
    document.addEventListener('keydown', (e) => {
      if (e.ctrlKey && e.shiftKey && e.key.toLowerCase() === 'e') {
        e.preventDefault();
        triggerAdminLogin();
      }
    });

    // ==========================================
    // CRUD MEDIOS Y LINKS DE AFILIADO
    // ==========================================
    function openMediaModal(id = null) {
      document.getElementById('media-modal').classList.remove('hidden');
      if (id) {
        const item = appState.mediaList.find(m => m.id === id);
        document.getElementById('media-modal-title').textContent = 'Editar Medio';
        document.getElementById('media-edit-id').value = item.id;
        document.getElementById('media-name').value = item.name;
        document.getElementById('media-category').value = item.category;
        document.getElementById('media-format').value = item.format;
        document.getElementById('media-badge').value = item.badge;
        document.getElementById('media-desc').value = item.desc;
        document.getElementById('media-url').value = item.url;
      } else {
        document.getElementById('media-modal-title').textContent = 'Agregar Nuevo Medio';
        document.getElementById('media-edit-id').value = '';
        document.getElementById('media-name').value = '';
        document.getElementById('media-category').value = 'politica';
        document.getElementById('media-format').value = '';
        document.getElementById('media-badge').value = '';
        document.getElementById('media-desc').value = '';
        document.getElementById('media-url').value = '';
      }
    }

    function saveMediaItem(e) {
      e.preventDefault();
      const id = document.getElementById('media-edit-id').value;
      const obj = {
        id: id || 'm_' + Date.now(),
        name: document.getElementById('media-name').value.trim(),
        category: document.getElementById('media-category').value,
        format: document.getElementById('media-format').value.trim(),
        badge: document.getElementById('media-badge').value.trim(),
        desc: document.getElementById('media-desc').value.trim(),
        url: document.getElementById('media-url').value.trim()
      };
      if (id) {
        const idx = appState.mediaList.findIndex(m => m.id === id);
        if (idx > -1) appState.mediaList[idx] = obj;
      } else {
        appState.mediaList.unshift(obj);
      }
      saveDraft();
      closeModal('media-modal');
      showToast('Medio guardado correctamente.');
    }

    function confirmDelete(type, id) {
      pendingDelete = { type, id };
      document.getElementById('delete-modal-text').textContent =
        type === 'media'
          ? '¿Seguro que deseas eliminar este medio del directorio?'
          : '¿Seguro que deseas eliminar este recurso afiliado?';
      document.getElementById('delete-modal').classList.remove('hidden');
    }

    function executeDelete() {
      if (!pendingDelete) return;
      if (pendingDelete.type === 'media') {
        appState.mediaList = appState.mediaList.filter(m => m.id !== pendingDelete.id);
      } else {
        appState.affiliateList = appState.affiliateList.filter(a => a.id !== pendingDelete.id);
      }
      pendingDelete = null;
      saveDraft();
      closeModal('delete-modal');
      showToast('Elemento eliminado.');
    }

    function openAffiliateModal(id = null) {
      document.getElementById('affiliate-modal').classList.remove('hidden');
      if (id) {
        const item = appState.affiliateList.find(a => a.id === id);
        document.getElementById('aff-modal-title').textContent = 'Editar Link Afiliado';
        document.getElementById('aff-edit-id').value = item.id;
        document.getElementById('aff-title').value = item.title;
        document.getElementById('aff-tag').value = item.tag;
        document.getElementById('aff-desc').value = item.desc;
        document.getElementById('aff-url').value = item.url;
        document.getElementById('aff-cta').value = item.cta;
      } else {
        document.getElementById('aff-modal-title').textContent = 'Agregar Recurso / Link Afiliado';
        document.getElementById('aff-edit-id').value = '';
        document.getElementById('aff-title').value = '';
        document.getElementById('aff-tag').value = '';
        document.getElementById('aff-desc').value = '';
        document.getElementById('aff-url').value = '';
        document.getElementById('aff-cta').value = 'Ver Recurso';
      }
    }

    function saveAffiliateItem(e) {
      e.preventDefault();
      const id = document.getElementById('aff-edit-id').value;
      const obj = {
        id: id || 'a_' + Date.now(),
        title: document.getElementById('aff-title').value.trim(),
        tag: document.getElementById('aff-tag').value.trim(),
        desc: document.getElementById('aff-desc').value.trim(),
        url: document.getElementById('aff-url').value.trim(),
        cta: document.getElementById('aff-cta').value.trim()
      };
      if (id) {
        const idx = appState.affiliateList.findIndex(a => a.id === id);
        if (idx > -1) appState.affiliateList[idx] = obj;
      } else {
        appState.affiliateList.unshift(obj);
      }
      saveDraft();
      closeModal('affiliate-modal');
      showToast('Recurso afiliado guardado.');
    }

    // Exportar HTML autónomo con los datos y clave actualizados
    function exportStandaloneHTML() {
      const cloneDoc = document.documentElement.cloneNode(true);
      const toolbar = cloneDoc.querySelector('#admin-toolbar');
      if (toolbar) toolbar.classList.add('hidden');
      const header = cloneDoc.querySelector('#main-header');
      if (header) {
        header.classList.add('top-0');
        header.classList.remove('top-[44px]');
      }
      const dataScript = cloneDoc.querySelector('#app-config-data');
      if (dataScript) {
        dataScript.textContent = '\n  ' + JSON.stringify(appState, null, 2) + '\n  ';
      }
      const mediaGrid = cloneDoc.querySelector('#media-grid');
      if (mediaGrid) mediaGrid.innerHTML = '';
      const affGrid = cloneDoc.querySelector('#affiliate-grid');
      if (affGrid) affGrid.innerHTML = '';

      const finalHtml = '<!DOCTYPE html>\n' + cloneDoc.outerHTML;
      const blob = new Blob([finalHtml], { type: 'text/html;charset=utf-8' });
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url;
      a.download = 'index.html';
      document.body.appendChild(a);
      a.click();
      document.body.removeChild(a);
      URL.revokeObjectURL(url);
      showToast('Archivo index.html descargado.');
    }

    // ==========================================
    // RENDERIZADO DE UI Y FILTROS
    // ==========================================
    function setCategory(cat) {
      currentCategory = cat;
      document.querySelectorAll('.cat-btn').forEach(btn => {
        if (btn.dataset.cat === cat) {
          btn.className = 'cat-btn active px-4 py-1.5 rounded-full text-xs font-semibold bg-sky-600 text-white shadow-sm transition cursor-pointer';
        } else {
          btn.className = 'cat-btn px-4 py-1.5 rounded-full text-xs font-semibold bg-white dark:bg-slate-800 text-slate-700 dark:text-slate-300 border border-slate-200 dark:border-slate-700 hover:border-sky-400 transition cursor-pointer';
        }
      });
      renderAll();
    }

    const categoryMeta = {
      politica: { label: 'Política y Mundo', color: 'bg-sky-100 text-sky-800 dark:bg-sky-950 dark:text-sky-300' },
      economia: { label: 'Economía y Finanzas', color: 'bg-emerald-100 text-emerald-800 dark:bg-emerald-950 dark:text-emerald-300' },
      ambiente: { label: 'Medio Ambiente', color: 'bg-teal-100 text-teal-800 dark:bg-teal-950 dark:text-teal-300' }
    };

    function renderAll() {
      const query = document.getElementById('search-input').value.toLowerCase().trim();
      const filteredMedia = appState.mediaList.filter(item => {
        const matchesCat = currentCategory === 'all' || item.category === currentCategory;
        const matchesQuery = !query ||
          item.name.toLowerCase().includes(query) ||
          item.desc.toLowerCase().includes(query) ||
          item.format.toLowerCase().includes(query) ||
          item.badge.toLowerCase().includes(query);
        return matchesCat && matchesQuery;
      });

      document.getElementById('results-count').textContent = `Mostrando ${filteredMedia.length} fuentes verificadas`;

      const mediaGrid = document.getElementById('media-grid');
      mediaGrid.innerHTML = filteredMedia.map(item => {
        const meta = categoryMeta[item.category] || categoryMeta.politica;
        const adminControls = isAdmin ? `
          <div class="flex items-center gap-1.5 mt-3 pt-3 border-t border-slate-100 dark:border-slate-800">
            <button onclick="openMediaModal('${item.id}')" class="px-2.5 py-1 text-[11px] font-semibold bg-slate-100 dark:bg-slate-800 hover:bg-sky-100 dark:hover:bg-sky-900 rounded text-slate-700 dark:text-slate-200 cursor-pointer">Editar / Link</button>
            <button onclick="confirmDelete('media', '${item.id}')" class="px-2.5 py-1 text-[11px] font-semibold bg-rose-50 dark:bg-rose-950/50 hover:bg-rose-100 text-rose-600 rounded cursor-pointer">Eliminar</button>
          </div>
        ` : '';

        return `
          <article class="group bg-white dark:bg-slate-900 rounded-2xl border border-slate-200 dark:border-slate-800 p-6 shadow-sm hover:shadow-md hover:border-sky-300 dark:hover:border-sky-700 transition flex flex-col justify-between">
            <div>
              <div class="flex items-center justify-between gap-2 mb-3">
                <span class="px-2.5 py-0.5 rounded-full text-[11px] font-semibold ${meta.color}">
                  ${meta.label}
                </span>
                <span class="text-[11px] font-medium text-slate-400 dark:text-slate-500">
                  ${item.format}
                </span>
              </div>
              <h3 class="font-serif font-bold text-lg text-slate-900 dark:text-white group-hover:text-sky-600 dark:group-hover:text-sky-400 transition">
                ${item.name}
              </h3>
              <p class="text-[11px] font-semibold text-emerald-600 dark:text-emerald-400 mt-0.5 mb-3">
                ✓ ${item.badge}
              </p>
              <p class="text-xs text-slate-600 dark:text-slate-300 leading-relaxed">
                ${item.desc}
              </p>
            </div>
            <div class="mt-5">
              <a href="${item.url}" target="_blank" rel="noopener noreferrer" class="inline-flex items-center justify-center w-full gap-1.5 px-4 py-2.5 rounded-xl bg-slate-900 dark:bg-slate-800 hover:bg-sky-600 dark:hover:bg-sky-600 text-white text-xs font-semibold transition">
                <span>Visitar Canal Oficial</span>
                <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"/>
                </svg>
              </a>
              ${adminControls}
            </div>
          </article>
        `;
      }).join('');

      const affGrid = document.getElementById('affiliate-grid');
      affGrid.innerHTML = appState.affiliateList.map(item => {
        const adminControls = isAdmin ? `
          <div class="flex items-center gap-1.5 mt-3 pt-3 border-t border-amber-200/50 dark:border-slate-800">
            <button onclick="openAffiliateModal('${item.id}')" class="px-2.5 py-1 text-[11px] font-semibold bg-slate-100 dark:bg-slate-800 hover:bg-amber-100 rounded text-slate-700 dark:text-slate-200 cursor-pointer">Editar Link</button>
            <button onclick="confirmDelete('affiliate', '${item.id}')" class="px-2.5 py-1 text-[11px] font-semibold bg-rose-50 dark:bg-rose-950/50 text-rose-600 rounded cursor-pointer">Eliminar</button>
          </div>
        ` : '';

        return `
          <div class="bg-gradient-to-br from-amber-50/70 to-white dark:from-slate-900 dark:to-slate-900 rounded-2xl border border-amber-200/80 dark:border-slate-800 p-6 flex flex-col justify-between shadow-sm">
            <div>
              <span class="inline-block px-2.5 py-0.5 rounded-md bg-amber-100 dark:bg-amber-950 text-amber-800 dark:text-amber-300 text-[11px] font-semibold mb-3">
                ${item.tag}
              </span>
              <h3 class="font-bold text-base text-slate-900 dark:text-white mb-2">
                ${item.title}
              </h3>
              <p class="text-xs text-slate-600 dark:text-slate-300 leading-relaxed">
                ${item.desc}
              </p>
            </div>
            <div class="mt-5">
              <a href="${item.url}" target="_blank" rel="sponsored noopener noreferrer" class="inline-flex items-center justify-center w-full gap-1.5 px-4 py-2.5 rounded-xl bg-amber-600 hover:bg-amber-500 text-white text-xs font-bold transition shadow-sm">
                <span>${item.cta}</span>
                <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/>
                </svg>
              </a>
              ${adminControls}
            </div>
          </div>
        `;
      }).join('');
    }

    // Tema claro/oscuro
    document.getElementById('theme-toggle').addEventListener('click', () => {
      document.documentElement.classList.toggle('dark');
      localStorage.setItem('rv_theme', document.documentElement.classList.contains('dark') ? 'dark' : 'light');
    });
    if (localStorage.getItem('rv_theme') === 'dark') {
      document.documentElement.classList.add('dark');
    }

    // Inicializar
    renderAll();
  </script>
</body>
</html>
