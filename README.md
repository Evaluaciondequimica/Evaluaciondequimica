<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Evaluacion de quimica de acidos nucleicos</title>
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 600px;
            margin: 50px auto;
            background: white;
            padding: 20px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }
        h1 {
            color: #333;
            font-size: 24px;
            margin-bottom: 20px;
        }
        .question {
            margin-bottom: 20px;
        }
        .question label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        .question input, .question textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 16px;
        }
        .submit-btn {
            background-color: #4285f4;
            color: white;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            border-radius: 4px;
            font-size: 16px;
        }
        .submit-btn:hover {
            background-color: #357ae8;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Encuesta</h1>
        <form id="surveyForm">
            <div class="question">
                <label for="q1">¿Que es el ADN?:</label>
                <input type="text" id="q1" name="q1">
            </div>
            <div class="question">
                <label for="q2">¿Para que sirve el ADN?:</label>
                <textarea id="q2" name="q2"></textarea>
            </div>
            <button type="submit" class="submit-btn">Enviar</button>
        </form>
    </div>
    <script>
        window.onbeforeunload = function() {
            return "¿Estás seguro de que quieres salir? Aún no has completado la encuesta.";
        };

        document.getElementById('surveyForm').onsubmit = function(event) {
            event.preventDefault();
            var q1 = document.getElementById('q1').value;
            var q2 = document.getElementById('q2').value;
            var emailBody = 'Pregunta 1: ' + q1 + '%0D%0APregunta 2: ' + q2;
            window.location.href = 'mailto:leonelbautistavillarrealpedraz@gmail.com?subject=Respuestas de la Encuesta&body=' + emailBody;
            window.onbeforeunload = null;
        };
    </script>
</body>
</html>
