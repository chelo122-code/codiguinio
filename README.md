# codigo de señal con ruido
los pasos hechos para el desarrollo del codico, comienzan con la obtencion de datos an el sitio web physionet; el cual es un repositorio de señales vitales humanas, escoger algunas de las señales, en mi caso fue un EMG(electro miograma) del corazon, descargar los archivos .dat y .hea, que subiremos a nuestro archivo de python.

Los datos seran tratados en python colab con ayuda de la libreria "wfdb" que nos ayuda a leer los datos de los archivo.

El codigo contiene aparte de la señal fisiologica, tiene una señal de pulso, ruido gaussiano y una señal de artefacto

Los datos de analisis que se imprimen son: el tamaño de la lista, promedio de los valores del emg, desviacion estandar, coeficiente de variacion de los valores, potencia de la señal y del ruido, el valor SNR.

grafica de todas las señales, e histograma de la funcion de probabilidad

 COSAS A TENER EN CUENTA

 -Los datos leidos tiene que ser guardados en un solo canal para tener una sola lista de datos
 -los valores del ruido gaussiano son nombrados valores_random
-El SNR(Signal to Noise Ratio) es un indicar de que tan alterado esta una señal con respecto del ruido, siendo los valores positivos que el la señal el mayor que el ruido y mientras mas grande el valor mas distinguible de ruido(mas claro), y cuando es valor es negativo, la señal fue superada por el ruido, y no es muy legible
-En la señal artefacto esta condionada fija a la cantidad de datos del archivo probado, 50860 datos, asi que para otra cantidad de muestras se debera calcular diferentes frecuencia, y cambiar la cantidad de datos.
-los datos estan amplificados por 100 para poder visualizarlos mejor
-cada señal de ruido tiene una variable tiempo para sus operaciones

Nota:confio en ti, tu puedes:)
