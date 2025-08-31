<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Certificado de Permiso Operativo - Bomberos de Siguatepeque</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #f4f4f4;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        h1 {
            text-align: center;
            color: #b22222;
        }
        .subtitle {
            font-size: 18px;
            color: #333;
            text-align: center;
            margin-top: 5px;
        }
        label {
            display: block;
            margin-top: 10px;
            font-weight: bold;
        }
        input, select, textarea {
            width: 100%;
            padding: 8px;
            margin-top: 5px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        button {
            margin-top: 20px;
            padding: 10px 20px;
            background-color: #b22222;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #8b1a1a;
        }
        #qrcode {
            text-align: center;
            margin-top: 20px;
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Estación de Bomberos de Siguatepeque</h1>
        <div class="subtitle">Datos de Certificación OTPSCI</div>
        <form id="certificationForm">
            <label for="empresa">Nombre de la Empresa:</label>
            <input type="text" id="empresa" name="empresa" required>

            <label for="rubro">Rubro:</label>
            <input type="text" id="rubro" name="rubro" required>

            <label for="registro">Número Correlativo de Registro:</label>
            <input type="text" id="registro" name="registro" required>

            <label for="direccion">Dirección del Establecimiento:</label>
            <input type="text" id="direccion" name="direccion" required>

            <label for="fecha_emision">Fecha de Emisión:</label>
            <input type="text" id="fecha_emision" name="fecha_emision" readonly>

            <label for="fecha_vencimiento">Fecha de Vencimiento:</label>
            <input type="date" id="fecha_vencimiento" name="fecha_vencimiento" required>

            <label for="inspectores">Nombre del Inspector(es):</label>
            <input type="text" id="inspectores" name="inspectores" required>

            <button type="button" onclick="procesarFormulario()">Generar QR y Enviar</button>
        </form>
        <div id="qrcode"></div>
    </div>

    <!-- Librerías necesarias -->
    <script src="https://cdn.jsdelivr.net/npm/qrcode/build/qrcode.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/emailjs-com@3/dist/email.min.js"></script>
    <script>
        // Inicializar EmailJS (CAMBIAR con tus credenciales)
        emailjs.init("6rDpJ_n9rKSrPWEAO");  

        // Fecha de emisión automática
        const fechaEmisionInput = document.getElementById('fecha_emision');
        const now = new Date();
        fechaEmisionInput.value = now.toLocaleDateString('es-HN');

        function procesarFormulario() {
            const form = document.getElementById('certificationForm');
            if (!form.checkValidity()) {
                alert('Por favor, complete todos los campos requeridos.');
                return;
            }

            // Datos del formulario
            const data = {
                empresa: document.getElementById('empresa').value,
                rubro: document.getElementById('rubro').value,
                registro: document.getElementById('registro').value,
                direccion: document.getElementById('direccion').value,
                fecha_emision: document.getElementById('fecha_emision').value,
                fecha_vencimiento: document.getElementById('fecha_vencimiento').value,
                inspectores: document.getElementById('inspectores').value
            };

            // ----------------------
            // 1. Enviar por EmailJS
            // ----------------------
            emailjs.send("service_2b2ic5t","template_co2q6n8", data)
            .then(() => {
                console.log("✅ Correo enviado");
            })
            .catch(err => console.error("❌ Error al enviar correo:", err));

            // ----------------------
            // 2. Generar QR con URL
            // ----------------------
            const queryString = encodeURIComponent(JSON.stringify(data));
            const qrUrl = window.location.origin + window.location.pathname + "?data=" + queryString;

            const qrcodeDiv = document.getElementById('qrcode');
            qrcodeDiv.style.display = 'block';
            qrcodeDiv.innerHTML = "";

            QRCode.toCanvas(document.createElement("canvas"), qrUrl, { width: 200 }, function (err, canvas) {
                if (!err) qrcodeDiv.appendChild(canvas);
            });
        }

        // ----------------------
        // 3. Si se escanea el QR
        // ----------------------
        window.onload = () => {
            const params = new URLSearchParams(window.location.search);
            if (params.has("data")) {
                try {
                    const savedData = JSON.parse(decodeURIComponent(params.get("data")));
                    document.getElementById("certificationForm").style.display = "none";
                    const qrcodeDiv = document.getElementById("qrcode");
                    qrcodeDiv.style.display = "block";
                    qrcodeDiv.innerHTML = `
                        <h2>Certificado</h2>
                        <p><b>Empresa:</b> ${savedData.empresa}</p>
                        <p><b>Rubro:</b> ${savedData.rubro}</p>
                        <p><b>Registro:</b> ${savedData.registro}</p>
                        <p><b>Dirección:</b> ${savedData.direccion}</p>
                        <p><b>Fecha de Emisión:</b> ${savedData.fecha_emision}</p>
                        <p><b>Fecha de Vencimiento:</b> ${savedData.fecha_vencimiento}</p>
                        <p><b>Inspector(es):</b> ${savedData.inspectores}</p>
                    `;
                } catch (e) {
                    console.error("Error leyendo datos del QR:", e);
                }
            }
        }
    </script>
</body>
</html>
