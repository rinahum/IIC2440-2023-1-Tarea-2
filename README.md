# IIC2440-2023-1-Tarea-1
Repositorio para la tarea 1 de IIC2440 - Procesamiento de Datos Masivos.

## Integrantes:
- Rodrigo Nahum
- Fernando Quintana

# Codigo
El repositorio cuenta con dos notebooks, `Tarea2_P1.ipynb` y `Tarea2_P2.ipynb`. `P1` corresponde a la implementación de PageRank, y `P2` corresponde a la implementación de Single Source Shortest Path.

# Single Source Shortest Path
En este notebook, implementamos el algoritmo Single Source Shortest Path para grafos distribuidos, basados en el paso de mensajes. El algoritmo funciona de la siguiente manera. Mantenemos, para cada nodo, el costo de llegar a él desde un nodo inicial (este costo es inicialmente infinito). Luego, en cada iteración, cada nodo le manda a sus vecinos su costo actual más el costo de la arista que conecta con ese vecino. Hacemos esto hasta que los costos convergan, o sea, no cambien entre iteraciones.

Notemos que, para converger, este algorimto requiere a lo más una cantidad de iteraciones igual al largo del camino más largo entre el nodo inicial y algún otro nodo. Esto se podría reducir, manteniendo el costo de ir de un nodo `a` a un nodo `b`, para todo par de nodos (`a`, `b`). Con esta estrategia, la cantidad de iteraciones hasta converger sería logarítmico. Sin emabargo, esto requeriría almacenamiento cuadrático, y para grafos grandes, esto no nos parece factible.