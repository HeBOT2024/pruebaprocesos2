<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Verificación de Clave</title>
    <script>
        function verificarClave() {
            // Obtiene los parámetros de la URL
            const params = new URLSearchParams(window.location.search);
            const clave = params.get('clave');
            const claveCorrecta = "prueba1";
            const urlFormulario = "https://forms.gle/UCsywdyoBjZXTJoA7";

            if (clave === claveCorrecta) {
                window.location.href = urlFormulario;
            } else {
                document.getElementById("mensaje").innerText = "Clave incorrecta. Intenta de nuevo.";
            }
        }

        window.onload = verificarClave;
    </script>
</head>
<body>
    <h2>Verificación de Clave</h2>
    <p id="mensaje"></p>
</body>
</html>
