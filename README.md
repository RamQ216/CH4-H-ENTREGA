Pipeline de Extracción y Análisis de Libros
Este proyecto implementa un flujo completo de datos (ETL) que extrae información de un catálogo web, la estructura en una base de datos relacional y realiza pruebas de rendimiento (benchmarking).

1. Componentes del Pipeline
Extracción (Scraping)
Tecnología: BeautifulSoup y requests.

Proceso: Navega por el catálogo de Books to Scrape, extrayendo títulos, precios, calificaciones y disponibilidad.

Manejo de Errores: Valida códigos de respuesta HTTP (e.g., 200 OK) antes de procesar.

Almacenamiento (Persistencia)
Motor: SQLite3.

Esquema: Tablas relacionales para categories y books, utilizando llaves foráneas para mantener la integridad referencial.

Integración: Uso de Pandas para la ingesta masiva de datos mediante to_sql.

Optimización y Análisis
Benchmarking: Compara tiempos de ejecución de consultas pesadas con y sin índices de base de datos.

Resultados: Demuestra la mejora en el rendimiento (Full Table Scan vs. Index Scan).

2. Requisitos de Ejecución
Entorno: Jupyter Notebook / Google Colab.
Librerías: pandas, sqlite3, beautifulsoup4, requests.
Archivos: El notebook full.ipynb genera automáticamente el archivo libros_pingüino.db.

