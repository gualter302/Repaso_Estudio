# Semana 2: Condicionales, bucles y funciones

## Plan de la semana

| Día | Tarea |
|---|---|
| Lunes | Conceptos de condicionales. Ejercicios 1–2 |
| Martes | Conceptos de bucles. Ejercicios 3–4 |
| Miércoles | Conceptos de funciones. Ejercicio 5 |
| Jueves | Ejercicios 6–7 |
| Viernes | Reto (ejercicio 8) + checklist de cierre |

## Conceptos

### Condicionales
- `if`, `elif`, `else`
- Condiciones combinadas con `and`, `or`, `not`
- **La indentación importa:** define qué código pertenece a cada bloque

### Bucles
- `while condición:` repite **mientras** la condición se cumpla (cuidado con los bucles infinitos)
- `for i in range(inicio, fin, paso):` repite un número conocido de veces
- `break` sale del bucle; `continue` salta a la siguiente vuelta
- **Acumulador** (`suma += x`) y **contador** (`contador += 1`): los dos patrones más usados

### Funciones
- `def nombre(parametros):` + `return`
- Diferencia entre **parámetro** (en la definición) y **argumento** (en la llamada)
- **Alcance (scope):** una variable creada dentro de una función no existe afuera
- Diferencia entre `print` y `return`. **Muy importante.**

### Autoevaluación

1. ¿Cuándo conviene `while` y cuándo `for`?
2. ¿Qué imprime `for i in range(1, 10, 3): print(i)`?
3. Si una función hace `print(x)` pero no `return`, ¿qué devuelve?
4. ¿Por qué una función es mejor que copiar y pegar el mismo código?

## Ejercicios

**Ej 1 ⭐ Par o impar:** pide un número y di si es par o impar.

**Ej 2 ⭐⭐ Calificación:** pide una nota del 0 al 10. Muestra "Excelente" (9–10), "Bueno" (7–8.9), "Regular" (5–6.9) o "Reprobado" (<5). Si la nota está fuera de rango, muestra un error.

**Ej 3 ⭐ Tabla de multiplicar:** pide un número y muestra su tabla del 1 al 12 con `for`.

**Ej 4 ⭐⭐ Validar entrada:** pide una contraseña hasta que el usuario escriba `"python123"`, con un máximo de 3 intentos. Usa `while`.

**Ej 5 ⭐⭐ Funciones básicas:** crea `es_primo(n)`, `factorial(n)` y `maximo(a, b, c)`. Las tres deben **retornar** el resultado, no imprimirlo. Pruébalas desde fuera de la función.

**Ej 6 ⭐⭐ Menú de calculadora:** muestra un menú repetido (1. Sumar, 2. Restar, 3. Multiplicar, 4. Dividir, 0. Salir). Cada operación va en su propia función. Controla la división entre cero.

**Ej 7 ⭐⭐ Tarifa de agua por rangos:** crea `calcular_pago(consumo_m3)` con estas tarifas:
- 0–15 m³: $0.30 por m³
- 16–30 m³: $0.45 por m³
- más de 30 m³: $0.70 por m³
- más un cargo fijo de $2.00

**Ej 8 ⭐⭐⭐ Reto: adivina el número:** el programa elige un número al azar del 1 al 100 (`import random`, `random.randint(1, 100)`). El usuario adivina y el programa responde "mayor" o "menor". Al final muestra en cuántos intentos lo logró. Sepáralo en al menos 2 funciones.

## Checklist de cierre

- [ ] Sé elegir entre `if/elif/else`, `while` y `for`
- [ ] Entiendo la diferencia entre `print` y `return`
- [ ] Sé qué es el alcance (scope) de una variable
- [ ] Puedo escribir un acumulador y un contador sin mirar
- [ ] Resolví al menos 6 de los 8 ejercicios sin que la IA escriba código
- [ ] Anoté la semana en la bitácora
