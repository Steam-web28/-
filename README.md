<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Química: Materia, Sistemas Ácido-Base y pH</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-color: #f5f5f5;
            color: #333;
            display: flex;
            flex-direction: column;
        }
        .header {
            background: #1a237e;
            color: white;
            text-align: center;
            padding: 1rem; /* Encabezado más pequeño */
            position: relative;
        }
        .toggle-button {
            background-color: #2980b9;
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
            position: absolute;
            right: 20px; /* Posición del botón */
            top: 10px;
        }
        .main-container {
            display: flex;
            max-width: 1200px;
            margin: 0 auto;
            background-color: white;
            box-shadow: 0 0 15px rgba(0,0,0,0.1);
            flex-grow: 1;
        }
        .sidebar {
            position: fixed; /* Mantenerlo fijo */
            left: -400px; /* Inicialmente oculto */
            width: 300px;
            background-color: #f8f9fa;
            padding: 20px;
            border-right: 1px solid #dee2e6;
            height: 100vh;
            overflow-y: auto;
            transition: left 0.3s; /* Suave transición */
        }
        .sidebar h2 {
            font-size: 1.5rem;
        }
        .sidebar ul {
            list-style-type: none;
            padding: 0;
            margin: 0;
        }
        .sidebar a {
            color: #1a237e;
            text-decoration: none;
            display: block;
            padding: 0.5rem;
            border-radius: 4px;
            font-size: 1.1rem;
        }
        .sidebar a:hover {
            background: #e8eaf6;
        }
        .content-section {
            flex-grow: 1;
            padding: 2rem;
        }
        h2 {
            color: #1a237e;
            border-bottom: 2px solid #1a237e;
            padding-bottom: 0.5rem;
            margin-top: 2rem;
        }
        h3 {
            color: #283593;
        }
        p {
            text-align: justify;
        }
        .reference {
            margin-top: 2rem;
            padding-top: 1rem;
            border-top: 1px solid #dee2e6;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 12px;
            text-align: center;
        }
        th {
            background-color: #2980b9;
            color: white;
        }
        footer {
            background: #1a237e;
            color: white;
            text-align: center;
            padding: 15px 0;
            margin-top: auto;
        }
        .image-container {
            text-align: center;
            margin: 20px 0;
        }
        .image-container img {
            max-width: 80%;
            height: auto;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
    </style>
</head>
<body>
    <header class="header">
        <h1>Información sobre el pH</h1>
        <button class="toggle-button" onclick="toggleSidebar()">Índice</button>
    </header>

    <div class="main-container">
        <nav class="sidebar" id="sidebar">
            <h2>Índice</h2>
            <ul>
                <li><a href="#historia">Historia</a></li>
                <li><a href="#definicion">Definición</a></li>
                <li><a href="#ph">pH</a></li>
                <li><a href="#poh">pOH</a></li>
                <li><a href="#medicion">Medición</a></li>
                <li><a href="#indicadores">Indicadores de pH</a></li>
                <li><a href="#soluciones">Soluciones no acuosas</a></li>
                <li><a href="#escala">Escala de pH absoluta unificada</a></li>
                <li><a href="#extremos">Extremos de las mediciones de pH</a></li>
                <li><a href="#aplicaciones">Aplicaciones</a></li>
                <li><a href="#ph-suelo">pH en el suelo</a></li>
                <li><a href="#ph-plantas">pH en las plantas</a></li>
                <li><a href="#ph-oceano">pH en el océano</a></li>
                <li><a href="#escalas-oceanografia">Tres escalas de pH en oceanografía</a></li>
                <li><a href="#ph-alimentos">pH en los alimentos</a></li>
                <li><a href="#ph-fluidos">pH de varios fluidos corporales</a></li>
                <li><a href="#calculos">Cálculos de pH</a></li>
                <li><a href="#acidos-bases">Ácidos y bases fuertes/débiles</a></li>
                <li><a href="#metodo">Método general</a></li>
                <li><a href="#referencias">Referencias</a></li>
                <li><a href="#visto-tambien">Véase también</a></li>
            </ul>
        </nav>

        <main class="content-section">
            <p class="intro">La comprensión de la materia y sus transformaciones constituye uno de los pilares fundamentales de la química moderna. Este estudio examina las clasificaciones esenciales de la materia, profundiza en el comportamiento del agua como solvente universal y analiza los conceptos fundamentales de los sistemas ácido-base.</p>

            <section id="historia">
                <h2>Historia</h2>
                <p>El concepto de pH fue introducido en 1909 por Søren P. L. Sørensen, un químico danés, para expresar la acidez o alcalinidad de soluciones. Desde entonces, ha sido fundamental en diversas áreas de la química, biología y medicina.</p>
                <div class="image-container">
                    <img src="historia.jpeg" alt="Historia del pH">
                </div>
            </section>

            <section id="definicion">
                <h2>Definición</h2>
                <p>El pH es una medida que expresa el grado de acidez o alcalinidad de una solución acuosa. Representa la concentración de iones hidrógeno (H⁺) en la solución, que determina si es ácida, neutra o alcalina.</p>
                <p><strong>Clasificación de soluciones:</strong></p>
                <ul>
                    <li>Ácido: pH < 7 (ejemplo: jugo de limón)</li>
                    <li>Neutro: pH = 7 (ejemplo: agua pura)</li>
                    <li>Alcalino: pH > 7 (ejemplo: solución de bicarbonato)</li>
                </ul>
                <div class="image-container">
                    <img src="Definicion.jpeg" alt="Definición de pH">
                </div>
            </section>

            <section id="ph">
                <h2>pH</h2>
                <p>El pH se mide en una escala que va de 0 a 14. Un pH menor que 7 indica acidez, mientras que un pH mayor que 7 indica alcalinidad. El pH 7 es considerado neutro.</p>
            </section>

            <section id="poh">
                <h2>pOH</h2>
                <p>El pOH es otra medida que indica la concentración de iones hidroxilo (OH⁻) en una solución. La relación entre pH y pOH es: pH + pOH = 14.</p>
            </section>

            <section id="medicion">
                <h2>Medición</h2>
                <p>El pH se puede medir mediante varios métodos, incluyendo el uso de un potenciómetro y papel indicador de pH.</p>
            </section>

            <section id="indicadores">
                <h2>Indicadores de pH</h2>
                <p>Los indicadores son sustancias que cambian de color dependiendo del pH de la solución. Por ejemplo, la fenolftaleína es incolora en pH ácido y rosa en pH básico.</p>
            </section>

            <section id="soluciones">
                <h2>Soluciones no acuosas</h2>
                <p>El concepto de pH también se aplica a soluciones no acuosas, aunque con algunas limitaciones y consideraciones adicionales.</p>
            </section>

            <section id="escala">
                <h2>Escala de pH absoluta unificada</h2>
                <p>La escala de pH puede ser ajustada para unificar diferentes mediciones en condiciones estándar.</p>
            </section>

            <section id="extremos">
                <h2>Extremos de las mediciones de pH</h2>
                <p>Las mediciones de pH pueden tener limitaciones, especialmente en soluciones extremas.</p>
            </section>

            <section id="aplicaciones">
                <h2>Aplicaciones</h2>
                <p>El pH tiene aplicaciones en diversas áreas, incluyendo la agricultura, medicina y tratamiento de aguas.</p>
            </section>

            <section id="ph-suelo">
                <h2>pH en el suelo</h2>
                <p>El pH del suelo es un factor crítico que influye en la disponibilidad de nutrientes para las plantas.</p>
            </section>

            <section id="ph-plantas">
                <h2>pH en las plantas</h2>
                <p>El pH del agua que absorben las plantas también afecta su salud y crecimiento.</p>
            </section>

            <section id="ph-oceano">
                <h2>pH en el océano</h2>
                <p>El pH del océano está cambiando debido a la absorción de CO₂, lo que afecta a los ecosistemas marinos.</p>
            </section>

            <section id="escalas-oceanografia">
                <h2>Tres escalas de pH en oceanografía</h2>
                <p>En oceanografía, se utilizan tres escalas de pH para medir la acidez del océano: la escala total, la escala libre y la escala de actividad.</p>
            </section>

            <section id="ph-alimentos">
                <h2>pH en los alimentos</h2>
                <p>El pH es un factor importante en la conservación de alimentos y en la fermentación.</p>
            </section>

            <section id="ph-fluidos">
                <h2>pH de varios fluidos corporales</h2>
                <p>El pH de fluidos como la sangre y la orina es crucial para mantener la homeostasis en el cuerpo.</p>
            </section>

            <section id="calculos">
                <h2>Cálculos de pH</h2>
                <p>El pH puede calcularse utilizando la siguiente fórmula:</p>
                <p>pH = -log[H⁺]</p>
            </section>

            <section id="acidos-bases">
                <h2>Ácidos y bases fuertes/débiles</h2>
                <p>La clasificación de los ácidos y bases como fuertes o débiles es esencial para comprender su comportamiento en solución.</p>
            </section>

            <section id="metodo">
                <h2>Método general</h2>
                <p>Para determinar el pH de una solución, se puede utilizar un potenciómetro o papel indicador de pH.</p>
            </section>

            <section id="referencias">
                <h2>Referencias</h2>
                <p>Lista de referencias y recursos utilizados para esta información.</p>
            </section>

            <section id="visto-tambien">
                <h2>Véase también</h2>
                <p>Otros temas relacionados con el pH y la química.</p>
            </section>
        </main>
    </div>

    <footer>
        <p>&copy; 2024 Información sobre el pH</p>
    </footer>

    <script>
        function toggleSidebar() {
            const sidebar = document.getElementById('sidebar');
            if (sidebar.style.left === '0px') {
                sidebar.style.left = '-400px'; // Ocultar
            } else {
                sidebar.style.left = '0px'; // Mostrar
            }
        }
    </script>
</body>
</html>
