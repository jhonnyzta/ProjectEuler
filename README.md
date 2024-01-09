# Proyecto Euler 
## Por: **Effe** / *Jhonny Zapata*

---

El presente repositorio contiene la solución a los ejercicios propuestos en *Project Euler* que como reto personal me he propuesto solucionar en los lenguajes de programación:

1. Python
2. C++
3. Julia
4. Rust
5. JavaScript

El objetivo es optimizar el código en cada lenguaje y de esta manera profundizar en las funcionalidades y potencialidades de los mismos. Los primeros cuatro lenguajes están ordenados en cuanto a tiempo que llevo trabajando con ellos, siendo Python en el que más experiencia tengo y Rust el que al momento de escribir estas lineas no poseo experiencia. Además he decidido incluir Javascript a la lista entendiendo que si bien los procesos realizados no son frecuentes en el desarrollo web, creo pueden tener utilidad en algunos proyectos como juegos o animaciones.

Además de presentar las soluciones también se van a ir anexando comparaciones respecto a tiempo de ejecución entre lenguajes y en algunos casos comparaciones dentro del mismo lenguaje utilizando diferentes estructuras.

---

### Ejemplo ilustrativo

El primer problema del Proyecto Euler plantea la siguiente situación:

Si listamos todos los números naturales menores que 10 que son mùltimos de 3 o de 5, tenemos 3,5,6 y 9. La suma de esos múltiplos es 23.

Encontrar la suma de todos los múltiplos de 3 o de 5 menores que 1000.

#### Enfoque básico:
Utilizando un ciclo for en Python se tiene:

```python
sum = 0
for i in range(1000):
    if (i%3==0 or i%5==0):
        sum+=i
print(sum)
```

Otro enfoque podría ser:

```python
lista = [i for i in range(1000) if (i%3==0 or i%5==0)]
print(sum(lista))
```

La cuestión que he intentado plantearme es comparar el rendimiento de cada 'manera' de definir, por lo que en algunos casos realizaré las comparaciones de estas 'maneras' de la siguiente forma:



