# _Ofertas_barberia_
Precios de la barberia 
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ofertas de Corte de Cabello</title>
</head>
<body>
    <h1>Ofertas de Corte de Cabello</h1>
    <form id="ofertasForm">
        <label>
            <input type="checkbox" name="servicio" value="250"> Corte sencillo: $250
        </label><br>
        <label>
            <input type="checkbox" name="servicio" value="300"> Degradado: $300
        </label><br>
        <label>
            <input type="checkbox" name="servicio" value="50"> Diseños: $50 ó +
        </label><br>
        <label>
            <input type="checkbox" name="servicio" value="50"> Cejas: $50
        </label><br>
        <label>
            <input type="checkbox" name="servicio" value="100"> Corte pigmentado: $100
        </label><br>
        <label>
            <input type="checkbox" name="servicio" value="200"> Cejas pigmentadas: $200
        </label><br>
    </form>
    <h2>Total: $<span id="total">0</span></h2>

    <script>
        const form = document.getElementById('ofertasForm');
        const totalElement = document.getElementById('total');

        form.addEventListener('change', () => {
            let total = 0;
            form.querySelectorAll('input[name="servicio"]:checked').forEach(checkbox => {
                total += parseInt(checkbox.value);
            });
            totalElement.textContent = total;
        });
    </script>
</body>
</html>
