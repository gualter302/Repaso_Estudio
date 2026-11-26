# Semana 3: Listas, cadenas, diccionarios, recursión y algoritmos

## Plan de la semana

| Día | Tarea |
|---|---|
| Lunes | Listas. Ejercicios 1–2 |
| Martes | Cadenas y diccionarios. Ejercicios 3–4 |
| Miércoles | Recursión. Ejercicio 5 |
| Jueves | Búsqueda y ordenamiento. Ejercicios 6–7 |
| Viernes | Reto (ejercicio 8) + checklist de cierre |

## Conceptos

### Listas
- Crear, acceder por índice (`lista[0]`, `lista[-1]`), cortes (`lista[1:3]`)
- `append`, `insert`, `remove`, `pop`, `len`, `in`
- Recorrer con `for x in lista` y con `for i in range(len(lista))`
- **Listas de listas** (matrices)

### Cadenas (strings)
- Se recorren igual que una lista
- `upper`, `lower`, `strip`, `split`, `join`, `replace`, `count`
- Son **inmutables**: no puedes cambiar un carácter directamente

### Diccionarios
- Pares clave → valor: `usuario = {"nombre": "Ana", "consumo": 12}`
- Acceder, agregar, recorrer con `.items()`
- Son la base de cómo se ve un registro de base de datos (útil para la fase 2)

### Recursión
- Una función que se llama a sí misma
- Necesita un **caso base** (cuándo parar) y un **caso recursivo** (acercarse al caso base)
- Sin caso base → `RecursionError`

### Algoritmos
- **Búsqueda lineal:** revisar uno por uno
- **Búsqueda binaria:** en una lista ordenada, partir a la mitad cada vez
- **Ordenamiento burbuja:** comparar vecinos e intercambiar
- **Complejidad (idea básica):** ¿cuántos pasos más hace mi algoritmo si los datos se duplican?

### Autoevaluación

1. ¿Qué devuelve `"hola mundo".split()`?
2. ¿Cuál es el caso base de `factorial(n)`?
3. ¿Por qué la búsqueda binaria necesita una lista ordenada?
4. ¿Cuándo usarías una lista y cuándo un diccionario?

## Ejercicios

**Ej 1 ⭐ Estadísticas:** pide 5 números, guárdalos en una lista y muestra suma, promedio, mayor y menor **sin usar** `sum`, `max` ni `min`.

**Ej 2 ⭐⭐ Sin repetidos:** dada una lista con elementos repetidos, crea una nueva lista sin repetidos, manteniendo el orden.

**Ej 3 ⭐⭐ Palíndromo:** función que diga si una frase es palíndromo, ignorando espacios y mayúsculas (`"Anita lava la tina"` → `True`).

**Ej 4 ⭐⭐ Contador de palabras:** pide un texto y muestra cuántas veces aparece cada palabra, usando un diccionario.

**Ej 5 ⭐⭐ Recursión:** escribe de forma recursiva `factorial(n)`, `fibonacci(n)` y `suma_digitos(n)`. Al lado, en un comentario, escribe la versión con bucle.

**Ej 6 ⭐⭐ Búsquedas:** implementa `busqueda_lineal(lista, x)` y `busqueda_binaria(lista, x)`. Cuenta cuántas comparaciones hace cada una con una lista del 1 al 1000.

**Ej 7 ⭐⭐ Burbuja:** implementa el ordenamiento burbuja **a mano**, sin `sort()`. Haz primero en papel un ejemplo con `[5, 2, 9, 1]`.

**Ej 8 ⭐⭐⭐ Reto: registro de lecturas:** guarda en una lista de diccionarios las lecturas de 5 usuarios:
```python
lecturas = [
    {"usuario": "Ana", "anterior": 120, "actual": 138},
    ...
]
```
Muestra el consumo de cada uno, quién consumió más y el total recaudado (usa tu función `calcular_pago` de la semana 2).

## Checklist de cierre

- [ ] Manejo listas, cadenas y diccionarios sin buscar cada método
- [ ] Puedo explicar la recursión con el ejemplo del factorial
- [ ] Sé explicar por qué la búsqueda binaria es más rápida
- [ ] Implementé un ordenamiento sin `sort()`
- [ ] Resolví al menos 6 de los 8 ejercicios sin que la IA escriba código
- [ ] Anoté la semana en la bitácora
