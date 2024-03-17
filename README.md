# Reto #4 programación de computadores

## Resolver los siguientes problemas usando un notebook de python y subirlos a un repo.

1. [Dado un número entero, determinar si ese número corresponde al código ASCII de una vocal minúscula.](#minusculas)

2. [Dada una cadena de longitud 1, determine si el código ASCII de primera letra de la cadena es par o no.](#par-o-no)

3. [Dado un carácter, construya un programa en Python para determinar si el carácter es un dígito o no.](#digito-o-no)

4. [Dado un número real x, construya un programa que permita determinar si el número es positivo, negativo o cero. Para cada caso de debe imprimir el texto que se especifica a continuación:](#positivo-negativo-o-cero)

- Positivo: "El número x es positivo"
- Negativo: "El número x es negativo"
- Cero (0): "El número x es el neutro para la suma"

5. [Dado el centro y el radio de un círculo, determinar si un punto de R2 pertenece o no al interior del círculo.](#circulo)

6. [Dadas tres longitudes positivas, determinar si con esas longitudes se puede construir un triángulo.](#triangulo)



***

## Minusculas  

```{python}
numeroEntero = int((input("Ingrese un número entero: ")))
if numeroEntero == 97 or numeroEntero == 101 or numeroEntero == 105 or numeroEntero == 111 or  numeroEntero == 117: 
    print("El código ASCII ", numeroEntero, " corresponde a la vocal minuscula", chr(numeroEntero))
else: 
    print("El código ASCII ", numeroEntero, " no corresponde a una vocal minuscula")

```
***
## Par o no 

```{python}
caracter : str = input("Ingrese un carácter: ")
codigo_ASCII = ord(caracter)
modulo = codigo_ASCII%2 
if modulo == 0: 
    print("El código ASCII de su caracter es par")
else: 
    print("El código ASCII de su caracter no es par")
```
***

## Digito o no 

```{python}
caracter : str = input("Ingrese un carácter: ")
codigo_ASCII = ord(caracter)
modulo = codigo_ASCII%2 
if modulo == 0: 
    print("El código ASCII de su caracter es par")
else: 
    print("El código ASCII de su caracter no es par")
```
***
## Positivo, negativo o cero
```{python}
numero = float((input("Ingrese un número real: ")))
if numero > 0: 
    print("El número ", numero ,"es positivo")
elif numero < 0: 
    print("El número ", numero, "es negativo")
else: 
    print("El número ", numero, "es el neutro para la suma")
```
***
## Circulo

```{python}
centro_x = float(input("Ingrese la coordenada x del centro del circulo: "))
centro_y = float(input("Ingrese la coordenada y del centro del circulo: "))
radio = float(input("Ingrese el radio del circulo: "))

R2_x = float(input("Ingrese la coordenada x del punto: "))
R2_y = float(input("Ingrese la coordenada y del punto: "))

distancia = (R2_x - centro_x) ** 2 + (R2_y- centro_y) ** 2

if distancia < (radio ** 2):
    print("El punto esta dentro del circulo.")
else:
    print("El punto no esta dentro del circulo.")
```
***
## Triangulo
```{python}
a = float(input("Ingrese la longitud 1: "))
b = float(input("Ingrese la longitud 2: "))
c = float(input("Ingrese la longitud 3: "))

if a + b > c and a + c > b and b + c > a: 
    print("Se puede construir un triangulo con las longitgudes ", a, b, c)
else: 
    print(" No se puede construir un triangulo con las longitgudes ", a, b, c)
```
