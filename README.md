# Análisis de Base de Datos para Startup de Libros

Este proyecto analiza una base de datos de un servicio de libros para identificar **patrones de consumo, popularidad de autores y editoriales, y comportamiento de los usuarios** mediante reseñas y calificaciones. El objetivo es generar **insights accionables** que sirvan de base para la **propuesta de valor de un nuevo producto digital** dirigido a lectores, aprovechando el auge del mercado de aplicaciones de lectura post-pandemia.

### Herramientas y tipo de proyecto
![Python](https://img.shields.io/badge/python-357ebd?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23357ebd.svg?style=for-the-badge&logo=pandas&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-357ebd?style=for-the-badge&logo=postgresql&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-357ebd?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-357ebd?style=for-the-badge&logo=python&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-357ebd?style=for-the-badge&logo=tableau&logoColor=white)
![Análisis de datos](https://img.shields.io/badge/Análisis_de_datos-295F98?style=for-the-badge)
![Visualización de datos](https://img.shields.io/badge/Visualización_de_datos-295F98?style=for-the-badge)
![Base de datos relacional](https://img.shields.io/badge/Base_de_datos_relacional-295F98?style=for-the-badge)

## Preguntas clave
1. ¿Cuántos libros publicados después del año 2000 hay en el catálogo?
2. ¿Qué libros generan mayor interacción (reseñas) y mejor calificación promedio?
3. ¿Qué editorial lidera en volumen de publicaciones sustanciales (>50 páginas)?
4. ¿Qué autor tiene la calificación promedio más alta, considerando solo libros con al menos 50 calificaciones?
5. ¿Cuál es el comportamiento de los usuarios más activos (con más de 50 calificaciones) en cuanto a reseñas de texto?

## Metodología
- **Extracción de datos:** Se estableció conexión a la base de datos PostgreSQL mediante `SQLAlchemy` y se exploraron las tablas (`books`, `authors`, `publishers`, `ratings`, `reviews`).
- **Consultas SQL:** Se formularon consultas específicas para responder cada pregunta, utilizando agregaciones, joins, subconsultas y filtros (ej. `LEFT JOIN` para preservar catálogo, `COALESCE` para valores nulos, y condiciones como `HAVING COUNT(rating_id) >= 50` para garantizar robustez estadística).
- **Análisis y visualización:** Los resultados se presentaron en DataFrames de Pandas y se generó una gráfica de barras horizontales con etiquetas integradas para comunicar de forma clara el top de libros por reseñas y calificación.
- **Interpretación de resultados:** Cada hallazgo se vinculó a una conclusión de negocio, orientando futuras decisiones estratégicas.

## Conclusiones y recomendaciones
### Hallazgos principales:
- **Catálogo moderno:** 819 libros publicados después del 2000, lo que indica una oferta actualizada y atractiva para lectores contemporáneos.
- **Engagement:** Sagas como *Harry Potter* y *Twilight* lideran en número de reseñas, pero *Harry Potter* mantiene una calificación superior (4.41 vs 3.66), lo que sugiere que la calidad sostenida genera mayor lealtad.
- **Editorial clave:** *Penguin Books* es la editorial con más títulos de más de 50 páginas (42 libros), posicionándose como el socio comercial ideal para asegurar volumen de inventario.
- **Autor destacado:** *J.K. Rowling* presenta la calificación promedio más alta (4.29) entre libros con al menos 50 calificaciones, confirmando el valor de autores consagrados.
- **Usuarios influyentes:** Los lectores que califican más de 50 libros escriben en promedio 24.3 reseñas de texto, identificando un segmento de "super-usuarios" que generan contenido valioso para la comunidad.

### Recomendaciones estratégicas:
1. **Curaduría basada en sagas:** Implementar un sistema de recomendaciones que destaque colecciones completas (como Harry Potter) para capitalizar el interés en series de fantasía.
2. **Programa de "Lectores Expertos":** Crear un sistema de recompensas (badges, niveles, acceso anticipado) para usuarios con alta actividad, fomentando la generación de reseñas que ayuden a otros lectores.
3. **Alianza editorial prioritaria:** Establecer acuerdos de contenido con *Penguin Books* para garantizar un catálogo amplio y de calidad.
4. **Enfoque en libros modernos:** Mantener la curaduría centrada en publicaciones posteriores al año 2000, alineada con los gustos actuales.

## Diccionario de datos
- **books:** Información de cada libro (`book_id`, `author_id`, `title`, `num_pages`, `publication_date`, `publisher_id`).
- **authors:** Identificación y nombre de autores (`author_id`, `author`).
- **publishers:** Identificación y nombre de editoriales (`publisher_id`, `publisher`).
- **ratings:** Calificaciones de usuarios (`rating_id`, `book_id`, `username`, `rating`).
- **reviews:** Reseñas de texto de usuarios (`review_id`, `book_id`, `username`, `text`).

## Visualización interactiva
Puedes explorar los resultados de este análisis en el siguiente dashboard de Tableau Public:

[**Ver Dashboard: Top 10 Books**](https://public.tableau.com/app/profile/ari.de.le.n/viz/Top10Books_17737109047610/Dashboard1?publish=yes)

---

# Database Analysis for a Book Startup

This project analyzes a book service database to identify **consumption patterns, author and publisher popularity, and user behavior** through reviews and ratings. The goal is to generate **actionable insights** that serve as the foundation for the **value proposition of a new digital product** aimed at readers, capitalizing on the post-pandemic reading app market boom.

### Tools and Project Type
![Python](https://img.shields.io/badge/python-357ebd?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23357ebd.svg?style=for-the-badge&logo=pandas&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-357ebd?style=for-the-badge&logo=postgresql&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-357ebd?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-357ebd?style=for-the-badge&logo=python&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-357ebd?style=for-the-badge&logo=tableau&logoColor=white)
![Data Analysis](https://img.shields.io/badge/Data_Analysis-295F98?style=for-the-badge)
![Data Visualization](https://img.shields.io/badge/Data_Visualization-295F98?style=for-the-badge)
![Relational Database](https://img.shields.io/badge/Relational_Database-295F98?style=for-the-badge)

## Key Questions
1. How many books published after the year 2000 are in the catalog?
2. Which books generate the most interaction (reviews) and the highest average rating?
3. Which publisher leads in substantial publications (>50 pages)?
4. Which author has the highest average rating, considering only books with at least 50 ratings?
5. What is the behavior of the most active users (with more than 50 ratings) regarding text reviews?

## Methodology
- **Data Extraction:** Established a connection to the PostgreSQL database using `SQLAlchemy` and explored the tables (`books`, `authors`, `publishers`, `ratings`, `reviews`).
- **SQL Queries:** Formulated specific queries to answer each question, using aggregations, joins, subqueries, and filters (e.g., `LEFT JOIN` to preserve catalog, `COALESCE` for null values, and conditions like `HAVING COUNT(rating_id) >= 50` to ensure statistical robustness).
- **Analysis and Visualization:** Results were presented as Pandas DataFrames and a horizontal bar chart with embedded labels was generated to clearly communicate the top books by reviews and rating.
- **Results Interpretation:** Each finding was linked to a business conclusion, guiding future strategic decisions.

## Conclusions and Recommendations
### Key Findings:
- **Modern catalog:** 819 books published after 2000, indicating an up-to-date offering attractive to contemporary readers.
- **Engagement:** Sagas like *Harry Potter* and *Twilight* lead in number of reviews, but *Harry Potter* maintains a higher rating (4.41 vs 3.66), suggesting that sustained quality generates greater loyalty.
- **Key publisher:** *Penguin Books* is the publisher with the most titles over 50 pages (42 books), positioning itself as the ideal business partner to ensure inventory volume.
- **Notable author:** *J.K. Rowling* has the highest average rating (4.29) among books with at least 50 ratings, confirming the value of established authors.
- **Influential users:** Readers who rate more than 50 books write an average of 24.3 text reviews, identifying a segment of "super-users" who generate valuable content for the community.

### Strategic Recommendations:
1. **Saga-based curation:** Implement a recommendation system that highlights complete collections (like Harry Potter) to capitalize on interest in fantasy series.
2. **"Expert Readers" Program:** Create a reward system (badges, levels, early access) for highly active users, encouraging the generation of reviews that help other readers.
3. **Priority publishing partnership:** Establish content agreements with *Penguin Books* to ensure a broad and quality catalog.
4. **Focus on modern books:** Maintain curation centered on publications after the year 2000, aligned with current tastes.

## Data Dictionary
- **books:** Information for each book (`book_id`, `author_id`, `title`, `num_pages`, `publication_date`, `publisher_id`).
- **authors:** Author identification and name (`author_id`, `author`).
- **publishers:** Publisher identification and name (`publisher_id`, `publisher`).
- **ratings:** User ratings (`rating_id`, `book_id`, `username`, `rating`).
- **reviews:** User text reviews (`review_id`, `book_id`, `username`, `text`).

## Interactive Visualization
You can explore the results of this analysis in the following Tableau Public dashboard:

[**View Dashboard: Top 10 Books**](https://public.tableau.com/app/profile/ari.de.le.n/viz/Top10Books_17737109047610/Dashboard1?publish=yes)
