# Lautaton.github.io
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Semana del Estudiante</title>
    <style>
        /* Estilos generales del cuerpo */
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f0f8ff; /* Azul cielo claro */
            color: #333;
            margin: 0;
            padding: 20px;
            display: flex;
            justify-content: center;
        }

        /* Contenedor principal */
        .container {
            width: 100%;
            max-width: 800px;
            background-color: #ffffff; /* Fondo blanco */
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            padding: 20px 40px;
        }

        /* Título principal */
        h1 {
            text-align: center;
            color: #0056b3; /* Azul oscuro */
            font-size: 2.5em;
            margin-bottom: 20px;
        }

        /* Títulos de los días y encuestas */
        h2 {
            background-color: #007bff; /* Azul primario */
            color: #ffffff;
            padding: 10px 15px;
            border-radius: 5px;
            margin-top: 30px;
        }

        /* Estilo de los botones de los juegos */
        .game-toggle {
            background-color: #e9ecef; /* Gris claro */
            color: #495057;
            cursor: pointer;
            padding: 15px;
            width: 100%;
            border: none;
            text-align: left;
            outline: none;
            font-size: 1.1em;
            transition: background-color 0.3s ease;
            margin-top: 10px;
            border-radius: 5px;
        }

        /* Efecto al pasar el mouse sobre el botón */
        .game-toggle:hover {
            background-color: #ced4da; /* Gris más oscuro */
        }
        
        /* Contenido descriptivo del juego (oculto por defecto) */
        .game-content {
            padding: 0 18px;
            background-color: white;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease-out;
            border-left: 3px solid #007bff;
            margin-left: 10px;
        }
        
        .game-content p {
            margin: 15px 0;
            line-height: 1.6;
        }

        /* Estilo para el ícono de flecha (eliminado como pediste) */
        .game-toggle::after {
            content: ''; 
            font-size: 12px;
            color: #007bff;
            float: right;
            margin-left: 5px;
            transition: transform 0.3s;
        }

        .game-toggle.active::after {
            transform: rotate(90deg); 
        }

        /* Estilos para las encuestas */
        .poll-question {
            margin-top: 20px;
            background-color: #f8f9fa; /* Gris muy claro para el fondo de la pregunta */
            border: 1px solid #dee2e6;
            border-radius: 5px;
            padding: 15px;
        }

        .poll-question p {
            font-weight: bold;
            margin-bottom: 10px;
            color: #0056b3; /* Color del título de la pregunta */
        }

        .poll-options label {
            display: block;
            margin-bottom: 8px;
            cursor: pointer;
        }

        .poll-options input[type="radio"] {
            margin-right: 8px;
        }

        .submit-poll {
            background-color: #28a745; /* Verde para el botón de enviar */
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 15px;
            font-size: 1em;
            transition: background-color 0.3s ease;
        }

        .submit-poll:hover {
            background-color: #218838; /* Verde más oscuro al pasar el mouse */
        }

        .poll-result {
            margin-top: 15px;
            padding: 10px;
            border-radius: 5px;
            font-weight: bold;
            display: none; /* Oculto por defecto */
        }

        .poll-result.correct {
            background-color: #d4edda; /* Verde claro para respuesta correcta */
            color: #155724; /* Verde oscuro para el texto */
        }

        .poll-result.incorrect {
            background-color: #f8d7da; /* Rojo claro para respuesta incorrecta */
            color: #721c24; /* Rojo oscuro para el texto */
        }

    </style>
</head>
<body>

    <div class="container">
        <h1>Semana del Estudiante</h1>

        <section>
            <h2>LUNES</h2>
            
            <button class="game-toggle">Carrera de Sillas</button>
            <div class="game-content">
                <p>Se colocan sillas en fila. Los alumnos deben sentarse y pasar al siguiente lugar rápidamente sin caerse. Gana el más veloz en llegar al final.</p>
            </div>

            <button class="game-toggle">Adivina la Canción</button>
            <div class="game-content">
                <p>Se ponen fragmentos cortos de canciones conocidas. El primer grupo que diga el nombre gana un punto.</p>
            </div>

            <button class="game-toggle">Globo en el Aire</button>
            <div class="game-content">
                <p>Cada equipo recibe un globo y debe mantenerlo en el aire sin que toque el suelo. El último grupo que lo mantenga gana.</p>
            </div>
        </section>

        <section>
            <h2>MARTES</h2>

            <button class="game-toggle">Pañuelito</button>
            <div class="game-content">
                <p>Dos equipos en fila, se da un número a cada jugador. El profesor levanta un pañuelo; cuando nombra un número, esos dos corren a agarrarlo.</p>
            </div>

            <button class="game-toggle">Mímica Relámpago</button>
            <div class="game-content">
                <p>Cada alumno representa con gestos una palabra (película, animal, famoso). Su equipo tiene 30 segundos para adivinar.</p>
            </div>

            <button class="game-toggle">Torre de Vasos</button>
            <div class="game-content">
                <p>Con vasos descartables, cada grupo debe apilarlos lo más alto posible en 2 minutos. Gana la torre más alta que no se caiga.</p>
            </div>
        </section>

        <section>
            <h2>MIÉRCOLES</h2>

            <button class="game-toggle">Sillas Musicales</button>
            <div class="game-content">
                <p>Se ponen sillas en círculo (una menos que participantes). Cuando la música para, todos deben sentarse. Quien queda de pie queda afuera.</p>
            </div>
            
            <button class="game-toggle">Carrera con Cucharas y Pelotas</button>
            <div class="game-content">
                <p>Cada jugador debe llevar una pelotita en una cuchara hasta la meta sin que se caiga. El más rápido gana.</p>
            </div>

            <button class="game-toggle">Teléfono Descompuesto</button>
            <div class="game-content">
                <p>Un equipo forma una fila. El primero recibe una frase corta y la susurra al siguiente. El último dice en voz alta lo que entendió. Gana el grupo que se acerque más a la frase original.</p>
            </div>
        </section>

        <section>
            <h2>Encuestas Divertidas</h2>

            <div class="poll-question" id="poll1">
                <p>1. ¿Cuál de estos juegos del Lunes te parece el más emocionante?</p>
                <div class="poll-options">
                    <label><input type="radio" name="question1" value="a"> Carrera de Sillas</label>
                    <label><input type="radio" name="question1" value="b"> Adivina la Canción</label>
                    <label><input type="radio" name="question1" value="c"> Globo en el Aire</label>
                </div>
                <button class="submit-poll" onclick="checkAnswer('poll1', 'a')">Responder</button>
                <div class="poll-result" id="result1"></div>
            </div>

            <div class="poll-question" id="poll2">
                <p>2. En el juego "Pañuelito", ¿quién nombra el número para que los jugadores corran?</p>
                <div class="poll-options">
                    <label><input type="radio" name="question2" value="a"> Un jugador del equipo contrario</label>
                    <label><input type="radio" name="question2" value="b"> El profesor</label>
                    <label><input type="radio" name="question2" value="c"> El capitán del equipo</label>
                </div>
                <button class="submit-poll" onclick="checkAnswer('poll2', 'b')">Responder</button>
                <div class="poll-result" id="result2"></div>
            </div>

            <div class="poll-question" id="poll3">
                <p>3. ¿Cuánto tiempo tiene un equipo para adivinar la mímica en "Mímica Relámpago"?</p>
                <div class="poll-options">
                    <label><input type="radio" name="question3" value="a"> 1 minuto</label>
                    <label><input type="radio" name="question3" value="b"> 30 segundos</label>
                    <label><input type="radio" name="question3" value="c"> Ilimitado</label>
                </div>
                <button class="submit-poll" onclick="checkAnswer('poll3', 'b')">Responder</button>
                <div class="poll-result" id="result3"></div>
            </div>

            <div class="poll-question" id="poll4">
                <p>4. ¿Qué juego del Miércoles consiste en apilar vasos lo más alto posible?</p>
                <div class="poll-options">
                    <label><input type="radio" name="question4" value="a"> Sillas Musicales</label>
                    <label><input type="radio" name="question4" value="b"> Carrera con Cucharas y Pelotas</label>
                    <label><input type="radio" name="question4" value="c"> Torre de Vasos</label>
                </div>
                <button class="submit-poll" onclick="checkAnswer('poll4', 'c')">Responder</button>
                <div class="poll-result" id="result4"></div>
            </div>

            <div class="poll-question" id="poll5">
                <p>5. En "Teléfono Descompuesto", ¿quién susurra la frase al siguiente en la fila?</p>
                <div class="poll-options">
                    <label><input type="radio" name="question5" value="a"> El primero que recibe la frase</label>
                    <label><input type="radio" name="question5" value="b"> El último de la fila</label>
                    <label><input type="radio" name="question5" value="c"> El profesor</label>
                </div>
                <button class="submit-poll" onclick="checkAnswer('poll5', 'a')">Responder</button>
                <div class="poll-result" id="result5"></div>
            </div>

        </section>
    </div>

<script>
    // Script para los botones de despliegue de contenido de los juegos
    const toggles = document.querySelectorAll('.game-toggle');

    toggles.forEach(toggle => {
        toggle.addEventListener('click', () => {
            toggle.classList.toggle('active');
            const content = toggle.nextElementSibling;
            if (content.style.maxHeight) {
                content.style.maxHeight = null;
            } else {
                content.style.maxHeight = content.scrollHeight + "px";
            }
        });
    });

    // Script para la lógica de las encuestas
    function checkAnswer(pollId, correctAnswer) {
        const pollElement = document.getElementById(pollId);
        const selectedOption = pollElement.querySelector(`input[name="question${pollId.replace('poll', '')}"]:checked`);
        const resultElement = document.getElementById(`result${pollId.replace('poll', '')}`);

        if (selectedOption) {
            resultElement.style.display = 'block';
            resultElement.classList.remove('correct', 'incorrect'); // Limpiar clases anteriores

            if (selectedOption.value === correctAnswer) {
                resultElement.textContent = "¡Correcto! 😊";
                resultElement.classList.add('correct');
            } else {
                resultElement.textContent = "Incorrecto. Intenta de nuevo. 🤔";
                resultElement.classList.add('incorrect');
            }
        } else {
            resultElement.style.display = 'block';
            resultElement.classList.remove('correct', 'incorrect');
            resultElement.classList.add('incorrect');
            resultElement.textContent = "Por favor, selecciona una opción.";
        }
    }
</script>

</body>
</html>
