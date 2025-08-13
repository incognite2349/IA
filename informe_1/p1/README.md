# Analisis del problema

Se nos exige encontrar la ruta mas corta y menos costosa para llegar de un punto A a un B, para este proceso se nos fue asignado el algoritmo A\* que consiste en una comparacion de costos finales de todos los caminos en pro de dejar el menos costoso.

## ¿Cómo se aplica A\*?

1. Define el punto de inicio (`initial`) y el objetivo (`goal`).
2. El algoritmo expande nodos desde el inicio, calculando para cada ciudad:

   - El costo real acumulado desde el inicio (g(n)).
   - La heurística h(n), que en este caso es la distancia en línea recta desde la ciudad actual hasta el objetivo. Esta distancia se calcula usando las coordenadas (x, y) de cada ciudad y la fórmula de distancia euclídea:

     ```python
     import math
     def h(node):
         x1, y1 = coordinates[node.state]
         x2, y2 = coordinates[goal]
         return math.hypot(x2 - x1, y2 - y1)
     ```

3. La función de evaluación es `f(n) = g(n) + h(n)`, y siempre se expande el nodo con menor f(n).
4. Cuando se alcanza el objetivo, se reconstruye el camino óptimo usando los padres de cada nodo.

Así, A\* encuentra el camino más corto entre cualquier par de ciudades, guiándose por los costos reales y la estimación informada de la distancia restante gracias a las coordenadas.

## ¿Por qué se considera que la ruta encontrada es óptima?

En cada paso, compara el costo real acumulado (g(n)) más la heurística (h(n)) para cada posible ruta.
Siempre expande el nodo con el menor valor de f(n) o costo.

Si encuentra un camino más barato a un nodo ya visitado, se devuelve y actualiza ese nodo y su ruta.
Así, A\* garantiza que cuando llega al objetivo, ha encontrado el camino de menor costo total, usando tanto la información real como la estimada (heurística).

## Ejecución

Puedes modificar las variables `initial` y `goal` en el notebook para buscar el camino óptimo entre cualquier par de ciudades.

---

> Proyecto para fines educativos. Inspirado en el clásico problema de Rumania de Inteligencia Artificial.
