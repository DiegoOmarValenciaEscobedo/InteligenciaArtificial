# Algoritmo para poder ganar un TikTakToe 3D

Para poder ganar este juego me lo imagino de la siguiente manera, en el algoritmo que explicare a continuación, solo tener en consideración 2 factores, uno no muy importante y el otro de gran peso, para empezar la figura que se elegira y la otra es quien inicia el juego, ya que al ser el primero en elegir la casilla, hay mas posibilidades de ganar el juego.

> **Nota:** Para casos del ejemplo se tomara la figura '**X**' para la maquina y hacer la simulacion de que el usuario es quien empieza el juego siempre.

## Peso de las casillas

Para este punto me gustaria poner 3 valores

 - Valor 1 de menor peso (Casillas intermedias).
 - Valor 2 de peso intermedio (Casillas de las esquinas).
 - Valor 3 de mayor peso (Casillas del centro).

Ya teniendo en cuenta los valores podremos tener en cuenta que casillas se priorizaran a ocupar primero, 


---
## Seleccionar el plano donde empezar
Este punto es muy importante ya que se debe verificar cual es el plano donde debe comenzar el juego, esto ya que al ser un cubo puede empezar en el nivel 1, 2, 3, de lado que sea o en diagonal. Por esto mismo siempre el usuario es quien comienza la partida y asi el decide en que plano comienza a jugar.

---

## Funciones 
Ahora ya sabiendo esto podemos empezar a ver las funciones que debe de tener el sistema para que funcione al 100%.
A mi punto de vista creo que son necesarias las siguientes funciones:

 - **Funcion para buscar la mejor casilla:** Esta función seria la principal ya que dentro de esta se haran uso de otras funciones para determinar la coordenada donde se pondra la ficha.
 - **Funcion para primer turno:** Esta función empezaría buscando la casilla cercana a donde el usuario puso su primer turno, buscamos la casilla adyaciente con mayor peso y se coloca ahi, si son varias pues sería la primer que se encuentre, y devolveria la coordenada donde esta esa casilla.
**Funcion para verificar trayectoria:** Esta función tomaria el valor que nos dia la función anterior y en base a todos las fichas propias que tiene el tablero, ver si es la mejor opción de manera que puede que aunque sea la casilla con mayor peso, no se genere una trayectoria ganadora, o sea recta, si no que sea en forma de **L**.
**Funcion para buscar amenaza:** Esta función buscaria en el tablero a ver si el usuario esta proximo a ganar y asi devolver la coordenada donde esta la amenaza, ya que de ser asi, se prioriza el obstruir el paso del usuario antes que todo.
**Funcion para verificar ganar:** Esta ultima seria para ver si al colocar la ficha del ultimo turno se ha ganado, tambien despues de cada turno del usuario para verificar si el ha ganado.
