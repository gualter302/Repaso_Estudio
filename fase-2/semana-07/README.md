# Semana 7: Modelado, normalización, llaves e índices

> Esta semana diseñas **la base de datos real** del proyecto final.

## Plan de la semana

| Día | Tarea |
|---|---|
| Lunes | Conceptos de modelado E-R. Ejercicio 1 |
| Martes | Normalización. Ejercicio 2 |
| Miércoles | Diseñar el E-R del sistema de agua potable |
| Jueves | Escribir `agua_potable.sql` |
| Viernes | Datos de prueba, índices y checklist de cierre |

## Conceptos

- **Entidad, atributo, relación**
- **Cardinalidad:** 1 a 1, 1 a muchos (1:N), muchos a muchos (N:M)
- Una relación **N:M** siempre se resuelve con una **tabla intermedia**
- **Normalización:**
  - **1FN:** cada celda guarda un solo valor (nada de `"0991234567, 0987654321"`)
  - **2FN:** todo depende de la llave completa
  - **3FN:** ningún atributo depende de otro que no sea llave
- **Restricciones:** `PRIMARY KEY`, `FOREIGN KEY`, `UNIQUE`, `NOT NULL`, `CHECK`
- `ON DELETE CASCADE` / `RESTRICT`: qué pasa con los hijos cuando se borra el padre
- **Índices:** aceleran las búsquedas pero hacen más lentas las escrituras. Úsalos en columnas por las que buscas mucho.

### Autoevaluación

1. Un estudiante toma muchas materias y una materia tiene muchos estudiantes. ¿Cuántas tablas necesitas?
2. ¿Por qué guardar `total_a_pagar` en una tabla puede ser una mala idea? ¿Cuándo sí tiene sentido?
3. ¿Cuándo conviene `RESTRICT` en vez de `CASCADE`?

## Ejercicios

**Ej 1 ⭐⭐ E-R de práctica:** diseña el E-R de tu Biblioteca de la fase 1 (libros, autores, socios, préstamos). Ojo: un libro puede tener varios autores.

**Ej 2 ⭐⭐ Normalizar:** esta tabla está mal diseñada. Llévala a 3FN y explica cada paso en `normalizacion.md`:

| factura | cedula | nombre | sector | telefonos | mes | consumo | tarifa_sector |
|---|---|---|---|---|---|---|---|
| 001 | 0912345678 | Ana | Centro | 0991..., 0987... | 2026-01 | 18 | 0.45 |

## Proyecto de la fase: base de datos del sistema de agua potable ⭐⭐⭐

**Requisitos (piensa en cómo funciona una junta de agua real):**
- Abonados (cédula, nombre, dirección, teléfonos, sector)
- Sectores con su tarifa
- Medidores asignados a abonados (un abonado puede tener más de un medidor)
- Lecturas mensuales por medidor
- Facturas generadas a partir de las lecturas, con estado: pendiente o pagada
- Pagos (fecha, monto, factura)
- Usuarios del sistema (administrador, lector, cajero)

**Entregables en esta carpeta:**
- [ ] `diagrama_er.png`: el diagrama E-R
- [ ] `agua_potable.sql`: el `CREATE TABLE` de todas las tablas con sus restricciones
- [ ] `datos_prueba.sql`: al menos 15 abonados, 3 sectores y 3 meses de lecturas
- [ ] `consultas.sql`: al menos 5 consultas útiles (morosos, consumo por sector, recaudación del mes, ...)
- [ ] Al menos 2 índices justificados con un comentario

## Checklist de cierre

- [ ] Puedo explicar 1FN, 2FN y 3FN con mis propios ejemplos
- [ ] Sé resolver una relación N:M
- [ ] La base del agua potable está creada y con datos
- [ ] Puedo justificar cada tabla y cada relación
- [ ] Anoté la semana en la bitácora
