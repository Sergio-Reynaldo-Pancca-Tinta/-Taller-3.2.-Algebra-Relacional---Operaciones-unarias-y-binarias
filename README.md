<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Infografía: Álgebra Relacional - Operaciones Unarias y Binarias | Northwind & Pubs</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #eef2f7;
            font-family: 'Inter', sans-serif;
            line-height: 1.4;
            padding: 2rem 1.5rem;
            color: #1a2c3e;
        }

        /* contenedor principal estilo infografía */
        .infografia {
            max-width: 1400px;
            margin: 0 auto;
            background: white;
            border-radius: 2rem;
            box-shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.2);
            overflow: hidden;
            transition: all 0.2s;
        }

        /* header académico */
        .header-academico {
            background: linear-gradient(135deg, #0b2b3b 0%, #1a4b6e 100%);
            color: white;
            padding: 1.8rem 2rem 1.5rem 2rem;
        }

        .universidad {
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            flex-wrap: wrap;
            gap: 0.5rem;
            font-weight: 600;
            border-bottom: 1px solid rgba(255,255,255,0.2);
            padding-bottom: 0.75rem;
            margin-bottom: 1rem;
        }

        .uni-nombre {
            font-size: 1.1rem;
            letter-spacing: 1px;
        }

        .curso-docente {
            font-size: 0.85rem;
            opacity: 0.9;
        }

        .titulo-taller {
            font-size: 2rem;
            font-weight: 800;
            margin: 0.5rem 0 0.25rem;
            letter-spacing: -0.01em;
        }

        .subtitulo {
            font-size: 1rem;
            font-weight: 400;
            opacity: 0.85;
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
        }

        .equipo {
            background: rgba(255,255,255,0.12);
            padding: 0.3rem 1rem;
            border-radius: 40px;
            font-size: 0.8rem;
            font-weight: 500;
        }

        /* grid infografía */
        .grid-contenido {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1.8rem;
            padding: 2rem 2rem 1.5rem;
        }

        .card {
            background: #ffffff;
            border-radius: 1.5rem;
            box-shadow: 0 8px 20px rgba(0,0,0,0.05);
            overflow: hidden;
            transition: transform 0.2s, box-shadow 0.2s;
            border: 1px solid #e9edf2;
        }

        .card:hover {
            transform: translateY(-4px);
            box-shadow: 0 20px 28px -12px rgba(0, 0, 0, 0.12);
        }

        .card-header {
            background: #f8fafd;
            padding: 1rem 1.5rem;
            border-bottom: 2px solid #dce5ec;
            display: flex;
            align-items: center;
            gap: 0.75rem;
        }

        .card-header i {
            font-size: 1.8rem;
            color: #2c7da0;
        }

        .card-header h2 {
            font-size: 1.5rem;
            font-weight: 700;
            margin: 0;
            color: #0f3b4f;
        }

        .card-body {
            padding: 1.2rem 1.5rem 1.5rem;
        }

        .operacion-lista {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .operacion-item {
            border-left: 4px solid #2c7da0;
            padding-left: 1rem;
            background: #fefefe;
        }

        .operacion-titulo {
            font-weight: 800;
            font-size: 1.1rem;
            color: #1e5a74;
            margin-bottom: 0.3rem;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .badge-tipo {
            background: #e1ecf4;
            border-radius: 30px;
            font-size: 0.65rem;
            padding: 0.2rem 0.7rem;
            font-weight: 600;
            color: #1e5a74;
        }

        .descripcion {
            font-size: 0.85rem;
            color: #2c3e4e;
            margin-bottom: 0.4rem;
            line-height: 1.4;
        }

        .ejemplo {
            background: #f1f5f9;
            padding: 0.5rem 0.7rem;
            border-radius: 12px;
            font-family: 'Courier New', monospace;
            font-size: 0.75rem;
            color: #0e4b6e;
            margin-top: 0.4rem;
        }

        .diagrama-nota {
            background: #eef2fa;
            border-radius: 1rem;
            padding: 0.8rem 1rem;
            margin-top: 1rem;
            font-size: 0.8rem;
            display: flex;
            align-items: center;
            gap: 12px;
            border: 1px solid #d4e0ea;
        }

        .badge-bd {
            background: #1f6392;
            color: white;
            border-radius: 20px;
            padding: 0.2rem 0.8rem;
            font-weight: 600;
            font-size: 0.7rem;
        }

        .full-width {
            grid-column: span 2;
        }

        .img-simulada {
            background: #e4eef5;
            border-radius: 1rem;
            padding: 0.8rem 1rem;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            gap: 10px;
        }

        .mock-botones {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        .boton-ejemplo {
            background: white;
            border-radius: 40px;
            padding: 0.3rem 0.9rem;
            box-shadow: 0 1px 2px rgba(0,0,0,0.05);
            font-size: 0.7rem;
            font-weight: 500;
            border: 1px solid #cbdde9;
            color: #1f5e7e;
        }

        .footer-conclusiones {
            background: #f0f4f9;
            padding: 1.5rem 2rem;
            border-top: 1px solid #dce5ec;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 1.5rem;
        }

        .conclusiones {
            flex: 2;
        }

        .conclusiones h3, .sugerencias h3 {
            font-size: 1.1rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
            gap: 8px;
            color: #144e68;
        }

        .conclusiones p, .sugerencias p {
            font-size: 0.8rem;
            color: #2c4a5e;
            line-height: 1.5;
        }

        .repo-links {
            background: white;
            border-radius: 1rem;
            padding: 0.7rem 1rem;
            margin-top: 0.8rem;
            font-size: 0.75rem;
            display: flex;
            gap: 1.2rem;
            flex-wrap: wrap;
        }

        .repo-links a {
            text-decoration: none;
            color: #1f6392;
            font-weight: 600;
        }

        hr {
            margin: 0.5rem 0;
        }

        @media (max-width: 860px) {
            .grid-contenido {
                grid-template-columns: 1fr;
                gap: 1.2rem;
                padding: 1.5rem;
            }
            .full-width {
                grid-column: span 1;
            }
            .header-academico {
                padding: 1.2rem;
            }
            .titulo-taller {
                font-size: 1.5rem;
            }
        }

        .iconito {
            width: 24px;
            text-align: center;
        }
        .referencias {
            background: #fafcff;
            border-radius: 1rem;
            font-size: 0.7rem;
            padding: 0.8rem;
            margin-top: 0.5rem;
            border: 1px solid #e2e8f0;
        }
    </style>
</head>
<body>
<div class="infografia">
    <div class="header-academico">
        <div class="universidad">
            <span class="uni-nombre"><i class="fas fa-university"></i> UNIVERSIDAD ANDINA DEL CUSCO - FACULTAD DE INGENIERÍA Y ARQUITECTURA</span>
            <span class="curso-docente">Modelado de Base de Datos | Docente: Hugo Espetia Huamanga</span>
        </div>
        <div class="titulo-taller">
            Álgebra Relacional <span style="font-weight: 500;">|</span> Operaciones Unarias y Binarias
        </div>
        <div class="subtitulo">
            <span><i class="fas fa-database"></i> Northwind · Pubs · ADO.NET Entity Framework · LINQ · C#</span>
            <span class="equipo"><i class="fas fa-users"></i> Los Dog Chamos 2.0 (ahora sí)</span>
        </div>
        <div class="equipo" style="margin-top: 8px; background: rgba(255,255,240,0.15); width: fit-content;">
            Andia Palomino R. | Mamani Apaza R. | Pancca Tinta S. | Ramos Hancco D.
        </div>
    </div>

    <div class="grid-contenido">
        <!-- COLUMNA IZQUIERDA: Operaciones Unarias -->
        <div class="card">
            <div class="card-header">
                <i class="fas fa-filter"></i>
                <h2>Operaciones Unarias</h2>
            </div>
            <div class="card-body">
                <div class="operacion-lista">
                    <div class="operacion-item">
                        <div class="operacion-titulo"><span class="badge-tipo">σ (Sigma)</span> Selección</div>
                        <div class="descripcion">Filtra filas que cumplen una condición específica. Ejemplo práctico: autores de un estado o libros con precio > valor.</div>
                        <div class="ejemplo">📘 LINQ: <strong>db.Autores.Where(a => a.estado == "CA")</strong> → Autores de California (Pubs)</div>
                    </div>
                    <div class="operacion-item">
                        <div class="operacion-titulo"><span class="badge-tipo">π (Pi)</span> Proyección</div>
                        <div class="descripcion">Extrae columnas específicas, eliminando atributos irrelevantes. Reduce la dimensionalidad.</div>
                        <div class="ejemplo">📖 Proyección: nombres de autores, títulos de libros → <strong>Select(a => new { a.nombre, a.apellido })</strong></div>
                    </div>
                    <div class="operacion-item">
                        <div class="operacion-titulo"><span class="badge-tipo">ρ (Rho)</span> Renombramiento</div>
                        <div class="descripcion">Asigna alias a relaciones o atributos para mejorar comprensión y evitar ambigüedades.</div>
                        <div class="ejemplo">🔄 En LINQ: <strong>.Select(x => new { NombreCompleto = x.au_fname })</strong> → Alias amigable</div>
                    </div>
                </div>
                <div class="diagrama-nota">
                    <i class="fas fa-table" style="font-size: 1.8rem; color:#2c7da0;"></i>
                    <span><strong>Implementación en Northwind & Pubs</strong> <br> Se realizaron consultas para filtrar autores por estado (selección), obtener solo nombres/títulos (proyección) y usar alias en resultados complejos.</span>
                </div>
            </div>
        </div>

        <!-- COLUMNA DERECHA: Operaciones Binarias -->
        <div class="card">
            <div class="card-header">
                <i class="fas fa-code-branch"></i>
                <h2>Operaciones Binarias</h2>
            </div>
            <div class="card-body">
                <div class="operacion-lista">
                    <div class="operacion-item">
                        <div class="operacion-titulo"><span class="badge-tipo">∪ (Union)</span> Unión</div>
                        <div class="descripcion">Combina tuplas de dos relaciones compatibles, eliminando duplicados. Unión de resultados de distintas tablas.</div>
                        <div class="ejemplo">🔗 Ejemplo conceptual: Autores de CA ∪ Autores de NY → usando <strong>Union()</strong> en LINQ</div>
                    </div>
                    <div class="operacion-item">
                        <div class="operacion-titulo"><span class="badge-tipo">− (Difference)</span> Diferencia</div>
                        <div class="descripcion">Registros presentes en una consulta pero no en otra. Identifica libros no vendidos o estados sin tiendas.</div>
                        <div class="ejemplo">📉 Diferencia: Libros publicados excepto aquellos con ventas registradas → <strong>Except()</strong> en LINQ</div>
                    </div>
                    <div class="operacion-item">
                        <div class="operacion-titulo"><span class="badge-tipo">× (Producto Cartesiano)</span> Producto Cartesiano</div>
                        <div class="descripcion">Combina cada fila de una tabla con cada fila de otra, generando todas las combinaciones posibles.</div>
                        <div class="ejemplo">🃏 Producto Cartesiano entre autores y títulos → análisis de relaciones cruzadas; en LINQ: <strong>from a in autores from t in titulos select new { a, t }</strong></div>
                    </div>
                </div>
                <div class="diagrama-nota">
                    <i class="fas fa-project-diagram"></i>
                    <span><strong>Caso Northwind / Pubs</strong> · Unión de consultas, diferencia para hallar libros sin ventas y producto cartesiano exploratorio.</span>
                </div>
            </div>
        </div>

        <!-- Sección destacada: Entity Framework y base de datos pubs + northwind (unión visual) -->
        <div class="card full-width">
            <div class="card-header">
                <i class="fas fa-cogs"></i>
                <h2>Implementación Tecnológica · Entity Framework + LINQ</h2>
            </div>
            <div class="card-body">
                <div style="display: flex; flex-wrap: wrap; gap: 20px; justify-content: space-between;">
                    <div style="flex: 1; min-width: 180px;">
                        <div class="badge-bd" style="display: inline-block; margin-bottom: 10px;"><i class="fas fa-database"></i> Northwind & Pubs</div>
                        <p style="font-size: 0.85rem;">Se utilizó ADO.NET Entity Framework para mapear las tablas: autores, títulos, ventas, editoriales, tiendas. Las operaciones del álgebra relacional se tradujeron a consultas declarativas en LINQ (Language Integrated Query).</p>
                        <div class="mock-botones" style="margin-top: 12px;">
                            <span class="boton-ejemplo"><i class="fas fa-search"></i> Selección</span>
                            <span class="boton-ejemplo"><i class="fas fa-columns"></i> Proyección</span>
                            <span class="boton-ejemplo"><i class="fas fa-tag"></i> Renombramiento</span>
                            <span class="boton-ejemplo"><i class="fas fa-layer-group"></i> Unión</span>
                            <span class="boton-ejemplo"><i class="fas fa-minus-circle"></i> Diferencia</span>
                            <span class="boton-ejemplo"><i class="fas fa-times"></i> Producto Cartesiano</span>
                        </div>
                    </div>
                    <div style="flex: 1; background: #f3f9ff; border-radius: 24px; padding: 0.8rem;">
                        <i class="fas fa-code"></i> <strong>Ejemplo concreto en Pubs (C#)</strong>
                        <div class="ejemplo" style="background:#eaf2f9; margin-top: 8px;">
                            // Selección: autores de 'UT'<br>
                            var autoresUt = db.Authors.Where(a => a.state == "UT");<br>
                            // Proyección: título y precio<br>
                            var titulosCaros = db.Titles.Where(t => t.price > 20).Select(t => new { t.title, t.price });<br>
                            // Diferencia: títulos sin ventas<br>
                            var sinVentas = db.Titles.Except(db.Sales.Select(s => s.Title));
                        </div>
                    </div>
                </div>
                <div class="img-simulada" style="margin-top: 1rem;">
                    <span><i class="fas fa-check-circle" style="color:#1e7e34;"></i> <strong>Resultados en consola y visual studio</strong> — 18 botones interactivos (9 unarios + 9 binarios) demostrados en el taller.</span>
                    <span class="badge-bd"><i class="fas fa-github"></i> Repositorio: Los Dog Chamos 2.0</span>
                </div>
            </div>
        </div>

        <!-- Bloque de diagramas y evidencia visual -->
        <div class="card">
            <div class="card-header">
                <i class="fas fa-project-diagram"></i>
                <h2>Modelo Diagramas · Northwind & Pubs</h2>
            </div>
            <div class="card-body">
                <p style="font-size:0.85rem; margin-bottom: 10px;">Se trabajó con los esquemas de Northwind y Pubs (clientes, pedidos, autores, títulos, ventas, tiendas). Las imágenes adjuntas en el informe muestran:</p>
                <ul style="margin-left: 1.2rem; font-size: 0.8rem; color: #2c556e;">
                    <li>Diagrama relacional de Northwind (imagen 1)</li>
                    <li>Conexión SQL Server en Visual Studio (imagen 2)</li>
                    <li>Diagrama base de datos Pubs (imagen 3)</li>
                    <li>Interfaz con 18 botones unarios/binarios (imagen 5 y 7)</li>
                    <li>Resultados de ejecución (imagen 6, 8)</li>
                </ul>
                <div class="referencias">
                    <i class="fas fa-image"></i> <strong>Nota:</strong> Las capturas demostraron filtrado por estados, proyección de títulos, renombramiento, unión de consultas y diferencia de conjuntos.
                </div>
            </div>
        </div>

        <div class="card">
            <div class="card-header">
                <i class="fas fa-chalkboard-teacher"></i>
                <h2>Metodología y Aprendizaje</h2>
            </div>
            <div class="card-body">
                <p style="font-size: 0.85rem;"><strong>Álgebra relacional como fundamento</strong>: base teórica de BD relacionales. Se aplicaron operaciones unarias (σ, π, ρ) y binarias (∪, −, ×) en un entorno moderno .NET con Entity Framework y LINQ, demostrando que el álgebra subyace incluso en ORM.</p>
                <div class="diagrama-nota" style="margin-top: 12px;">
                    <i class="fab fa-microsoft"></i>
                    <span>Se fortalecieron habilidades de manipulación declarativa, legibilidad del código y uso de patrones de acceso a datos.</span>
                </div>
                <p style="font-size:0.75rem; margin-top: 12px; color:#386a82;"><i class="fas fa-lightbulb"></i> Conclusión clave: Las operaciones unarias y binarias se pueden traducir directamente a métodos LINQ (Where, Select, Union, Except, SelectMany, etc.) probando la vigencia del álgebra relacional.</p>
            </div>
        </div>

        <!-- Conclusiones y Sugerencias a dos columnas dentro del mismo full-width -->
        <div class="full-width" style="background: transparent; padding: 0;">
            <div class="footer-conclusiones" style="border-radius: 1.5rem; margin-top: 0.5rem;">
                <div class="conclusiones">
                    <h3><i class="fas fa-check-double"></i> Conclusiones</h3>
                    <p>✓ La implementación práctica permitió comprender el álgebra relacional como base esencial de las consultas SQL y ORM.<br>
                    ✓ Entity Framework + LINQ facilitan representar selección, proyección, renombramiento, unión, diferencia y producto cartesiano de forma elegante.<br>
                    ✓ Se demostró la identificación de libros no vendidos (diferencia) y autores por región (selección), entre otros casos reales sobre Pubs y Northwind.<br>
                    ✓ Las operaciones mejoran la eficiencia en la manipulación de información y reducen la complejidad del código.</p>
                </div>
                <div class="sugerencias">
                    <h3><i class="fas fa-comment-dots"></i> Sugerencias</h3>
                    <p>🔹 Profundizar en LINQ y Entity Framework para aplicaciones empresariales complejas.<br>
                    🔹 Incorporar interfaces gráficas para visualizar resultados de las operaciones relacionales de forma dinámica.<br>
                    🔹 Documentar el código y aplicar buenas prácticas de mantenibilidad.<br>
                    🔹 Integrar reportes visuales que permitan interpretar mejor las uniones y productos cartesianos.</p>
                </div>
            </div>
        </div>

        <!-- Bibliografía + Links repositorio -->
        <div class="full-width" style="padding: 0 2rem 1.8rem 2rem;">
            <div class="repo-links">
                <div><i class="fab fa-github"></i> <strong>Repositorio GitHub:</strong> <a href="#">github.com/Sergio-Reynaldo-Panca-Tinta/-Taller-3.2-Algebra-Relacional</a></div>
                <div><i class="fas fa-chalkboard"></i> <strong>Infografía online:</strong> <a href="#">sergio-reynaldo-panca-tinta.github.io/-Taller-3.2-Algebra-Relacional-Operaciones-unarias-y-binarias</a></div>
            </div>
            <div class="referencias" style="margin-top: 0.5rem;">
                <i class="fas fa-book-open"></i> <strong>Bibliografia recomendada:</strong> Microsoft Learn (Entity Framework, SQL Server), Elmasri & Navathe (Fundamentals of Database Systems, 7th ed.), Silberschatz (Database System Concepts, 7th ed.).
                <hr style="margin: 8px 0;">
                <i class="fas fa-database"></i> Base de datos de ejemplo: Northwind & Pubs · Documentación oficial Microsoft.
            </div>
            <div style="text-align: right; margin-top: 1rem; font-size: 0.7rem; color: #6c8eaa;">
                <i class="fas fa-calendar-alt"></i> Cusco - Perú, 2026 | Los Dog Chamos 2.0 (ahora sí)
            </div>
        </div>
    </div>
</div>
</body>
</html>
