# Matplotlib

1. [Getting started](#schema1)
2. [Subplots](#schema2)
1. [Leyendas ](#schema1)



<hr>

<a name="schema1"></a>

# 1. Getting started
1º Importar Matplotlib
~~~python
import matplotlib.pyplot as plt
~~~
Y casi siempre vamos a necesitar `numpy` y `pandas`
~~~python
import pandas as pd
import numpy as np
~~~

2º Hacer el primer plot
~~~python
plt.plot(x,y)
~~~
![image](./image/001.png)

3º Añadir títulos a los ejes y ponerle un título
~~~python
plt.plot(x,x)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('First title')
~~~
![image](./image/first_title.png)

<hr>

<a name="schema2"></a>

# 2. Subplots
Crear varios conjutos de ejes devolviendo una referencia a la figura y a los ejes.
~~~python
plt.subplot(3,2,1)
plt.subplot(3,2,2)
plt.subplot(3,2,3)
plt.subplot(3,2,4)
~~~
![subplot](./image/subplot.png)


<hr>

<a name="schema1"></a>

# 1. Leyendas

Para poner las leyendas en las visualiaciones se pone:
~~~python
plt.plot(x,y,label = 'First example')
plt.legend()
~~~