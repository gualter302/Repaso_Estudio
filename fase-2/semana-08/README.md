# Semana 8: Git en serio y cómo funciona la web

## Plan de la semana

| Día | Tarea |
|---|---|
| Lunes | Learn Git Branching: sección "Introducción" completa |
| Martes | Ejercicios de Git 1–3 en este repo |
| Miércoles | Ejercicio de Git 4 (conflicto) + Learn Git Branching "Remotos" |
| Jueves | Cómo funciona la web: conceptos y ejercicios 5–6 |
| Viernes | Ejercicio 7 + checklist de cierre de la fase 2 |

## Conceptos de Git

- **Repositorio, commit, staging area** (`git add`)
- **Commits con sentido:** un cambio lógico por commit, con un mensaje claro (`"Agrega validación de cédula"`, no `"cambios"`)
- **Ramas:** `git switch -c nueva-rama`, `git merge`
- **Remoto:** `git push`, `git pull`, `git fetch`
- **Conflictos:** qué son y cómo resolverlos a mano
- **Pull Request:** proponer cambios para que se revisen antes de unirlos a `main`
- `.gitignore`: qué **no** subir (contraseñas, `node_modules`, `__pycache__`, `.env`)

## Conceptos de la web

- **Cliente y servidor:** quién pide y quién responde
- **HTTP:** petición (método + URL + headers + cuerpo) y respuesta (código + headers + cuerpo)
- **Métodos:** `GET` (leer), `POST` (crear), `PUT`/`PATCH` (actualizar), `DELETE` (borrar)
- **Códigos de estado:** `200` ok, `201` creado, `400` petición mal hecha, `401` sin autenticar, `404` no existe, `500` error del servidor
- **API REST:** un servidor que responde datos (normalmente JSON) en vez de páginas
- **JSON:** se parece mucho a los diccionarios de Python
- **DNS**, **dominio**, **puerto**: lo básico

### Autoevaluación

1. ¿Qué diferencia hay entre `git fetch` y `git pull`?
2. ¿Por qué nunca se sube un archivo `.env` con contraseñas?
3. ¿Qué método HTTP usarías para registrar un nuevo abonado? ¿Y para consultar sus facturas?
4. Si una página muestra el error 404, ¿de quién es la culpa: del cliente o del servidor?

## Ejercicios

**Git 1 ⭐:** crea la rama `practica-git`, agrega un archivo `notas_git.md` con los comandos que aprendiste, haz 3 commits y súbela.

**Git 2 ⭐⭐:** abre un Pull Request desde `practica-git` hacia `main` en GitHub, revísalo y únelo (merge).

**Git 3 ⭐:** crea un `.gitignore` en la raíz del repo para Python (`__pycache__/`, `.env`, `venv/`).

**Git 4 ⭐⭐⭐ Conflicto a propósito:** crea dos ramas que modifiquen **la misma línea** de un archivo. Únelas, provoca el conflicto y resuélvelo a mano. Explica en `notas_git.md` qué significan `<<<<<<<`, `=======` y `>>>>>>>`.

**Web 5 ⭐:** abre las herramientas de desarrollador de tu navegador (F12 → pestaña Red/Network), entra a cualquier página y anota en `notas_web.md` 3 peticiones que veas: método, URL y código de respuesta.

**Web 6 ⭐⭐:** abre en el navegador `https://api.github.com/users/gualter302`. Es una API real que responde JSON. Identifica 5 campos y explica qué significan.

**Web 7 ⭐⭐ Diseña tu API:** en `api_agua_potable.md`, escribe en una tabla las rutas que tendría tu sistema (sin programar nada todavía):

| Método | Ruta | Qué hace |
|---|---|---|
| GET | /abonados | Lista los abonados |
| POST | /abonados | Registra un abonado |
| ... | ... | ... |

## Checklist de cierre de la fase 2

- [ ] Trabajo con ramas y Pull Requests sin miedo
- [ ] Resolví un conflicto de Git a mano
- [ ] Puedo explicar qué pasa desde que escribo una URL hasta que veo la página
- [ ] Conozco los métodos HTTP y los códigos de estado principales
- [ ] Diseñé las rutas de la API del agua potable
- [ ] Marqué la fase 2 como completada en el README principal 🎉
