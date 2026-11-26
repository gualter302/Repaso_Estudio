# Fase 2: Bases de datos y fundamentos del oficio (semanas 5–8)

> Meta de la fase: diseñar una base de datos desde cero a partir de un problema real, consultarla con SQL sin ayuda y usar Git como lo usa un equipo.

## Herramientas

- **PostgreSQL:** [postgresql.org/download](https://www.postgresql.org/download/)
- **Cliente gráfico:** pgAdmin (viene con PostgreSQL) o [DBeaver](https://dbeaver.io/) (gratis)
- **Git:** [git-scm.com](https://git-scm.com/) (ya lo usas para este repo)
- **Diagramas E-R:** [draw.io](https://app.diagrams.net/) o [dbdiagram.io](https://dbdiagram.io/)

> Si en tu carrera usan MySQL o SQL Server, el SQL de esta fase es casi igual.

## Reglas de esta fase

1. Cada consulta va en un archivo `.sql` con un comentario arriba que diga qué pregunta responde.
2. **Escribe la consulta tú.** Si no sale, pídele a la IA que te explique el error, no que la reescriba.
3. Antes de ejecutar, **predice** cuántas filas va a devolver.

## Semanas

| Semana | Tema | Carpeta |
|---|---|---|
| 5 | SQL básico: SELECT, WHERE, INSERT, UPDATE, DELETE | [semana-05](semana-05/) |
| 6 | JOINs, GROUP BY, agregaciones, subconsultas | [semana-06](semana-06/) |
| 7 | Modelado E-R, normalización, llaves, índices | [semana-07](semana-07/) |
| 8 | Git en serio + cómo funciona la web (HTTP, APIs) | [semana-08](semana-08/) |

## Recursos de la fase

- [SQLBolt](https://sqlbolt.com/): lecciones interactivas de SQL (empieza aquí)
- [Tutorial de PostgreSQL (documentación oficial)](https://www.postgresql.org/docs/current/tutorial.html)
- [Learn Git Branching](https://learngitbranching.js.org/?locale=es_ES): Git visual e interactivo, en español
- [MDN: ¿Cómo funciona la web?](https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/How_the_Web_works)

## Entregable final de la fase

En `semana-07/`: el **diagrama E-R** y el **script SQL completo** (`agua_potable.sql`) de la base de datos del sistema de agua potable, con datos de prueba. Es la base de la fase 3.
