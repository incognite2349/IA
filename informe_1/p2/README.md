## ¿Cómo cambia el comportamiento del algoritmo si cambiamos la función de costo?

va a variar en funcion de lo que busquemos, si lo dejamos sin que busque algo en especifico llegara por cualquier camino por lago que pueda ser, pero si le ponemos un algoritmo como A\* comenzara a filtrar y decidir en funcion del costo

## ¿Qué sucede si hay múltiples salidas en el laberinto? ¿Cómo podrías modificar el algoritmo para manejar esto?

haciendo que a pesar de encontrar una salida, siga explorando el laberinto en busca de mas y guarde los resultados en una lista para luego reconstruir el camino de cada una de las salidas encontradas para al final imprimirlas con su longitud y los pasos que da

## Modifica el laberinto por uno más grande y con otro tipo de obstáculo además de paredes. ¿Qué limitación encuentras en el algoritmo?
En mi caso, con el tema de los portales, encontré que al principio no los reconocía o caía en bucles, por lo que tuve que corregir su funcionamiento. Además, el algoritmo se empeñaba en buscar diferentes rutas y, en algunas ocasiones, tomaba caminos largos e ilógicos, lo cual también tuve que ajustar. Ahora tengo la limitación de que cada vez debe repetir el proceso y recorrer todos los caminos posibles, lo que resulta ineficiente.