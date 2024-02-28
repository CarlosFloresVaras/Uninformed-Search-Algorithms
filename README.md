Uninformed Search Algorithms

Inteligencia Artificial

Inteligencia Biológica
Alejandra Escallada Martínez
Efrén Flores Porras
Carlos Flores Varas

Versión del código: 
v 1.0.0

PROPÓSITO
El propósito de este proyecto es mostrarle al usuario los algoritmos de búsqueda en grafos a través de una interfaz gráfica, en donde el usuario podrá escoger el nodo de inicio y el nodo destino de un grafo, en donde se le mostrará el camino que recorre cada algoritmo para llegar al nodo final. Se implementarán los siguientes algoritmos de búsqueda: búsqueda a lo ancho (DFS), Dijkstra, búsqueda por profundidad (BFS), búsqueda por profundidad con límite y búsqueda por profundidad iterativa. 

INSTRUCCIONES
Para utilizar el programa de algoritmos de búsqueda, es necesario instalar las siguientes librerías: networkx, matplotlib.pylot, time, tkinter, OpenCV, PIL.Image y PIL.ImageTk. También se tiene que asegurar que el programa se encuentre en un notebook de Python (con la extensión ipynb).
Una vez asegurado lo anterior, podemos ejecutar el programa (asegurarse de correr todo el notebook “Ejecutar Todo” cada vez que se quiera ejecutar la implementación).
Al ejecutarlo, aparecerá una ventana en donde se deberán de insertar el nodo donde iniciará la búsqueda, el nodo final, el límite máximo para el BFS con límite, y la profundidad máxima para el BFS iterativo. 

Figura 1 Interfaz de algoritmos de búsqueda
Debajo de los espacios de inserción de datos, se encuentran 7 botones. El primer botón “RUN ALL” muestra el camino recorrido de todos los algoritmos de búsqueda, el segundo botón “TIME ALL” que muestra únicamente el tiempo de ejecución de los algoritmos, y los 5 botones restantes que realizan la búsqueda respectiva de manera individual. Si nos vamos de izquierda a derecha, el primer botón “BFS” realiza la búsqueda a lo profundo, el siguiente botón “Dijkstra” el algoritmo Dijkstra, luego el botón “DFS” que realiza la búsqueda por profundidad, después el “DLS” que realiza el algoritmo de profundidad con límite, y hasta la derecha el BFS iterativo “IDS”. 
Una vez insertados los datos, se podrá escoger entre realizar todas las búsquedas, o cada búsqueda de manera individual, y al presionar cualquier opción, en la parte inferior de los botones aparecerán el camino recorrido del algoritmo seleccionado y sus respectivos datos, ya sea el costo para el algoritmo Dijkstra, o el número de iteraciones para el algoritmo IDS.
Además de mostrar los tiempos de ejecución con el botón “TIME ALL”, cada algoritmo individual muestra su tiempo de ejecución en milisegundos, o en su defecto, al escoger “RUN ALL” también se mostrarán los tiempos de cada algoritmo.
LIBRERIAS
networkx
matplotlib.pylot
time
tkinter
OpenCV
PIL.Image
PIL.ImageTk

VARIABLES GLOBALES
G: Objeto que representa un grafo dirigido.
Pos: Diccionario que contiene las posiciones de cada nodo.
edge_labels: Obtiene el costo de cada arista.
window: Ventana principal de la interfaz.
title: Objeto de Tkinter que muestra el título de la ventana principal.
label_graph: Objeto label de Tkinter para mostrar el grafo.
img_grafo: Imagen del grafo generada con matplotlib.pylot.
frame_input: Frame para las cajas de texto.
entry_start: Objeto de entrada de Tkinter para ingresar el nodo inicial.
entry_target: Objeto de entrada de Tkinter para ingresar el nodo destino.
entry_limit: Objeto de entrada de Tkinter para ingresar el límite de profundidad.
entry_max_limit: Objeto de entrada de Tkinter para ingresar la profundidad máxima.
frame_botones: Frame para los botones “BFS”, “DIJKSTRA”, “DFS”, “DLS” e “IDS”.
button_buscar_ruta: Botón “RUN ALL” de Tkinter que realiza la búsqueda de todos los algoritmos
button_bfs: Botón “BFS” que realiza la búsqueda BFS.
button_dijkstra: Botón “Dijkstra” que realiza la búsqueda Dijkstra.
button_dfs: Botón “DFS” que realiza la búsqueda DFS.
button_dls: Botón “DLS” que realiza la búsqueda DLS.
button_ids: Botón “IDS” que realiza la búsqueda IDS.
frame_ruta: Frame que contiene las rutas de cada búsqueda

FUNCIONES DE APOYO
bfs()
PROPÓSITO: Ejecuta la búsqueda BFS en la terminal desde el nodo inicial hasta el nodo destino.
PARÁMETROS:
graph: Grafo
start: Nodo inicial
target: Nodo destino
RESULTADO DE EJECUCIÓN: Impresión de todos los nodos recorridos desde el nodo inicial hasta el nodo destino.
dijkstra()
PROPÓSITO: Ejecuta la búsqueda Dijkstra en la terminal desde el nodo inicial hasta el nodo destino.
PARÁMETROS:
G: Grafo
start: Nodo inicial
target: Nodo destino
RESULTADO DE EJECUCIÓN: Impresión de todos los nodos recorridos desde el nodo inicial hasta el nodo destino, y el costo del camino recorrido.
depth_first_search()
PROPÓSITO: Ejecuta la búsqueda DFS en la terminal desde el nodo inicial hasta el nodo destino.
PARÁMETROS:
Graph: Grafo
start: Nodo inicial
target: Nodo destino
RESULTADO DE EJECUCIÓN: Impresión de todos los nodos recorridos desde el nodo inicial hasta el nodo destino.
DepthLimitedSearch()
PROPÓSITO: Ejecuta la búsqueda DLS en la terminal con límite de profundidad dado desde el nodo inicial hasta el nodo destino.
PARÁMETROS:
Graph: Grafo
Start: Nodo inicial
Target: Nodo destino
Limit: Límite de profundidad
RESULTADO DE EJECUCIÓN: Impresión de todos los nodos recorridos desde el nodo inicial hasta el nodo destino.
DLS()
PROPÓSITO: Función recursiva para implementar la búsqueda DLS y la búsqueda IDS.
PARÁMETROS:
Graph: Grafo
Start: Nodo inicial
Target: Nodo destino
Limit: Límite de profundidad
RESULTADO DE EJECUCIÓN: 
IterativeDeepeningSearch()
PROPÓSITO: Realiza la búsqueda IDS con una profundidad máxima dada, desde el nodo inicial hasta el nodo destino
PARÁMETROS:
Graph: Grafo
Start: Nodo inicial
Target: Nodo destino
MaxDepth: Profundidad máxima
RESULTADO DE EJECUCIÓN: Impresión de todos los nodos recorridos desde el nodo inicial hasta el nodo destino, y el número de iteraciones llevadas a cabo en el recorrido.

FUNCIONES PRINCIPALES
run_all()
PROPÓSITO: Ejecuta todos los algoritmos de búsqueda a la vez.
PARÁMETROS: Nodo Inicial, Nodo Final, Límite Máximo y Profundidad Máxima
RESULTADO DE EJECUCIÓN: Muestra todos los caminos recorridos de cada algoritmo de búsqueda, el costo de la búsqueda Dijkstra, el número de iteraciones de la búsqueda y el tiempo de ejecución de cada algoritmo

time_all()
PROPÓSITO: Mostrar el tiempo que tardo en ejecutar cada método.
PARÁMETROS: Nodo Inicial, Nodo Final, Límite Máximo y Profundidad Máxima
RESULTADO DE EJECUCIÓN: Muestra únicamente el tiempo tardado en ejecutarse y completarse cada método de busqueda (en milisegundos).

buscar_ruta_BFS()
PROPÓSITO: Realiza la búsqueda BFS dentro de la interfaz gráfica desde el nodo inicial hasta el nodo destino.
PARÁMETROS: Nodo Inicial y Nodo Final
RESULTADO DE EJECUCIÓN: Muestra todos los nodos recorridos para llegar al nodo destino, y el tiempo de ejecución

buscar_ruta_Dijkstra()
PROPÓSITO: Ejecuta todos los algoritmos de búsqueda a la vez.
PARÁMETROS: Nodo Inicial y Nodo Final
RESULTADO DE EJECUCIÓN: Muestra todos los nodos recorridos para llegar al nodo destino, el costo y el tiempo de ejecución.

buscar_ruta_DFS()
PROPÓSITO: Ejecuta todos los algoritmos de búsqueda a la vez.
PARÁMETROS: Nodo Inicial y Nodo Final
RESULTADO DE EJECUCIÓN: Muestra todos los nodos recorridos para llegar al nodo destino, y el tiempo de ejecución.

buscar_ruta_DLS()
PROPÓSITO: Ejecuta todos los algoritmos de búsqueda a la vez.
PARÁMETROS: Nodo Inicial, Nodo Final y Límite Máximo
RESULTADO DE EJECUCIÓN: Muestra todos los nodos recorridos para llegar al nodo destino, y el tiempo de ejecución.

buscar_ruta_IDS()
PROPÓSITO: Ejecuta todos los algoritmos de búsqueda a la vez.
PARÁMETROS: Nodo Inicial, Nodo Final, Límite Máximo y Profundidad Máxima
RESULTADO DE EJECUCIÓN: Muestra todos los nodos recorridos para llegar al nodo destino, el número de iteraciones que se llevaron a cabo, y el tiempo de ejecución.
