# Matplotlib

1. [Getting started](#schema1)
2. [Subplots](#schema2)
3. [Types of plots](#schema3)
4. [Leyendas ](#schema4)
5. [Object oriented plots](#scema5)



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

Crear los subplots con una separación
~~~python
plt.subplot(3,2,1)
plt.subplot(3,2,2)
plt.subplot(3,2,3)
plt.subplot(3,2,4)
plt.tight_layout()
~~~
![subplot](./image/subplot2.png)

Dibujar en algún subplot
~~~python
plt.subplot(3,2,1)
plt.subplot(3,2,2)
plt.plot(x,y)
plt.subplot(3,2,3)
plt.subplot(3,2,4)
plt.plot(x,x)
plt.tight_layout()
~~~
![subplot](./image/subplot3.png)
Ponerle a cada uno de los subplot sus leyendas para los ejes
~~~python
plt.subplot(3,2,1)
plt.plot(y,x)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.subplot(3,2,2)
plt.plot(x,x)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.tight_layout()
~~~
![subplot](./image/subplot4.png)

<hr>
<a name="schema3"></a>

# 3. Types of plots

Hay distintos tipos de plots, vamos a ver algunos.
~~~python
plt.plot(x,y)
~~~
![subplot](./image/t1.png)
~~~python
plt.scatter(x,y)
~~~
![subplot](./image/t2.png)

~~~python
plt.hist(x,y)
~~~
![subplot](./image/t3.png)

~~~python
plt.bar(x,y)
~~~
![subplot](./image/t4.png)

~~~python
plt.fill(x,y)
~~~
![subplot](./image/t5.png)

~~~python
plt.polar(x,y)
~~~
![subplot](./image/t6.png)



<hr>
<a name="schema4"></a>

# 4. Legends

Para poner las leyendas en las visualiaciones se pone:
~~~python
plt.plot(x,y,label = 'First example')
plt.legend()
~~~
![legend](./image/fe.png)

Poner la leyenda para cada eje
~~~python
plt.plot(x,y,y,x,label = 'First example')
plt.legend()
~~~
![legend](./image/l2.png)

Cambiar la posición de la leyenda
~~~python
plt.plot(x,y,y,x,label = 'First example')
plt.legend(loc = 2)
~~~

![legend](./image/l3.png)
~~~python
plt.plot(x,y,y,x,label = 'First example')
plt.legend(loc = 10)
~~~

![legend](./image/l4.png)

<hr>
<a name="schema5"></a>

# 5. Object oriented plots

Cambiar el tamaño de los ejes

~~~python
fig = plt.figure()
axes = fig.add_axes([0.1,0.1,1,1])
~~~
![axes](./image/oop1.png)

~~~python
fig = plt.figure()
axes = fig.add_axes([0.1,0.3,1,1])
~~~
![axes](./image/oop2.png)


~~~python
fig = plt.figure()
axes = fig.add_axes([0.1,0.3,1,1])
axes.plot(x,y)
~~~
![axes](./image/oop3.png)