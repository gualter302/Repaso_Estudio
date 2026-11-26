# Semana 1: Variables, tipos, operadores y entrada/salida

## Plan de la semana

| Día | Tarea |
|---|---|
| Lunes | Instalar Python y VS Code. Leer los conceptos. Ejercicios 1–2 |
| Martes | Ejercicios 3–4 |
| Miércoles | Ejercicios 5–6 |
| Jueves | Ejercicio 7 |
| Viernes | Reto (ejercicio 8) + checklist de cierre |

## Conceptos

- **Variable:** un nombre que guarda un valor. `edad = 22`
- **Tipos básicos:** `int` (entero), `float` (decimal), `str` (texto), `bool` (verdadero/falso)
- **Conversión de tipos:** `int("5")`, `float("3.2")`, `str(10)`
- **Operadores aritméticos:** `+ - * / // % **`
- **Operadores de comparación:** `== != < > <= >=`
- **Operadores lógicos:** `and or not`
- **Entrada y salida:** `input()` **siempre devuelve texto**; `print()` muestra en pantalla
- **f-strings:** `print(f"Hola {nombre}, tienes {edad} años")`

### Autoevaluación (responde sin buscar)

1. ¿Qué diferencia hay entre `/` y `//`? ¿Y qué hace `%`?
2. ¿Por qué `input("Edad: ") + 1` da error?
3. ¿Qué imprime `print(7 % 3)`? ¿Y `print(2 ** 3)`?
4. ¿Qué tipo de dato es `"25"`? ¿Y `25.0`?

## Ejercicios

**Ej 1 ⭐ Saludo:** pide nombre y edad, y muestra: `Hola Oscar, el próximo año tendrás 23 años.`

**Ej 2 ⭐ Conversor de temperatura:** pide grados Celsius y muestra Fahrenheit (`F = C * 9/5 + 32`).

**Ej 3 ⭐ Área y perímetro:** pide base y altura de un rectángulo y muestra área y perímetro.

**Ej 4 ⭐⭐ Segundos a tiempo:** pide una cantidad de segundos (ej. `3725`) y muestra `1 h 2 min 5 s`. *Pista: `//` y `%`.*

**Ej 5 ⭐⭐ Cuenta de la cena:** pide el total, el porcentaje de propina y el número de personas. Muestra cuánto paga cada uno con 2 decimales (`f"{valor:.2f}"`).

**Ej 6 ⭐⭐ Consumo de agua:** pide la lectura anterior y la actual de un medidor (en m³) y el precio por m³. Muestra el consumo y el valor a pagar. *(Te va a servir para la fase 3.)*

**Ej 7 ⭐⭐ Tabla de verdad:** declara `a = True` y `b = False` e imprime el resultado de `a and b`, `a or b`, `not a` y `not (a and b)`. Antes de ejecutar, **escribe en un comentario** lo que crees que va a salir.

**Ej 8 ⭐⭐⭐ Reto: dígitos:** pide un número de 3 cifras (ej. `472`) y muestra la suma de sus dígitos (`13`) **sin convertirlo a texto**. Solo con `//` y `%`.

## Checklist de cierre

- [ ] Puedo explicar qué es una variable y los 4 tipos básicos
- [ ] Sé por qué hay que convertir lo que devuelve `input()`
- [ ] Entiendo `//` y `%` y sé cuándo usarlos
- [ ] Resolví al menos 6 de los 8 ejercicios **sin que la IA escriba código**
- [ ] Probé al menos un ejercicio en [Python Tutor](https://pythontutor.com/)
- [ ] Anoté la semana en la bitácora del README principal
