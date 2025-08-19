<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>MUSI-K4U | Tu Revolución Musical</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" rel="stylesheet">
  <style>
    :root {
      --primary: #1a237e;
      --secondary: #8b0000;
      --accent: #00b8d4;
      --gold: #ffd700;
      --dark: #121212;
      --light: #f8f8f8;
    }
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #0f0f23, #1a1a2e);
      color: white;
      min-height: 100vh;
      margin: 0;
      overflow-x: hidden;
    }
    .btn {
      @apply px-6 py-3 bg-gradient-to-r from-blue-700 to-pink-600 text-white font-bold rounded-full shadow-lg hover:from-blue-800 hover:to-pink-700 transition transform hover:scale-105;
    }
    .btn-outline {
      @apply border border-cyan-500 text-cyan-400 hover:bg-cyan-500 hover:text-black;
    }
    .card {
      @apply bg-black/40 backdrop-blur-sm border border-cyan-500/30 rounded-2xl p-6 shadow-2xl;
    }
    .input, select, textarea {
      @apply w-full p-3 bg-gray-800 rounded-lg border border-gray-600 text-white placeholder-gray-400 focus:border-cyan-500 focus:outline-none;
    }
    .option-btn {
      @apply p-3 m-2 text-center rounded-lg border border-gray-600 cursor-pointer hover:bg-blue-900 hover:border-cyan-500 transition transform hover:scale-105;
    }
    .option-btn.selected {
      @apply bg-cyan-600 border-cyan-400 text-black font-bold;
    }
    .progress-container {
      @apply w-full bg-gray-800 rounded-full h-3 mt-4;
    }
    .progress-bar {
      @apply h-full rounded-full bg-gradient-to-r from-cyan-500 to-pink-500 flex items-center justify-center text-xs font-bold text-black;
    }
    .hidden { display: none; }
    header {
      background: rgba(10, 10, 20, 0.95);
      backdrop-filter: blur(10px);
      padding: 1.5rem;
      text-align: center;
      border-bottom: 1px solid var(--primary);
    }
    header h1 {
      font-size: 2.5rem;
      color: white;
      text-shadow: 0 0 15px rgba(0, 184, 212, 0.6);
      letter-spacing: 1.5px;
      font-weight: 700;
    }
    .logo-sub {
      font-size: 1.1rem;
      color: var(--accent);
      font-style: italic;
    }
    footer {
      text-align: center;
      padding: 2rem;
      margin-top: 4rem;
      color: #888;
      border-top: 1px solid rgba(255, 255, 255, 0.1);
      font-size: 0.9rem;
    }
    .nav-link {
      @apply hover:text-cyan-400 cursor-pointer;
    }
  </style>
</head>
<body class="bg-gradient-to-br from-gray-900 via-indigo-950 to-black text-white min-h-screen">

  <!-- Header -->
  <header>
    <h1>MUSI-K4U</h1>
    <div class="logo-sub">Tu Música. Tu Artista. Tu Éxito.</div>
  </header>

  <!-- Navigation -->
  <div class="max-w-6xl mx-auto px-6 py-4 flex justify-center gap-8 text-sm">
    <span class="nav-link" onclick="showPage('home')">Inicio</span>
    <span class="nav-link" onclick="showPage('pricing')">Precios</span>
    <span class="nav-link" onclick="showPage('help')">Ayuda</span>
    <span class="nav-link" onclick="showPage('feedback')">Enviar Feedback</span>
    <span class="nav-link" onclick="showPage('terms')">Términos</span>
    <span class="nav-link" onclick="showPage('privacy')">Privacidad</span>
  </div>

  <main class="max-w-6xl mx-auto p-6 pt-2 pb-20">

    <!-- Home -->
    <section id="home" class="page">
      <div class="text-center mb-10">
        <h2 class="text-4xl font-bold mb-4">Crea tu Música con IA</h2>
        <p class="text-lg text-gray-300">Genera canciones, artistas virtuales y videos en 4K. Todo en minutos.</p>
      </div>

      <div class="grid md:grid-cols-3 gap-8 mb-10">
        <div class="card text-center">
          <i class="fas fa-music text-5xl mb-4 text-cyan-400"></i>
          <h3 class="text-xl mb-2">Canción de 3-4 min</h3>
          <p>Con voces naturales, letras profesionales y estilo global.</p>
        </div>
        <div class="card text-center">
          <i class="fas fa-user-astronaut text-5xl mb-4 text-pink-400"></i>
          <h3 class="text-xl mb-2">Avatar Personalizado</h3>
          <p>Crea tu vocalista: ropa, rostro, accesorios, baile.</p>
        </div>
        <div class="card text-center">
          <i class="fas fa-film text-5xl mb-4 text-gold"></i>
          <h3 class="text-xl mb-2">Video de 3-4 min</h3>
          <p>Con escenarios reales o futuristas. Listo para YouTube y TikTok.</p>
        </div>
      </div>

      <div class="text-center">
        <button onclick="showPage('create')" class="btn">🎵 Empezar a Crear</button>
      </div>
    </section>

    <!-- Crear -->
    <section id="create" class="page hidden">
      <div class="card">
        <h2 class="text-3xl mb-6 text-center">🎨 Diseña tu Artista Virtual</h2>
        <div class="grid md:grid-cols-2 gap-6 mb-8">
          <div>
            <label>Género</label>
            <select id="gender" class="input">
              <option>Hombre</option>
              <option>Mujer</option>
              <option>No Binario</option>
            </select>
          </div>
          <div>
            <label>Color de Piel</label>
            <select id="skin" class="input">
              <option>Blanco</option>
              <option>Moreno</option>
              <option>Oscuro</option>
              <option>Albino</option>
            </select>
          </div>
          <div>
            <label>Color de Cabello</label>
            <select id="hair" class="input">
              <option>Negro</option>
              <option>Rubio</option>
              <option>Rojo</option>
              <option>Azul</option>
              <option>Plateado</option>
            </select>
          </div>
          <div>
            <label>Estilo de Ropa</label>
            <select id="outfit" class="input">
              <option>Elegante</option>
              <option>Casual</option>
              <option>Grunge</option>
              <option>Formal</option>
              <option>Futurista</option>
            </select>
          </div>
        </div>

        <h2 class="text-3xl mb-6 text-center">🌆 Elige tu Escenario</h2>
        <div class="grid md:grid-cols-3 gap-4 mb-8">
          <div class="option-btn selected" data-scene="studio">Estudio Profesional</div>
          <div class="option-btn" data-scene="park">Parque Natural</div>
          <div class="option-btn" data-scene="concert">Concierto en Vivo</div>
        </div>

        <div class="text-center mt-8">
          <button onclick="showPage('music')" class="btn">Siguiente →</button>
        </div>
      </div>
    </section>

    <!-- Música -->
    <section id="music" class="page hidden">
      <div class="card">
        <h2 class="text-3xl mb-6 text-center">🎶 Genera tu Canción</h2>
        <div class="mb-6">
          <label>Tema o Idea</label>
          <input type="text" id="theme" class="input" placeholder="Ej: amor, traición, fiesta...">
        </div>
        <div class="mb-6">
          <label>Género Musical</label>
          <input type="text" id="genre" class="input" placeholder="Ej: Corridos Tumbados, Rock 80's...">
        </div>
        <div class="mb-6">
          <label>Letra (Opcional)</label>
          <textarea id="lyrics" class="input h-32" placeholder="Escribe tu letra aquí..."></textarea>
        </div>
        <div class="text-center">
          <button onclick="startGeneration()" class="btn">🚀 Generar Canción y Video</button>
        </div>
      </div>
    </section>

    <!-- Generación -->
    <section id="generate" class="page hidden">
      <div class="card text-center">
        <h2 class="text-3xl mb-6">⏳ Generando tu Obra Maestra</h2>
        <p id="progressText">Iniciando sistema de creación...</p>
        
        <div class="progress-container">
          <div id="progressBar" class="progress-bar" style="width: 0%">0%</div>
        </div>
        
        <div class="mt-8 space-y-2 text-sm text-cyan-300">
          <p id="status1">• Creando avatar virtual...</p>
          <p id="status2" class="hidden">• Componiendo música con Reffusion AI...</p>
          <p id="status3" class="hidden">• Generando voz ultra realista...</p>
          <p id="status4" class="hidden">• Animando al artista en el escenario...</p>
          <p id="status5" class="hidden">• Renderizando video en 4K (3-4 min)...</p>
          <p id="status6" class="hidden">• Listo para descarga y distribución.</p>
        </div>
      </div>
    </section>

    <!-- Resultado -->
    <section id="result" class="page hidden">
      <div class="card text-center">
        <h2 class="text-3xl mb-4">🎉 ¡Listo, Artista!</h2>
        <p class="text-lg mb-6">Tu canción y video han sido creados con éxito.</p>

        <div class="my-8">
          <audio controls class="w-full max-w-2xl mx-auto rounded-lg">
            <source src="https://cdn.pixabay.com/audio/2022/03/16/audio_3f75836316.mp3" type="audio/mpeg">
          </audio>
        </div>

        <div class="my-6">
          <img src="https://images.unsplash.com/photo-1587486913847-ef518e868f7e" 
               alt="Video del concierto" 
               class="w-full max-w-2xl mx-auto rounded-lg">
        </div>

        <div class="mb-8">
          <h3 class="text-xl mb-4">📥 Descargar</h3>
          <div class="flex flex-wrap justify-center gap-4">
            <button class="btn bg-green-700 hover:bg-green-800">🎵 MP3</button>
            <button class="btn bg-blue-700 hover:bg-blue-800">🎬 MP4</button>
            <button class="btn bg-purple-700 hover:bg-purple-800">🎧 M4A</button>
            <button class="btn bg-gray-700 hover:bg-gray-800">🔊 WAV</button>
          </div>
        </div>

        <button onclick="showPage('pricing')" class="btn">📈 Publicar y Monetizar</button>
      </div>
    </section>

    <!-- Precios -->
    <section id="pricing" class="page hidden">
      <h2 class="text-3xl text-center mb-10">💎 Suscripciones</h2>
      <div class="grid md:grid-cols-3 gap-8">

        <!-- Gratis -->
        <div class="card text-center">
          <h3 class="text-2xl font-bold text-cyan-400">Gratis</h3>
          <div class="text-4xl my-4">$0<span class="text-sm">/mes</span></div>
          <ul class="space-y-2 mb-6">
            <li>✔️ Canción de 3-4 min</li>
            <li>✔️ Avatar básico</li>
            <li>✔️ Escenario limitado</li>
            <li>❌ Sin monetización</li>
            <li>❌ Sin distribución</li>
          </ul>
          <button class="btn btn-outline">Descargar App</button>
        </div>

        <!-- U'RE 1st STEP -->
        <div class="card text-center border-2 border-cyan-500 relative">
          <div class="absolute -top-4 left-1/2 transform -translate-x-1/2 bg-cyan-500 text-black px-4 py-1 rounded-full text-sm font-bold">Más Popular</div>
          <h3 class="text-2xl font-bold text-cyan-400">U'RE 1st STEP</h3>
          <div class="text-4xl my-4">$34.99<span class="text-sm">/mes</span></div>
          <ul class="space-y-2 mb-6">
            <li>✔️ Derechos de autor tuyos</li>
            <li>✔️ Distribución en Spotify, Apple, YouTube</li>
            <li>✔️ Soporte prioritario</li>
            <li>✔️ Estadísticas detalladas</li>
            <li class="font-bold text-green-400">💰 Ganancia: $15–$30/mes por suscripción</li>
          </ul>
          <button class="btn">Suscribirse</button>
        </div>

        <!-- GO 4 MORE -->
        <div class="card text-center">
          <h3 class="text-2xl font-bold text-pink-400">GO 4 MORE</h3>
          <div class="text-4xl my-4">$69.99<span class="text-sm">/mes</span></div>
          <ul class="space-y-2 mb-6">
            <li>✔️ Todo de U'RE 1st STEP</li>
            <li>✔️ Marketing y promoción</li>
            <li>✔️ Asesoría profesional</li>
            <li>✔️ Publicación automática</li>
            <li class="font-bold text-green-400">💰 Ganancia: $20–$40/mes por suscripción</li>
          </ul>
          <button class="btn">Escalar Ahora</button>
        </div>
      </div>
    </section>

    <!-- Páginas Legales -->
    <section id="terms" class="page hidden">
      <div class="card">
        <h2 class="text-2xl mb-4">📄 Términos de Servicio</h2>
        <p>Al usar MUSI-K4U, aceptas que:</p>
        <ul class="list-disc ml-5 mt-2 space-y-1">
          <li>No clonamos voces reales de artistas.</li>
          <li>Tú eres dueño de tu música con planes premium.</li>
          <li>No nos hacemos responsables por uso indebido.</li>
        </ul>
      </div>
    </section>

    <section id="privacy" class="page hidden">
      <div class="card">
        <h2 class="text-2xl mb-4">🔒 Política de Privacidad</h2>
        <p>No vendemos tus datos. Solo usamos tu correo para autenticación y notificaciones. Tus canciones son privadas a menos que las publiques.</p>
      </div>
    </section>

    <section id="help" class="page hidden">
      <div class="card">
        <h2 class="text-2xl mb-4">❓ Ayuda</h2>
        <p>¿Tienes dudas? Escríbenos a: <strong>soporte@musi-k4u.com</strong></p>
      </div>
    </section>

    <section id="feedback" class="page hidden">
      <div class="card">
        <h2 class="text-2xl mb-4">📬 Enviar Feedback</h2>
        <textarea class="input h-32 mb-4" placeholder="Tu opinión es importante..."></textarea>
        <button class="btn">Enviar</button>
      </div>
    </section>

  </main>

  <footer>
    <p>© 2025 MUSI-K4U – Todos los derechos reservados.</p>
    <p><em>Proyecto visionado y creado por Mike Estrada. Este código marca el inicio de una nueva era en la música con IA.</em></p>
  </footer>

  <script>
    // Navegación
    function showPage(id) {
      document.querySelectorAll('.page').forEach(p => p.classList.add('hidden'));
      document.getElementById(id).classList.remove('hidden');
    }

    // Selección de escenarios
    document.querySelectorAll('.option-btn').forEach(btn => {
      btn.addEventListener('click', function () {
        document.querySelectorAll('.option-btn').forEach(b => b.classList.remove('selected'));
        this.classList.add('selected');
      });
    });

    // Generación progresiva
    function startGeneration() {
      showPage('generate');
      let progress = 0;
      const progressBar = document.getElementById('progressBar');
      const progressText = document.getElementById('progressText');
      const statuses = ['status1', 'status2', 'status3', 'status4', 'status5', 'status6'];

      const interval = setInterval(() => {
        progress += 1;
        progressBar.style.width = progress + '%';
        progressBar.textContent = Math.round(progress) + '%';

        if (progress === 16) {
          progressText.textContent = 'Creando avatar virtual...';
        } else if (progress === 33) {
          document.getElementById('status1').classList.add('line-through');
          document.getElementById('status2').classList.remove('hidden');
          progressText.textContent = 'Componiendo música con Reffusion AI...';
        } else if (progress === 50) {
          document.getElementById('status2').classList.add('line-through');
          document.getElementById('status3').classList.remove('hidden');
          progressText.textContent = 'Generando voz ultra realista...';
        } else if (progress === 67) {
          document.getElementById('status3').classList.add('line-through');
          document.getElementById('status4').classList.remove('hidden');
          progressText.textContent = 'Animando al artista en el escenario...';
        } else if (progress === 85) {
          document.getElementById('status4').classList.add('line-through');
          document.getElementById('status5').classList.remove('hidden');
          progressText.textContent = 'Renderizando video en 4K...';
        } else if (progress >= 100) {
          clearInterval(interval);
          document.getElementById('status5').classList.add('line-through');
          document.getElementById('status6').classList.remove('hidden');
          progressText.textContent = '¡Listo! Tu obra maestra está completa.';
          setTimeout(() => showPage('result'), 1500);
        }
      }, 60);
    }
  </script>

  <!-- 
  🛠️ Código desarrollado con visión por Mike Estrada
  📅 2025
  🚀 Este es el inicio de MUSI-K4U: la revolución musical sin fronteras.
  💡 No clones este proyecto. Respeta al creador.
  -->
</body>
</html>
