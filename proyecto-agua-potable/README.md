# Fase 3: Proyecto Sistema de Agua Potable v2 (semanas 9–12)

> Meta: reconstruir el proyecto de vinculación **entendiendo cada línea**. Lo importante no es que tenga muchas funciones, sino que lo puedas explicar en una entrevista.

## Tecnologías

| Capa | Tecnología | Por qué |
|---|---|---|
| Frontend | HTML + CSS + JavaScript (sin frameworks) | Primero entender la base; los frameworks vienen después |
| Backend | Python + [Flask](https://flask.palletsprojects.com/) | Mismo lenguaje de la fase 1, simple y sin "magia" |
| Base de datos | PostgreSQL | La que diseñaste en la semana 7 |
| Conexión a BD | `psycopg` con SQL escrito a mano | Para que veas el SQL de verdad; un ORM puede venir más adelante |

## Reglas de esta fase

1. **Rama por funcionalidad:** `feature/registro-abonados`, `feature/lecturas`, ... y un Pull Request por cada una.
2. **La IA puede ayudarte a revisar, no a construir.** Escribes tú y después le pides que revise o que te pregunte.
3. Cada semana termina con algo que **funciona**, aunque sea feo.
4. Nada de contraseñas en el código: van en un archivo `.env` (ya está en el `.gitignore`).

## Estructura sugerida

```
proyecto-agua-potable/
├── README.md            # esta guía + al final, cómo instalar y usar tu sistema
├── backend/
│   ├── app.py           # servidor Flask
│   ├── db.py            # conexión a PostgreSQL
│   ├── requirements.txt
│   └── .env.example     # ejemplo de variables (sin datos reales)
├── frontend/
│   ├── index.html
│   ├── abonados.html
│   ├── css/estilos.css
│   └── js/
└── database/
    └── (copia aquí agua_potable.sql de la semana 7)
```

---

## Semana 9: HTML y CSS

**Conceptos:** estructura de un documento HTML, etiquetas semánticas (`header`, `nav`, `main`, `section`, `footer`), formularios (`form`, `input`, `label`, `select`), tablas, selectores CSS, modelo de caja, Flexbox, diseño responsive básico.

**Recursos:** [MDN: HTML](https://developer.mozilla.org/es/docs/Learn/HTML) · [MDN: CSS](https://developer.mozilla.org/es/docs/Learn/CSS) · [Flexbox Froggy](https://flexboxfroggy.com/#es)

**Tareas:**
- [ ] Dibujar en papel (o en Figma) las pantallas: inicio, abonados, lecturas, facturas
- [ ] `index.html` con menú de navegación
- [ ] `abonados.html`: formulario de registro + tabla de abonados (con datos escritos a mano por ahora)
- [ ] `lecturas.html`: formulario para registrar una lectura
- [ ] Hoja de estilos común que se vea bien también en el celular
- [ ] Terminar Flexbox Froggy

---

## Semana 10: JavaScript

**Conceptos:** variables (`let`, `const`), funciones, arreglos y objetos (muy parecidos a las listas y diccionarios de Python), el DOM (`document.querySelector`), eventos (`addEventListener`), validación de formularios, `fetch` y promesas (`async`/`await`).

**Recursos:** [MDN: JavaScript](https://developer.mozilla.org/es/docs/Learn/JavaScript) · [javascript.info (en español)](https://es.javascript.info/)

**Tareas:**
- [ ] Validar el formulario de abonados: cédula de 10 dígitos, campos obligatorios
- [ ] ⭐⭐⭐ Validar la cédula ecuatoriana con el algoritmo del dígito verificador (búscalo y entiéndelo antes de programarlo)
- [ ] Agregar abonados a la tabla con JavaScript, sin recargar la página
- [ ] Filtro de búsqueda en la tabla
- [ ] Calcular en pantalla el consumo y el valor a pagar al registrar una lectura (reutiliza la lógica de la tarifa por rangos)

---

## Semana 11: Backend con Flask + PostgreSQL

**Conceptos:** qué es un servidor web, rutas, recibir y devolver JSON, entorno virtual (`python -m venv venv`), variables de entorno, conexión a la base de datos, **consultas parametrizadas** (para evitar inyección SQL), CORS.

**Recursos:** [Quickstart de Flask](https://flask.palletsprojects.com/en/stable/quickstart/) · [Documentación de psycopg](https://www.psycopg.org/psycopg3/docs/)

**Tareas** (usa la tabla de rutas que diseñaste en la semana 8):
- [ ] Crear el entorno virtual e instalar `flask`, `psycopg[binary]` y `python-dotenv`
- [ ] `GET /abonados` y `POST /abonados`
- [ ] `GET /abonados/<id>` y `PUT /abonados/<id>`
- [ ] `POST /lecturas`
- [ ] Conectar el frontend con `fetch`: la tabla de abonados ya sale de la base de datos real
- [ ] Devolver códigos HTTP correctos (`201`, `400`, `404`)
- [ ] Explicar en un comentario qué es la inyección SQL y cómo la evitas

---

## Semana 12: Facturación, pulido y documentación

**Tareas:**
- [ ] `POST /facturas/generar`: genera las facturas del mes a partir de las lecturas
- [ ] `POST /pagos`: registra un pago y marca la factura como pagada
- [ ] Pantalla de facturas pendientes (morosos)
- [ ] Manejo de errores: mensajes claros en pantalla si algo falla
- [ ] Completar la sección "Cómo instalar y usar" de este README
- [ ] Capturas de pantalla del sistema funcionando

**Opcional (si te sobra tiempo):** login con roles (administrador, lector, cajero), exportar facturas a PDF, reporte de recaudación por sector.

---

## Checklist final del trayecto

- [ ] El sistema funciona de punta a punta: registrar abonado → lectura → factura → pago
- [ ] Puedo explicar qué pasa desde que hago clic en "Guardar" hasta que el dato queda en la base de datos
- [ ] Puedo explicar cada archivo y cada función
- [ ] Le pedí a la IA una **entrevista técnica simulada** sobre este proyecto y la pasé
- [ ] El README explica cómo instalarlo
- [ ] Marqué la fase 3 como completada en el README principal 🎉🎉

---

## Cómo instalar y usar

_(Complétalo tú en la semana 12.)_
