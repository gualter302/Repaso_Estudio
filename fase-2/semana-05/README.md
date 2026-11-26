# Semana 5: SQL básico

## Plan de la semana

| Día | Tarea |
|---|---|
| Lunes | Instalar PostgreSQL + pgAdmin o DBeaver. SQLBolt, lecciones 1–4 |
| Martes | SQLBolt 5–6. Crear la base `practica` y la tabla de abajo |
| Miércoles | Ejercicios 1–5 (SELECT) |
| Jueves | Ejercicios 6–9 (INSERT, UPDATE, DELETE) |
| Viernes | Reto + checklist de cierre |

## Conceptos

- **Base de datos, tabla, fila (registro) y columna (campo)**
- **Tipos de datos:** `INTEGER`, `SERIAL`, `VARCHAR(n)`, `TEXT`, `NUMERIC(10,2)`, `DATE`, `BOOLEAN`
- `CREATE TABLE`, `DROP TABLE`
- `SELECT ... FROM ... WHERE ... ORDER BY ... LIMIT`
- Operadores: `=`, `<>`, `>`, `BETWEEN`, `IN`, `LIKE`, `IS NULL`
- `INSERT INTO`, `UPDATE ... SET ... WHERE`, `DELETE FROM ... WHERE`
- ⚠️ **Un `UPDATE` o `DELETE` sin `WHERE` afecta a TODA la tabla**

### Autoevaluación

1. ¿Qué diferencia hay entre `VARCHAR(50)` y `TEXT`?
2. ¿Por qué `WHERE nombre = NULL` no funciona? ¿Qué se usa en su lugar?
3. ¿Qué hace `LIKE 'A%'`?

## Preparación

Crea esta tabla en una base llamada `practica`:

```sql
CREATE TABLE abonados (
    id          SERIAL PRIMARY KEY,
    cedula      VARCHAR(10) NOT NULL UNIQUE,
    nombre      VARCHAR(100) NOT NULL,
    sector      VARCHAR(50),
    fecha_alta  DATE NOT NULL,
    activo      BOOLEAN DEFAULT TRUE
);
```

Inserta **tú** al menos 10 abonados con datos inventados, en 3 sectores distintos, y deja al menos 2 inactivos.

## Ejercicios

Guarda cada consulta en `ej01.sql`, `ej02.sql`, ...

1. ⭐ Mostrar todos los abonados.
2. ⭐ Mostrar solo nombre y sector, ordenados alfabéticamente por nombre.
3. ⭐ Abonados del sector que elijas.
4. ⭐⭐ Abonados activos dados de alta en 2024 o después.
5. ⭐⭐ Abonados cuyo nombre empiece con "M" o cuyo sector esté vacío (`NULL`).
6. ⭐ Insertar 2 abonados nuevos.
7. ⭐⭐ Cambiar de sector a un abonado, buscándolo por su cédula.
8. ⭐⭐ Desactivar (`activo = FALSE`) a todos los abonados de un sector.
9. ⭐⭐ Eliminar un abonado por su id. **Antes**, haz un `SELECT` con el mismo `WHERE` para comprobar qué vas a borrar.

**Reto ⭐⭐⭐:** intenta insertar un abonado con una cédula repetida. ¿Qué error da y por qué? Explícalo en un comentario dentro de `reto.sql`.

## Checklist de cierre

- [ ] PostgreSQL instalado y funcionando
- [ ] Terminé SQLBolt, lecciones 1–6
- [ ] Escribo `SELECT` con filtros y orden sin buscar la sintaxis
- [ ] Siempre pruebo con `SELECT` antes de un `UPDATE` o `DELETE`
- [ ] Anoté la semana en la bitácora
