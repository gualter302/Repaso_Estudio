# Semana 4: Programación Orientada a Objetos (POO)

## Plan de la semana

| Día | Tarea |
|---|---|
| Lunes | Clases y objetos. Ejercicio 1 |
| Martes | Encapsulamiento. Ejercicio 2 |
| Miércoles | Herencia y polimorfismo. Ejercicios 3–4 |
| Jueves | Proyecto Biblioteca: diseño (en papel) y clases |
| Viernes | Proyecto Biblioteca: menú y pruebas + checklist de cierre |

## Conceptos

- **Clase:** el molde. **Objeto:** una cosa concreta hecha con ese molde.
- **Atributos** (datos) y **métodos** (acciones)
- `__init__`: el constructor; `self`: el propio objeto
- **Encapsulamiento:** proteger los datos internos (`_saldo`) y modificarlos solo mediante métodos que validan
- **Herencia:** `class Perro(Animal):` reutiliza y extiende una clase
- **Polimorfismo:** distintas clases con el mismo método (`hablar()`), cada una a su manera
- **Abstracción / interfaces:** definir *qué* debe hacer algo sin decir *cómo* (`from abc import ABC, abstractmethod`)
- `__str__`: cómo se ve el objeto al imprimirlo

### Los 4 pilares, en una frase cada uno

| Pilar | Idea |
|---|---|
| Encapsulamiento | Nadie toca mis datos sin pasar por mis reglas |
| Herencia | No repito código: lo heredo y lo extiendo |
| Polimorfismo | Mismo mensaje, distinta respuesta según el objeto |
| Abstracción | Muestro qué hace, escondo cómo lo hace |

### Autoevaluación

1. ¿Qué diferencia hay entre una clase y un objeto? Da un ejemplo de la vida real.
2. ¿Para qué sirve `self`?
3. ¿Por qué no conviene que cualquiera modifique `cuenta.saldo` directamente?
4. Explica el polimorfismo sin usar la palabra "polimorfismo".

## Ejercicios

**Ej 1 ⭐ Clase Estudiante:** atributos nombre, carrera y lista de notas. Métodos `agregar_nota(n)`, `promedio()` y `__str__`. Crea 3 estudiantes.

**Ej 2 ⭐⭐ Cuenta bancaria:** clase `CuentaBancaria` con `_saldo` protegido. Métodos `depositar`, `retirar` (que no permita dejar saldo negativo) y `consultar_saldo`.

**Ej 3 ⭐⭐ Herencia:** clase `Empleado` (nombre, sueldo base) y dos hijas, `EmpleadoTiempoCompleto` y `EmpleadoPorHoras`, cada una con su propio `calcular_pago()`. Recorre una lista mezclada de empleados llamando a `calcular_pago()` en todos (eso es polimorfismo).

**Ej 4 ⭐⭐ Abstracción:** clase abstracta `Figura` con el método abstracto `area()`. Clases hijas `Circulo`, `Rectangulo` y `Triangulo`.

## Proyecto de la fase: Biblioteca ⭐⭐⭐

App de consola con menú. Antes de programar, **dibuja en papel** las clases, sus atributos y métodos (es un diagrama de clases UML sencillo). Súbelo como foto a esta carpeta.

**Clases mínimas:**
- `Libro`: código, título, autor, disponible (bool)
- `Socio`: cédula, nombre, lista de libros prestados (máximo 3)
- `Biblioteca`: lista de libros y de socios, con los métodos `registrar_libro`, `registrar_socio`, `prestar(codigo, cedula)`, `devolver(codigo, cedula)`, `listar_disponibles`

**Reglas:**
- No se puede prestar un libro ya prestado
- Un socio no puede tener más de 3 libros a la vez
- Mostrar mensajes claros cuando algo no se puede hacer

**Extra opcional:** guardar y cargar los datos en un archivo `.json` para que no se pierdan al cerrar.

## Checklist de cierre de la fase 1

- [ ] Puedo explicar los 4 pilares de la POO con ejemplos propios
- [ ] Hice el diagrama de clases antes de programar la Biblioteca
- [ ] La Biblioteca funciona y respeta las reglas
- [ ] Puedo explicar **cada línea** del proyecto
- [ ] Le pedí a la IA que me haga 10 preguntas sobre mi código y las respondí
- [ ] Marqué la fase 1 como completada en el README principal 🎉
