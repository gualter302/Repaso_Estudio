# Semana 6: JOINs, agregaciones y subconsultas

## Plan de la semana

| Día | Tarea |
|---|---|
| Lunes | Llaves foráneas. Crear las tablas nuevas. SQLBolt 6–7 |
| Martes | JOINs: ejercicios 1–3 |
| Miércoles | GROUP BY y agregaciones: ejercicios 4–6 |
| Jueves | Subconsultas: ejercicios 7–8 |
| Viernes | Reto + checklist de cierre |

## Conceptos

- **Llave primaria (PK)** y **llave foránea (FK):** cómo se relacionan dos tablas
- `INNER JOIN`: solo las filas que coinciden en ambas tablas
- `LEFT JOIN`: todas las de la izquierda, coincidan o no
- **Funciones de agregación:** `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`
- `GROUP BY` agrupa; `HAVING` filtra **grupos** (`WHERE` filtra **filas**)
- **Subconsultas:** una consulta dentro de otra
- **Orden lógico de ejecución:** `FROM → JOIN → WHERE → GROUP BY → HAVING → SELECT → ORDER BY`

### Autoevaluación

1. ¿Qué diferencia hay entre `INNER JOIN` y `LEFT JOIN`? Dibuja un ejemplo.
2. ¿Por qué no puedes usar `WHERE COUNT(*) > 2`?
3. ¿Qué pasa si haces `GROUP BY sector` pero en el `SELECT` pones `nombre`?

## Preparación

Sobre tu base `practica`, agrega:

```sql
CREATE TABLE medidores (
    id           SERIAL PRIMARY KEY,
    numero_serie VARCHAR(20) NOT NULL UNIQUE,
    abonado_id   INTEGER NOT NULL REFERENCES abonados(id)
);

CREATE TABLE lecturas (
    id           SERIAL PRIMARY KEY,
    medidor_id   INTEGER NOT NULL REFERENCES medidores(id),
    fecha        DATE NOT NULL,
    lectura_m3   NUMERIC(10,2) NOT NULL
);
```

Inserta medidores (deja a un abonado **sin** medidor) y lecturas de 3 meses para cada medidor.

## Ejercicios

1. ⭐ Nombre del abonado junto al número de serie de su medidor (`INNER JOIN`).
2. ⭐⭐ Todos los abonados, tengan o no medidor (`LEFT JOIN`). ¿Cuál sale con `NULL`?
3. ⭐⭐ Todas las lecturas con el nombre del abonado (dos JOINs).
4. ⭐ Cuántos abonados hay por sector.
5. ⭐⭐ Lectura promedio por medidor.
6. ⭐⭐ Sectores con más de 3 abonados (`HAVING`).
7. ⭐⭐ Abonados que **no** tienen medidor, usando una subconsulta con `NOT IN`.
8. ⭐⭐⭐ La lectura más reciente de cada medidor.

**Reto ⭐⭐⭐:** el consumo de un mes es la lectura del mes menos la del mes anterior. Calcula el consumo de cada medidor en el último mes. *(Pista: investiga `LAG()` o resuélvelo con un JOIN de la tabla consigo misma.)*

## Checklist de cierre

- [ ] Explico la diferencia entre `INNER` y `LEFT JOIN` con un dibujo
- [ ] Sé cuándo usar `WHERE` y cuándo `HAVING`
- [ ] Escribí al menos una subconsulta funcional
- [ ] Me sé el orden lógico de ejecución de una consulta
- [ ] Anoté la semana en la bitácora
