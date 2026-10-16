# Umbralmasajes-bienestar-salud
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Umbral Spa | Servicios de Alta Terapia a Domicilio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2c2c2c;
            --accent: #c5a059;
            --bg-light: #f9f9f7;
            --text-main: #333333;
        }
        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-light);
            color: var(--text-main);
            scroll-behavior: smooth;
        }
        h1, h2, h3, .serif {
            font-family: 'Playfair Display', serif;
        }
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 1s ease-out;
        }
        .reveal.visible {
            opacity: 1;
            transform: translateY(0);
        }
        .nav-link {
            position: relative;
            transition: color 0.3s;
        }
        .nav-link::after {
            content: '';
            position: absolute;
            width: 0;
            height: 1px;
            bottom: -2px;
            left: 0;
            background-color: var(--accent);
            transition: width 0.3s;
        }
        .nav-link:hover::after {
            width: 100%;
        }
        .btn-luxury {
            background-color: var(--primary);
            color: white;
            padding: 0.75rem 2rem;
            border: 1px solid var(--primary);
            transition: all 0.3s;
            letter-spacing: 0.1em;
        }
        .btn-luxury:hover {
            background-color: transparent;
            color: var(--primary);
        }
        .service-card {
            background: white;
            transition: transform 0.4s ease;
        }
        .service-card:hover {
            transform: translateY(-10px);
        }
        .ai-glow {
            box-shadow: 0 0 15px rgba(197, 160, 89, 0.2);
            border: 1px solid rgba(197, 160, 89, 0.4);
        }
        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background-color: #25d366;
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            z-index: 1000;
            transition: transform 0.3s ease, background-color 0.3s ease;
        }
        .whatsapp-float:hover {
            transform: scale(1.1);
            background-color: #128c7e;
        }
    </style>
</head>
<body>

    <!-- Navegación -->
    <nav class="fixed w-full z-50 bg-white/90 backdrop-blur-sm border-b border-stone-100">
        <div class="max-w-7xl mx-auto px-8 py-5 flex justify-between items-center">
            <div class="text-3xl serif font-bold tracking-tighter text-stone-900">Umbral<span class="text-[#c5a059]">.</span></div>
            <div class="hidden md:flex space-x-10 text-[10px] tracking-[0.2em] uppercase font-semibold">
                <a href="#inicio" class="nav-link">Inicio</a>
                <a href="#terapias" class="nav-link">Terapias</a>
                <a href="#paquete" class="nav-link">Paquete Premium</a>
                <a href="#ia-consultor" class="nav-link text-amber-700 font-bold italic">Consultor ✨</a>
                <a href="#contacto" class="btn-luxury">Agendar</a>
            </div>
        </div>
    </nav>

    <!-- Botón de WhatsApp Flotante Actualizado -->
    <a href="https://wa.me/50769611471?text=Hola,%20deseo%20solicitar%20un%20servicio%20de%20masaje%20a%20domicilio%20de%20Umbral%20Spa." 
       class="whatsapp-float" 
       target="_blank" 
       aria-label="Contactar por WhatsApp">
        <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" fill="currentColor" viewBox="0 0 16 16">
            <path d="M13.601 2.326A7.854 7.854 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.933 7.933 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93A7.898 7.898 0 0 0 13.6 2.326zM7.994 14.521a6.573 6.573 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.557 6.557 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592zm3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.099-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.729.729 0 0 0-.529.247c-.182.198-.691.677-.691 1.654 0 .977.71 1.916.81 2.049.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232z"/>
        </svg>
    </a>

    <!-- Hero Section -->
    <section id="inicio" class="relative h-[85vh] flex items-center justify-center overflow-hidden">
        <div class="absolute inset-0">
            <img src="https://images.unsplash.com/photo-1544161515-4ab6ce6db874?auto=format&fit=crop&q=80&w=2000" 
                 alt="[Masaje profesional en casa]" 
                 class="w-full h-full object-cover grayscale-[10%] brightness-50">
        </div>
        <div class="relative z-10 text-center text-white px-6">
            <h1 class="text-6xl md:text-7xl mb-4 leading-tight italic font-light">El Spa que viaja <br><span class="not-italic font-bold text-[#c5a059]">a su Hogar</span></h1>
            <p class="text-lg md:text-xl font-light tracking-[0.3em] max-w-2xl mx-auto opacity-90 uppercase mt-4">
                Servicios de Alta Terapia a Domicilio
            </p>
        </div>
    </section>

    <!-- Banner de Equipamiento Incluido -->
    <section class="bg-stone-900 py-10 border-b border-stone-800">
        <div class="max-w-7xl mx-auto px-8 flex flex-wrap justify-center gap-12 text-stone-400">
            <div class="flex items-center space-x-3">
                <span class="text-[#c5a059] font-bold">✓</span>
                <span class="text-[10px] tracking-widest uppercase font-semibold">Camilla Profesional</span>
            </div>
            <div class="flex items-center space-x-3">
                <span class="text-[#c5a059] font-bold">✓</span>
                <span class="text-[10px] tracking-widest uppercase font-semibold">Aceites Orgánicos</span>
            </div>
            <div class="flex items-center space-x-3">
                <span class="text-[#c5a059] font-bold">✓</span>
                <span class="text-[10px] tracking-widest uppercase font-semibold">Música & Aromaterapia</span>
            </div>
            <div class="flex items-center space-x-3">
                <span class="text-[#c5a059] font-bold">✓</span>
                <span class="text-[10px] tracking-widest uppercase font-semibold">Herramientas Incluidas</span>
            </div>
        </div>
    </section>

    <!-- Sección de Terapias -->
    <section id="terapias" class="py-24 px-8">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-20 reveal">
                <span class="text-[#c5a059] text-xs tracking-[0.4em] uppercase mb-4 block">Carta de Servicios a Domicilio</span>
                <h2 class="text-4xl md:text-5xl serif italic">Tipos de Masajes</h2>
                <p class="text-stone-400 text-sm mt-4 font-light">Todos los servicios incluyen equipamiento y traslado.</p>
                <div class="w-12 h-px bg-stone-300 mx-auto mt-6"></div>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Relajante -->
                <div class="service-card p-8 border border-stone-100 reveal">
                    <h3 class="text-2xl serif mb-4">Relajante</h3>
                    <p class="text-stone-500 text-sm font-light leading-relaxed mb-6 italic">Tu pausa obligatoria. Un festín de suavidad que disuelve el estrés y reconecta tu paz interior.</p>
                    <div class="space-y-3 border-t border-stone-50 pt-4">
                        <div class="flex justify-between text-[11px] tracking-widest uppercase">
                            <span>60 Minutos</span>
                            <span class="font-bold text-[#c5a059]">90.00 USD</span>
                        </div>
                        <div class="flex justify-between text-[11px] tracking-widest uppercase">
                            <span>1:30 Minutos</span>
                            <span class="font-bold text-[#c5a059]">140.00 USD</span>
                        </div>
                    </div>
                </div>

                <!-- Descontracturante -->
                <div class="service-card p-8 border border-stone-100 reveal">
                    <h3 class="text-2xl serif mb-4">Descontracturante</h3>
                    <p class="text-stone-500 text-sm font-light leading-relaxed mb-6 italic">El adiós al dolor. Técnica precisa para liberar nudos y devolverle la libertad a tus movimientos.</p>
                    <div class="space-y-3 border-t border-stone-50 pt-4">
                        <div class="flex justify-between text-[11px] tracking-widest uppercase">
                            <span>60 Minutos</span>
                            <span class="font-bold text-[#c5a059]">115.00 USD</span>
                        </div>
                        <div class="flex justify-between text-[11px] tracking-widest uppercase">
                            <span>1:30 Minutos</span>
                            <span class="font-bold text-[#c5a059]">140.00 USD</span>
                        </div>
                    </div>
                </div>

                <!-- Deportivo -->
                <div class="service-card p-8 border border-stone-100 reveal">
                    <h3 class="text-2xl serif mb-4">Deportivo</h3>
                    <p class="text-stone-500 text-sm font-light leading-relaxed mb-6 italic">El combustible de tus músculos. Optimiza tu rendimiento, previene lesiones y acelera tu recuperación al máximo.</p>
                    <div class="space-y-3 border-t border-stone-50 pt-4">
                        <div class="flex justify-between text-[11px] tracking-widest uppercase">
                            <span>60 Minutos</span>
                            <span class="font-bold text-[#c5a059]">115.00 USD</span>
                        </div>
                        <div class="flex justify-between text-[11px] tracking-widest uppercase">
                            <span>1:30 Minutos</span>
                            <span class="font-bold text-[#c5a059]">140.00 USD</span>
                        </div>
                    </div>
                </div>

                <!-- Drenaje Linfático -->
                <div class="service-card p-8 border border-stone-100 reveal">
                    <h3 class="text-2xl serif mb-4">Drenaje Linfático</h3>
                    <p class="text-stone-500 text-sm font-light leading-relaxed mb-6 italic">El plan detox definitivo. Estimula tu sistema, elimina toxinas y reduce la hinchazón con suavidad rítmica.</p>
                    <div class="space-y-3 border-t border-stone-50 pt-4">
                        <div class="flex justify-between text-[11px] tracking-widest uppercase">
                            <span>60 Minutos</span>
                            <span class="font-bold text-[#c5a059]">90.00 USD</span>
                        </div>
                        <div class="flex justify-between text-[11px] tracking-widest uppercase">
                            <span>1:30 Minutos</span>
                            <span class="font-bold text-[#c5a059]">140.00 USD</span>
                        </div>
                    </div>
                </div>

                <!-- Masaje Prenatal -->
                <div class="service-card p-8 border border-stone-100 reveal">
                    <h3 class="text-2xl serif mb-4">Masaje Prenatal</h3>
                    <p class="text-stone-500 text-sm font-light leading-relaxed mb-6 italic">Un abrazo para dos. Alivia la carga física del embarazo y crea un espacio de serenidad para ti y tu bebé.</p>
                    <div class="space-y-3 border-t border-stone-50 pt-4">
                        <div class="flex justify-between text-[11px] tracking-widest uppercase">
                            <span>60 Minutos</span>
                            <span class="font-bold text-[#c5a059]">90.00 USD</span>
                        </div>
                        <div class="flex justify-between text-[11px] tracking-widest uppercase">
                            <span>1:30 Minutos</span>
                            <span class="font-bold text-[#c5a059]">140.00 USD</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Paquete Bienestar Total -->
    <section id="paquete" class="py-24 bg-stone-900 text-white overflow-hidden">
        <div class="max-w-6xl mx-auto px-8">
            <div class="grid md:grid-cols-2 gap-16 items-center">
                <div class="reveal">
                    <span class="text-[#c5a059] text-xs tracking-[0.5em] uppercase mb-4 block italic">Exclusividad Umbral</span>
                    <h2 class="text-5xl serif mb-8">Paquete Bienestar Total</h2>
                    <p class="text-stone-400 font-light leading-relaxed mb-8">
                        Una renovación integral de pies a cabeza diseñada para una desconexión absoluta sin salir de casa.
                    </p>
                    <ul class="space-y-4 mb-10">
                        <li class="flex items-start space-x-3">
                            <span class="text-[#c5a059] mt-1">✦</span>
                            <p class="text-sm"><strong class="text-white">Masaje Descontracturante:</strong> Liberación profunda de la tensión muscular.</p>
                        </li>
                        <li class="flex items-start space-x-3">
                            <span class="text-[#c5a059] mt-1">✦</span>
                            <p class="text-sm"><strong class="text-white">Facial Hidratante:</strong> Suaviza líneas de expresión y relaja los músculos del rostro.</p>
                        </li>
                        <li class="flex items-start space-x-3">
                            <span class="text-[#c5a059] mt-1">✦</span>
                            <p class="text-sm"><strong class="text-white">Masaje Craneal:</strong> Despeja la mente y elimina el agotamiento nervioso.</p>
                        </li>
                        <li class="flex items-start space-x-3">
                            <span class="text-[#c5a059] mt-1">✦</span>
                            <p class="text-sm"><strong class="text-white">Reflexología Podal:</strong> Equilibrio y vitalidad estimulando puntos clave.</p>
                        </li>
                    </ul>
                    
                    <div class="bg-stone-800/50 p-6 inline-block border border-stone-700 mb-8 w-full md:w-auto">
                        <p class="text-xs tracking-[0.2em] uppercase text-stone-400 mb-1">Precio Paquete</p>
                        <p class="text-4xl serif text-[#c5a059]">180.00 USD <span class="text-sm text-stone-500 italic font-light ml-2">/ 120 MIN</span></p>
                    </div>

                    <div class="mt-4">
                        <a href="https://wa.me/50769611471?text=Deseo%20reservar%20el%20Paquete%20Bienestar%20Total" target="_blank" class="inline-block bg-[#c5a059] text-white px-10 py-4 text-xs tracking-widest uppercase hover:bg-white hover:text-stone-900 transition-all font-bold">
                            Agendar Experiencia Completa
                        </a>
                    </div>
                </div>
                <div class="relative reveal">
                    <img src="https://images.unsplash.com/photo-1515377905703-c4788e51af15?auto=format&fit=crop&q=80&w=1000" 
                         alt="[Tratamiento facial y spa premium]" 
                         class="grayscale shadow-2xl">
                    <div class="absolute -bottom-6 -left-6 bg-stone-900 border border-stone-700 p-8 hidden md:block">
                        <p class="serif italic text-2xl text-[#c5a059]">Todo incluido a domicilio.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- IA Consultor -->
    <section id="ia-consultor" class="py-24 bg-stone-50 border-y border-stone-200">
        <div class="max-w-4xl mx-auto px-8">
            <div class="bg-white p-12 ai-glow reveal text-center">
                <span class="text-[#c5a059] text-[10px] tracking-[0.4em] uppercase mb-4 block font-bold">Personalización Inteligente</span>
                <h2 class="text-4xl serif italic mb-6">¿Qué necesita hoy su cuerpo? ✨</h2>
                <p class="text-stone-500 font-light mb-10 text-sm leading-relaxed">
                    Nuestra IA analizará sus necesidades para recomendarle el tratamiento a domicilio ideal.
                </p>
                <div class="space-y-6">
                    <textarea id="aiInput" placeholder="Ej: He tenido mucha tensión en la espalda baja por el trabajo..." 
                              class="w-full h-32 border border-stone-200 p-4 focus:outline-none focus:border-[#c5a059] transition-colors resize-none font-light text-sm italic bg-stone-50"></textarea>
                    <button onclick="consultarIA()" id="aiBtn" class="w-full bg-stone-900 text-white py-4 text-xs font-bold tracking-widest uppercase hover:bg-[#c5a059] transition-all">
                        Analizar mi Bienestar ✨
                    </button>
                    <div id="aiResponse" class="hidden mt-8 text-left p-6 bg-[#fcfaf7] border-l-2 border-[#c5a059]">
                        <p id="aiContent" class="text-stone-700 text-sm leading-loose font-light"></p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contacto / Reserva -->
    <section id="contacto" class="py-24 bg-white">
        <div class="max-w-3xl mx-auto px-8 text-center reveal">
            <h2 class="text-4xl serif mb-12 italic">Reserva Privada</h2>
            <form id="bookingForm" class="space-y-8 text-left bg-stone-50 p-10 shadow-sm border border-stone-100">
                <div class="grid md:grid-cols-2 gap-8">
                    <div class="flex flex-col">
                        <label class="text-[10px] uppercase tracking-widest mb-2 opacity-50 font-bold">Su Nombre</label>
                        <input type="text" id="formName" required class="border-b border-stone-200 py-2 focus:outline-none focus:border-stone-900 transition-colors bg-transparent">
                    </div>
                    <div class="flex flex-col">
                        <label class="text-[10px] uppercase tracking-widest mb-2 opacity-50 font-bold">WhatsApp de Contacto</label>
                        <input type="tel" required class="border-b border-stone-200 py-2 focus:outline-none focus:border-stone-900 transition-colors bg-transparent">
                    </div>
                </div>
                <div class="flex flex-col">
                    <label class="text-[10px] uppercase tracking-widest mb-2 opacity-50 font-bold">Dirección de Visita</label>
                    <input type="text" id="formAddr" placeholder="Calle, edificio, departamento..." required class="border-b border-stone-200 py-2 focus:outline-none focus:border-stone-900 transition-colors bg-transparent">
                </div>
                <div class="grid md:grid-cols-2 gap-8">
                    <div class="flex flex-col">
                        <label class="text-[10px] uppercase tracking-widest mb-2 opacity-50 font-bold">Terapia</label>
                        <select id="therapySelect" class="border-b border-stone-200 py-2 bg-transparent focus:outline-none focus:border-stone-900 transition-colors cursor-pointer">
                            <option value="Relajante">Relajante</option>
                            <option value="Descontracturante">Descontracturante</option>
                            <option value="Deportivo">Deportivo</option>
                            <option value="Drenaje Linfático">Drenaje Linfático</option>
                            <option value="Masaje Prenatal">Masaje Prenatal</option>
                            <option value="Paquete Bienestar Total">Paquete Bienestar Total (120 min)</option>
                        </select>
                    </div>
                    <div class="flex flex-col" id="durationContainer">
                        <label class="text-[10px] uppercase tracking-widest mb-2 opacity-50 font-bold">Duración</label>
                        <select id="durationSelect" class="border-b border-stone-200 py-2 bg-transparent focus:outline-none focus:border-stone-900 transition-colors cursor-pointer">
                            <option value="60 min">60 Minutos</option>
                            <option value="1:30 min">1:30 Minutos</option>
                        </select>
                    </div>
                </div>
                
                <div id="statusMessage" class="hidden p-4 bg-stone-100 text-[10px] tracking-widest text-center uppercase">
                    Redirigiendo a WhatsApp del coordinador...
                </div>
                
                <button type="submit" class="w-full btn-luxury uppercase text-xs font-bold py-5">
                    Solicitar Agenda Privada
                </button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-16 bg-white text-center border-t border-stone-100">
        <div class="text-3xl serif font-bold mb-6">Umbral<span class="text-[#c5a059]">.</span></div>
        <p class="text-stone-400 text-[10px] tracking-[0.4em] uppercase mb-12 italic">Llevando el bienestar a su puerta</p>
        <div class="mt-16 text-stone-300 text-[9px] uppercase tracking-widest">&copy; 2024 Umbral Spa • Masajes a Domicilio • Todos los equipos incluidos.</div>
    </footer>

    <script>
        const apiKey = ""; 

        async function consultarIA() {
            const input = document.getElementById('aiInput').value;
            const btn = document.getElementById('aiBtn');
            const responseDiv = document.getElementById('aiResponse');
            const content = document.getElementById('aiContent');

            if (!input.trim()) return;

            btn.disabled = true;
            btn.innerText = "Consultando... ✨";
            
            const systemPrompt = `Eres el consultor experto de Umbral Spa. 
            Debes recomendar una de nuestras terapias a domicilio (Relajante, Descontracturante, Deportivo, Drenaje Linfático, Prenatal o Paquete Bienestar Total) según lo que el usuario describa.
            Menciona siempre que el servicio incluye todo el equipamiento en su hogar. Responde en español con tono de lujo y empatía.`;

            try {
                const response = await fetch(`https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify({
                        contents: [{ parts: [{ text: input }] }],
                        systemInstruction: { parts: [{ text: systemPrompt }] }
                    })
                });
                const result = await response.json();
                const text = result.candidates?.[0]?.content?.parts?.[0]?.text;
                responseDiv.classList.remove('hidden');
                content.innerHTML = text.replace(/\n/g, '<br>');
            } catch (error) {
                content.innerText = "Error al conectar. Por favor contacte vía WhatsApp al +507 6961-1471.";
                responseDiv.classList.remove('hidden');
            } finally {
                btn.disabled = false;
                btn.innerText = "Analizar mi Bienestar ✨";
            }
        }

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) entry.target.classList.add('visible');
            });
        }, { threshold: 0.1 });
        document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

        const therapySelect = document.getElementById('therapySelect');
        const durationContainer = document.getElementById('durationContainer');
        therapySelect.addEventListener('change', function() {
            durationContainer.style.display = this.value === 'Paquete Bienestar Total' ? 'none' : 'flex';
        });

        document.getElementById('bookingForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const status = document.getElementById('statusMessage');
            
            const name = document.getElementById('formName').value;
            const addr = document.getElementById('formAddr').value;
            const therapy = document.getElementById('therapySelect').value;
            const duration = document.getElementById('durationSelect').value;
            
            status.classList.remove('hidden');
            
            // Construir mensaje de WhatsApp
            const msg = `Hola Umbral Spa, mi nombre es ${name}. Deseo solicitar un masaje a domicilio:
- Terapia: ${therapy}
- Duración: ${therapy === 'Paquete Bienestar Total' ? '120 min' : duration}
- Dirección: ${addr}`;
            
            const waUrl = `https://wa.me/50769611471?text=${encodeURIComponent(msg)}`;
            
            setTimeout(() => {
                window.open(waUrl, '_blank');
                status.innerText = "Redirigido a WhatsApp.";
                status.style.color = "#166534";
            }, 1000);
        });
    </script>
</body>
</html>
