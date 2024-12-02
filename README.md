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

Complejidad: Depende del número de vuelos y restricciones, pero se mitiga con poda y heurística.

### ESTACIONES DE BOMBEROS

