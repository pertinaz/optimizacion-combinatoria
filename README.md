### ORGANIZACION DE VUELOS
1. Representación del problema

    Estado: Una matriz de 15×10 donde cada celda representa una hora y contiene una lista de vuelos asignados.

    Operadores: Agregar un vuelo de una compañía a un horario específico.

    Restricciones:
        No más de dos vuelos de la misma compañía a la misma hora.
        Vuelos al mismo destino de una compañía separados al menos 6 horas.

    Función de costo: Ganancia negativa del aeropuerto para que A* minimice el costo.

    Función heurística: Número de vuelos restantes penalizado por violaciones de restricciones.

2. Diseño del algoritmo

    Definir el espacio de estados:
        Crear una estructura que represente el horario parcial.
        Incorporar una lista de vuelos pendientes para asignar.

    Crear operadores válidos:
        Verificar restricciones antes de aplicar el operador.

    Implementar una función heurística mejorada:
        Penalizar estados con conflictos.
        Priorizar estados que maximicen la ganancia.

    Estructurar el algoritmo A*:
        Usar una cola de prioridad basada en f(n)=g(n)+h(n)f(n)=g(n)+h(n).
        Explorar estados en orden de costo estimado más bajo.

Entrada: Lista de vuelos disponibles (compañía, destino, ganancia).

Salida: Horario óptimo que maximiza la ganancia cumpliendo restricciones.


# RESPUESTA

### ESTACIONES DE BOMBEROS
1. Representación del problema
    - Estado: Una cuadrícula N×MN×M donde cada celda contiene:

        - Número de estaciones de bomberos.
        - Número de camiones asignados.

    - Restricciones:

        - No exceder PP estaciones de bomberos.
        - Asignar exactamente CC camiones.
        - Respetar el rango de 1 a 3 camiones por estación.

    - Función de costo: 
        - Penalizar la cantidad de camiones y estaciones usadas para minimizar costos.

    - Función heurística: 
        - Aproximar la mejora en el factor de seguridad con los camiones restantes.

2. Diseño del algoritmo
    - Estado inicial: 
        - Cuadrícula vacía sin estaciones ni camiones asignados.

    - Espacio de estados:

        -  Asignar estaciones de bomberos y camiones progresivamente.

    - Operadores válidos:

        -  Colocar una estación en una celda.
        - Asignar 1, 2 o 3 camiones si la celda tiene una estación.

    - Función heurística:

        - Calcular el potencial incremento en el factor de seguridad basado en las celdas restantes.

    - Criterio de finalización:

        - Todas las estaciones (PP) y camiones (CC) han sido asignados.

#### Ventajas del enfoque

    *Restricciones respetadas*: Las restricciones son verificadas en cada paso.

    *Óptimo global*: A* asegura la solución con el mayor factor de seguridad.

    *Escalabilidad*: Puede adaptarse a cuadrículas más grandes y restricciones adicionales.

#### Limitaciones

    *Complejidad computacional*: Puede ser costoso si N×MN×M es grande.

    *Dependencia de la heurística:* Una mala heurística puede ralentizar la solución.

Complejidad: Depende del número de vuelos y restricciones, pero se mitiga con poda y heurística.

### ESTACIONES DE BOMBEROS

