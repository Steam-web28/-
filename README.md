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
            padding: 2rem; /* Aumentado para mayor espacio */
            margin-bottom: 1rem; /* Espacio entre el encabezado y el contenido */
            position: static; /* Asegurando que no se mueva */
        }
        .header h1 {
            font-size: 1.5rem;
            margin: 0;
        }
        .main-container {
            display: flex;
            max-width: 1200px;
            margin: 0 auto;
            background-color: white;
            box-shadow: 0 0 15px rgba(0,0,0,0.1);
            flex-grow: 1;
            margin-left: 50px;
        }
        .sidebar {
            position: fixed;
            top: 80px;
            left: -400px;
            width: 400px;
            background-color: #f8f9fa;
            padding: 20px;
            border-right: 1px solid #dee2e6;
            height: calc(100vh - 80px);
            overflow-y: auto;
            transition: left 0.3s;
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
        .toggle-button {
            background-color: #1a237e;
            color: white;
            border: none;
            padding: 10px 15px;
            cursor: pointer;
            margin: 20px;
            border-radius: 5px;
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 1001;
        }
        .toggle-button:hover {
            background-color: #3949ab;
        }
    </style>
</head>
<body>
    <header class="header">
        <h1>Información sobre el pH</h1>
    </header>

    <div class="main-container">
        <nav class="sidebar" id="sidebar">
            <h2>Índice</h2>
            <ul>
                <li><a href="#historia" onclick="closeSidebar()">Historia</a></li>
                <li><a href="#definicion" onclick="closeSidebar()">Definición</a></li>
                <li><a href="#ph" onclick="closeSidebar()">pH</a></li>
                <li><a href="#poh" onclick="closeSidebar()">pOH</a></li>
                <li><a href="#medicion" onclick="closeSidebar()">Medición</a></li>
                <li><a href="#indicadores" onclick="closeSidebar()">Indicadores de pH</a></li>
                <li><a href="#soluciones" onclick="closeSidebar()">Soluciones no acuosas</a></li>
                <li><a href="#escala" onclick="closeSidebar()">Escala de pH absoluta unificada</a></li>
                <li><a href="#extremos" onclick="closeSidebar()">Extremos de las mediciones de pH</a></li>
                <li><a href="#aplicaciones" onclick="closeSidebar()">Aplicaciones</a></li>
                <li><a href="#ph-suelo" onclick="closeSidebar()">pH en el suelo</a></li>
                <li><a href="#ph-plantas" onclick="closeSidebar()">pH en las plantas</a></li>
                <li><a href="#ph-oceano" onclick="closeSidebar()">pH en el océano</a></li>
                <li><a href="#escalas-oceanografia" onclick="closeSidebar()">Tres escalas de pH en oceanografía</a></li>
                <li><a href="#ph-alimentos" onclick="closeSidebar()">pH en los alimentos</a></li>
                <li><a href="#ph-fluidos" onclick="closeSidebar()">pH de varios fluidos corporales</a></li>
                <li><a href="#calculos" onclick="closeSidebar()">Cálculos de pH</a></li>
                <li><a href="#acidos-bases" onclick="closeSidebar()">Ácidos y bases fuertes/débiles</a></li>
                <li><a href="#metodo" onclick="closeSidebar()">Método general</a></li>
                <li><a href="#referencias" onclick="closeSidebar()">Referencias</a></li>
                <li><a href="#visto-tambien" onclick="closeSidebar()">Véase también</a></li>
            </ul>
        </nav>

        <main class="content-section">
            <p class="intro">La comprensión de la materia y sus transformaciones constituye uno de los pilares fundamentales de la química moderna. Este estudio examina las clasificaciones esenciales de la materia, profundiza en el comportamiento del agua como solvente universal y analiza los conceptos fundamentales de los sistemas ácido-base.</p>

            <section id="historia">
                <h2>Historia</h2>
                <p>El concepto de pH fue introducido en 1909 por Søren P. L. Sørensen, un químico danés, para expresar la acidez o alcalinidad de soluciones. Desde entonces, ha sido fundamental en diversas áreas de la química, biología y medicina.</p>
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
            </section>

            <section id="ph">
                <h2>pH</h2>
                <p>El pH se mide en una escala que va de 0 a 14. Un pH menor que 7 indica acidez, mientras que un pH mayor que 7 indica alcalinidad. El pH 7 es considerado neutro.</p>
            </section>

            <section id="poh">
                <h2>pOH</h2>
                <p>El pOH es otra medida que expresa la concentración de iones hidróxido (OH⁻) en una solución. La relación entre pH y pOH se expresa mediante la ecuación: pH + pOH = 14.</p>
            </section>

            <section id="medicion">
                <h2>Medición</h2>
                <p>El pH se puede medir utilizando diversos métodos, como indicadores de pH, electrodos de pH y tiras reactivas. La precisión de la medición puede variar según el método utilizado.</p>
            </section>

            <section id="indicadores">
                <h2>Indicadores de pH</h2>
                <p>Los indicadores de pH son sustancias que cambian de color en función del pH de la solución. Ejemplos incluyen el tornasol y la fenolftaleína, que son comúnmente utilizados en laboratorios.</p>
            </section>

            <section id="soluciones">
                <h2>Soluciones no acuosas</h2>
                <p>Además de soluciones acuosas, el concepto de pH también se aplica a soluciones no acuosas, aunque su medición puede ser más complicada debido a la falta de agua como solvente.</p>
            </section>

            <section id="escala">
                <h2>Escala de pH absoluta unificada</h2>
                <p>La escala de pH absoluta unificada es un sistema más preciso para medir el pH de soluciones, que toma en cuenta factores como la temperatura y la composición del solvente.</p>
            </section>

            <section id="extremos">
                <h2>Extremos de las mediciones de pH</h2>
                <p>Las mediciones de pH pueden llegar a extremos, como valores por debajo de 0 o por encima de 14, en soluciones concentradas o en condiciones especiales.</p>
            </section>

            <section id="aplicaciones">
                <h2>Aplicaciones</h2>
                <p>El pH es crucial en diversas aplicaciones, incluyendo la agricultura, medicina, industria alimentaria y análisis ambiental, donde el control del pH puede afectar la calidad y seguridad de productos.</p>
            </section>

            <section id="ph-suelo">
                <h2>pH en el suelo</h2>
                <p>El pH del suelo afecta la disponibilidad de nutrientes para las plantas y su crecimiento. Suelos ácidos o alcalinos pueden limitar el desarrollo vegetal.</p>
            </section>

            <section id="ph-plantas">
                <h2>pH en las plantas</h2>
                <p>Las plantas tienen rangos óptimos de pH para la absorción de nutrientes. Cambios en el pH pueden influir en el crecimiento y salud de las plantas.</p>
            </section>

            <section id="ph-oceano">
                <h2>pH en el océano</h2>
                <p>El pH del océano ha estado disminuyendo debido al aumento de CO₂, lo que afecta la vida marina y los ecosistemas acuáticos.</p>
            </section>

            <section id="escalas-oceanografia">
                <h2>Tres escalas de pH en oceanografía</h2>
                <p>Existen tres escalas de pH en oceanografía que permiten medir la acidez del océano y su variación en diferentes condiciones ambientales.</p>
            </section>

            <section id="ph-alimentos">
                <h2>pH en los alimentos</h2>
                <p>El pH de los alimentos puede influir en su conservación y sabor. Por ejemplo, alimentos ácidos tienden a ser más preservados.</p>
            </section>

            <section id="ph-fluidos">
                <h2>pH de varios fluidos corporales</h2>
                <p>El pH de fluidos corporales como la sangre y la orina es crucial para mantener la homeostasis en el organismo.</p>
            </section>

            <section id="calculos">
                <h2>Cálculos de pH</h2>
                <p>Se pueden realizar cálculos para determinar el pH de soluciones utilizando fórmulas y datos de concentración de iones H⁺.</p>
            </section>

            <section id="acidos-bases">
                <h2>Ácidos y bases fuertes/débiles</h2>
                <p>Los ácidos y bases se clasifican como fuertes o débiles según su capacidad para disociarse en solución acuosa, afectando así el pH.</p>
            </section>

            <section id="metodo">
                <h2>Método general</h2>
                <p>El método general para determinar el pH implica la medición de la concentración de iones H⁺ y la utilización de la fórmula: pH = -log[H⁺].</p>
            </section>

            <section id="referencias">
                <h2>Referencias</h2>
                <p>1. Sørensen, S.P.L. (1909). "Die Methode der pH-Wert Bestimmung".</p>
                <p>2. Aiken, G.R., et al. (1994). "Acidity and pH". <em>Environmental Science & Technology</em>.</p>
            </section>

            <section id="visto-tambien">
                <h2>Véase también</h2>
                <ul>
                    <li><a href="#">Química orgánica</a></li>
                    <li><a href="#">Acidez y basicidad</a></li>
                    <li><a href="#">Efecto del pH en la salud</a></li>
                </ul>
            </section>
        </main>
    </div>

    <button class="toggle-button" onclick="toggleSidebar()">Índice</button>

    <footer>
        <p>© 2024 Química Moderna. Todos los derechos reservados.</p>
    </footer>

    <script>
        function toggleSidebar() {
            const sidebar = document.getElementById('sidebar');
            if (sidebar.style.left === '0px') {
                sidebar.style.left = '-400px';
            } else {
                sidebar.style.left = '0px';
            }
        }

        function closeSidebar() {
            const sidebar = document.getElementById('sidebar');
            sidebar.style.left = '-400px';
        }
    </script>
</body>
</html>
