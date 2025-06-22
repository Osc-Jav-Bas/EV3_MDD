# EV3_MDD
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Presentación ENSSEX</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .slide {
            display: none;
            min-height: 100vh;
            padding: 40px;
            text-align: center;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            margin-bottom: 20px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
        }

        .slide.active {
            display: block;
            animation: slideIn 0.5s ease-in-out;
        }

        @keyframes slideIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        h1 {
            font-size: 2.5em;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        h2 {
            font-size: 2em;
            margin-bottom: 30px;
            color: #ffd700;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
        }

        h3 {
            font-size: 1.5em;
            margin-bottom: 20px;
            color: #87ceeb;
        }

        .logo {
            width: 150px;
            height: 80px;
            background: white;
            margin: 0 auto 20px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #667eea;
            font-weight: bold;
            font-size: 1.2em;
        }

        .authors {
            font-size: 1.3em;
            margin: 20px 0;
        }

        .section-info {
            font-size: 1.1em;
            margin: 10px 0;
        }

        .content-box {
            background: rgba(255, 255, 255, 0.15);
            padding: 30px;
            border-radius: 15px;
            margin: 20px 0;
            text-align: left;
        }

        .variables-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }

        .variable-item {
            background: rgba(255, 255, 255, 0.2);
            padding: 15px;
            border-radius: 10px;
            text-align: left;
        }

        .stats-container {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin: 20px 0;
        }

        .stat-box {
            background: rgba(255, 255, 255, 0.2);
            padding: 20px;
            border-radius: 15px;
            margin: 10px;
            min-width: 150px;
        }

        .stat-number {
            font-size: 2em;
            font-weight: bold;
            color: #ffd700;
        }

        .recommendations {
            text-align: left;
            margin: 20px 0;
        }

        .recommendation-item {
            background: rgba(255, 255, 255, 0.15);
            padding: 15px;
            margin: 10px 0;
            border-radius: 10px;
            border-left: 4px solid #ffd700;
        }

        .navigation {
            position: fixed;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 10px;
            z-index: 1000;
        }

        .nav-btn {
            background: rgba(255, 255, 255, 0.3);
            border: none;
            padding: 15px 25px;
            border-radius: 25px;
            color: white;
            cursor: pointer;
            font-size: 1em;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .nav-btn:hover {
            background: rgba(255, 255, 255, 0.5);
            transform: translateY(-2px);
        }

        .nav-btn:disabled {
            opacity: 0.5;
            cursor: not-allowed;
        }

        .slide-counter {
            position: fixed;
            top: 20px;
            right: 20px;
            background: rgba(255, 255, 255, 0.2);
            padding: 10px 20px;
            border-radius: 20px;
            backdrop-filter: blur(10px);
        }

        .methodology-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }

        .model-card {
            background: rgba(255, 255, 255, 0.2);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
        }

        .model-title {
            color: #ffd700;
            font-size: 1.3em;
            margin-bottom: 10px;
        }

        ul {
            text-align: left;
            padding-left: 20px;
        }

        li {
            margin: 8px 0;
            line-height: 1.4;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="slide-counter">
            <span id="slideNumber">1</span> / <span id="totalSlides">8</span>
        </div>

        <!-- Slide 1: Portada -->
        <div class="slide active">
            <div class="logo">DUOC UC</div>
            <h1>Análisis de Factores Asociados al Uso de Métodos de Barrera</h1>
            <h2>Encuesta Nacional de Salud, Sexualidad y Género (ENSSEX)</h2>
            <div class="authors">
                <strong>Integrantes:</strong> Oscar Silva y Bastián González
            </div>
            <div class="section-info">
                <strong>Asignatura:</strong> Minería de Datos<br>
                <strong>Sección:</strong> BIY 7122-002D<br>
                <strong>Docente:</strong> José Antonio Ruiz Tagle Maturana<br>
                <strong>Fecha:</strong> 18 de Junio, 2025
            </div>
        </div>

        <!-- Slide 2: Introducción -->
        <div class="slide">
            <h2>Introducción</h2>
            <div class="content-box">
                <h3>Contexto del Estudio</h3>
                <p>El objetivo principal es <strong>identificar los factores que se relacionan con el uso de métodos de barrera</strong> en la última relación sexual, utilizando datos de la Encuesta Nacional de Salud Sexual y Reproductiva del Ministerio de Salud.</p>
                
                <h3>Importancia</h3>
                <p>Comprender estos factores es crucial para el desarrollo de políticas públicas de salud sexual y reproductiva, permitiendo diseñar intervenciones más efectivas y focalizadas.</p>
                
                <div class="stats-container">
                    <div class="stat-box">
                        <div class="stat-number">923</div>
                        <div>Variables totales</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-number">20,392</div>
                        <div>Observaciones</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-number">15</div>
                        <div>Variables seleccionadas</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Slide 3: Variables Seleccionadas -->
        <div class="slide">
            <h2>Variables Independientes Seleccionadas</h2>
            <div class="variables-grid">
                <div class="variable-item">
                    <h3>Demográficas</h3>
                    <ul>
                        <li><strong>Edad:</strong> Influye en comportamiento sexual</li>
                        <li><strong>Sexo:</strong> Diferencias culturales en responsabilidad</li>
                        <li><strong>Educación:</strong> Asociada con conductas preventivas</li>
                    </ul>
                </div>
                <div class="variable-item">
                    <h3>Relacionales</h3>
                    <ul>
                        <li><strong>Estado civil:</strong> Confianza vs. precaución</li>
                        <li><strong>Infidelidad:</strong> Exposición a riesgos</li>
                        <li><strong>Sexo con amor:</strong> Percepción de riesgo</li>
                    </ul>
                </div>
                <div class="variable-item">
                    <h3>Educativas</h3>
                    <ul>
                        <li><strong>Educación sexual escolar:</strong> Conocimientos preventivos</li>
                        <li><strong>Educación familiar:</strong> Valores y conductas</li>
                    </ul>
                </div>
                <div class="variable-item">
                    <h3>Conductuales</h3>
                    <ul>
                        <li><strong>Consumo de alcohol/drogas:</strong> Reducción percepción de riesgo</li>
                        <li><strong>Uso de apps:</strong> Relaciones casuales</li>
                        <li><strong>Juguetes sexuales:</strong> Nuevas dinámicas</li>
                    </ul>
                </div>
            </div>
        </div>

        <!-- Slide 4: Metodología -->
        <div class="slide">
            <h2>Metodología de Análisis</h2>
            <div class="content-box">
                <h3>Proceso de Limpieza y Preparación</h3>
                <ul>
                    <li>Transformación de variables categóricas a factores y binarias</li>
                    <li>Creación de variable objetivo: <strong>uso_preservativo</strong> (0=No, 1=Sí)</li>
                    <li>Manejo de valores faltantes y verificación de consistencia</li>
                    <li>Partición de datos: 70% entrenamiento, 30% prueba</li>
                </ul>
                
                <h3>Modelos Implementados</h3>
                <div class="methodology-grid">
                    <div class="model-card">
                        <div class="model-title">Regresión Logística</div>
                        <p>Modelo base para identificar asociaciones lineales</p>
                    </div>
                    <div class="model-card">
                        <div class="model-title">Árbol de Decisión</div>
                        <p>Captura relaciones no lineales e interacciones</p>
                    </div>
                    <div class="model-card">
                        <div class="model-title">Random Forest</div>
                        <p>Evalúa importancia de variables y mejora precisión</p>
                    </div>
                    <div class="model-card">
                        <div class="model-title">Naive Bayes</div>
                        <p>Clasificación probabilística basada en independencia</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Slide 5: Resultados Principales -->
        <div class="slide">
            <h2>Hallazgos Principales</h2>
            <div class="content-box">
                <h3>Factores Asociados Positivamente</h3>
                <ul>
                    <li><strong>Educación completa:</strong> Mayor probabilidad de uso de preservativos</li>
                    <li><strong>Educación sexual escolar:</strong> Impacto significativo en conductas preventivas</li>
                    <li><strong>Uso de aplicaciones:</strong> Asociado con mayor precaución en encuentros casuales</li>
                    <li><strong>Personas solteras:</strong> Mayor uso comparado con parejas estables</li>
                </ul>
                
                <h3>Factores de Riesgo</h3>
                <ul>
                    <li><strong>Consumo de alcohol/drogas:</strong> Reducción de percepción de riesgo</li>
                    <li><strong>Relaciones estables:</strong> Menor uso de métodos de barrera</li>
                    <li><strong>Percepción de reducción del placer:</strong> Barrera para el uso</li>
                    <li><strong>Falta de educación sexual:</strong> Menor conocimiento preventivo</li>
                </ul>
            </div>
        </div>

        <!-- Slide 6: Análisis por Género -->
        <div class="slide">
            <h2>Diferencias por Género y Situación Amorosa</h2>
            <div class="content-box">
                <h3>Patrones Identificados</h3>
                <ul>
                    <li><strong>Diferencias de género:</strong> Variaciones en la responsabilidad percibida del uso de métodos de barrera</li>
                    <li><strong>Situación amorosa:</strong> Las personas solteras muestran mayor uso de preservativos</li>
                    <li><strong>Educación sexual:</strong> Impacto diferencial según el contexto (escolar vs. familiar)</li>
                </ul>
                
                <div class="stats-container">
                    <div class="stat-box">
                        <div class="stat-number">↑</div>
                        <div>Uso en solteros</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-number">↓</div>
                        <div>Uso en parejas estables</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-number">+</div>
                        <div>Educación sexual</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Slide 7: Recomendaciones -->
        <div class="slide">
            <h2>Recomendaciones</h2>
            <div class="recommendations">
                <div class="recommendation-item">
                    <h3>Educación Sexual Integral</h3>
                    <p>Fortalecer programas desde edades tempranas, incorporando dimensiones como placer, consentimiento y desmitificación del uso del condón.</p>
                </div>
                
                <div class="recommendation-item">
                    <h3>Campañas Focalizadas</h3>
                    <p>Diseñar intervenciones específicas para grupos de riesgo (consumo de sustancias, encuentros casuales).</p>
                </div>
                
                <div class="recommendation-item">
                    <h3>Estrategias para Parejas Estables</h3>
                    <p>Desarrollar programas que refuercen la importancia de la protección continua, incluso en relaciones de confianza.</p>
                </div>
                
                <div class="recommendation-item">
                    <h3>Capacitación Familiar</h3>
                    <p>Entrenar a familias y educadores para proporcionar información sexual sin estigmas.</p>
                </div>
            </div>
        </div>

        <!-- Slide 8: Conclusiones -->
        <div class="slide">
            <h2>Conclusiones</h2>
            <div class="content-box">
                <h3>Impacto del Estudio</h3>
                <p>El análisis demuestra que múltiples factores demográficos, educativos y conductuales influyen significativamente en el uso de métodos de barrera.</p>
                
                <h3>Principales Contribuciones</h3>
                <ul>
                    <li>Identificación de variables predictoras clave</li>
                    <li>Comprensión de patrones de comportamiento sexual</li>
                    <li>Base evidencial para políticas públicas</li>
                    <li>Metodología replicable para futuras investigaciones</li>
                </ul>
                
                <h3>Proyecciones Futuras</h3>
                <p>Este estudio proporciona una base sólida para el desarrollo de intervenciones más efectivas en salud sexual y reproductiva, adaptadas a las realidades contemporáneas.</p>
                
                <div class="stats-container">
                    <div class="stat-box">
                        <div class="stat-number">AUC</div>
                        <div>Modelos predictivos validados</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-number">15</div>
                        <div>Variables analizadas</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-number">4</div>
                        <div>Modelos comparados</div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="navigation">
        <button class="nav-btn" id="prevBtn" onclick="changeSlide(-1)">← Anterior</button>
        <button class="nav-btn" id="nextBtn" onclick="changeSlide(1)">Siguiente →</button>
    </div>

    <script>
        let currentSlide = 0;
        const slides = document.querySelectorAll('.slide');
        const totalSlides = slides.length;

        document.getElementById('totalSlides').textContent = totalSlides;

        function showSlide(n) {
            slides[currentSlide].classList.remove('active');
            currentSlide = (n + totalSlides) % totalSlides;
            slides[currentSlide].classList.add('active');
            
            document.getElementById('slideNumber').textContent = currentSlide + 1;
            
            // Update navigation buttons
            document.getElementById('prevBtn').disabled = currentSlide === 0;
            document.getElementById('nextBtn').disabled = currentSlide === totalSlides - 1;
        }

        function changeSlide(direction) {
            if (direction === 1 && currentSlide < totalSlides - 1) {
                showSlide(currentSlide + 1);
            } else if (direction === -1 && currentSlide > 0) {
                showSlide(currentSlide - 1);
            }
        }

        // Keyboard navigation
        document.addEventListener('keydown', function(e) {
            if (e.key === 'ArrowLeft') changeSlide(-1);
            if (e.key === 'ArrowRight') changeSlide(1);
        });

        // Initialize
        showSlide(0);
    </script>
</body>
</html>
