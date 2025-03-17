# Ejercicios estructuras repetitivas
1) Crea una aplicación que pida un número y calcule su factorial (La factorial de un número es el
producto de todos los enteros entre 1 y el propio número y se representa por el número
seguido de un signo de exclamación. ¡Por ejemplo 5! = 1x2x3x4x5=120),
R// Algoritmo Calcular_factorial
	definir a,b,num1 Como Real
	a<-1 
	Escribir "ingresa un numero"
	leer num1
	Para b<-1 Hasta num1 Con Paso 1 Hacer
		a<-a*b
	Fin Para
	Escribir "el factorial es:" num1
	escribir "es:" a 
	FinAlgoritmo

2)Crea una aplicación que permita adivinar un número. La aplicación genera un número
aleatorio del 1 al 100. A continuación, va pidiendo números y va respondiendo si el número a
adivinar es mayor o menor que el introducido, además de los intentos que te quedan (tienes
10 intentos para acertarlo). El programa termina cuando se acierta el número (además te dice
en cuantos intentos lo has acertado), si se llega al límite de intentos te muestra el número que
había generado.
R// Algoritmo adivina_el_numero
	Definir num_secreto, num_usuario, intentos Como Entero
    num_secreto <- Aleatorio(1, 100)
    intentos <- 10
	Escribir "¡Bienvenido al juego de adivinar el número!"
    Escribir "Tienes 10 intentos para adivinar un número entre 1 y 100."
	Repetir
        Escribir "Introduce un número:"
        Leer num_usuario
        intentos <- intentos - 1
	      Si num_usuario = num_secreto Entonces
            Escribir "¡Felicidades! Has adivinado el número en ", 10 - intentos, " intentos."
        Sino
            Si num_usuario > num_secreto Entonces
                Escribir "El número es menor. Intentos restantes: ", intentos
            Sino
                Escribir "El número es mayor. Intentos restantes: ", intentos
            FinSi
        FinSi
		Hasta Que intentos = 0
    Si num_usuario <> num_secreto Entonces
        Escribir "¡Lo siento! Se acabaron los intentos. El número correcto era: ", num_secreto
    FinSi
FinAlgoritmo

3)Algoritmo que pida números hasta que se introduzca un cero. Debe imprimir la suma y la
media de todos los números introducidos
R// Algoritmo pedirnumeros
	Definir num, suma, cantidadNumeros Como Entero
    suma <- 0
    cantidadNumeros <- 0
    Repetir
        Escribir "Introduce un número (0 para salir): "
        Leer num
            Si num <> 0 Entonces
            suma <- suma + num
            cantidadNumeros <- cantidadNumeros + 1
        FinSi
    Hasta Que num = 0
    Si cantidadNumeros > 0 Entonces
        Escribir "La suma de los números es: ", suma
        Escribir "La media de los números es: ", suma / cantidadNumeros
    Sino
        Escribir "No se ingresaron números válidos."
    FinSi
FinAlgoritmo

4)Realizar un algoritmo que pida números (se pedirá por teclado la cantidad de números a
introducir). El programa debe informar de cuantos números introducidos son mayores que 0,
menores que 0 e iguales a 0.
R// Algoritmo Numeros_introducidos 
	definir num_introducido, num_mayores, num_menores, num_iguales Como Real
	num_mayores <- 0
    num_menores <- 0
    num_iguales <- 0
	Repetir
        Escribir "Ingresar número (pulsar 0 para salir):"
        Leer num_introducido
		Si num_introducido > 0 Entonces 
            num_mayores <- num_mayores + 1
        Sino 
			Si num_introducido < 0 Entonces 
				num_menores <- num_menores + 1
			Sino
				num_iguales <- num_iguales + 1
			FinSi 
		FinSi
	Hasta Que num_introducido = 0
		Escribir "Cantidad de números mayores a 0: ", num_mayores
		Escribir "Cantidad de números menores a 0: ", num_menores
		Escribir "Cantidad de números iguales a 0: ", num_iguales 
	FinAlgoritmo

5) Algoritmo que pida caracteres e imprima ‘VOCAL’ si son vocales y ‘NO VOCAL’ en caso
contrario, el programa termina cuando se introduce un espacio.
R// Algoritmo identificar_vocal
	definir caracter Como Caracter
	repetir 
		Escribir "ingresar caracteres"
		leer Caracter
		si Caracter = ""  Entonces
			Escribir "programa finalizado"
			sino 
				si Caracter = "a" o caracter = "e" o caracter = "i" o caracter = "o" o caracter = "u"
					Escribir "vocal"
				SiNo
					Escribir "no vocal"
				FinSi
		FinSi
	Hasta Que caracter = ""
FinAlgoritmo

6) Escribir un programa que imprima todos los números pares entre dos números que se le pidan
al usuario.
R// Algoritmo numeros_pares 
	definir nume, a Como Entero
	escribir "ingresar numeros"
	Leer nume
	Leer nume
	para a <-2 Hasta (nume) Con Paso 2 Hacer
		Escribir a 
	FinPara
	FinAlgoritmo

7) Realizar un algoritmo que muestre la tabla de multiplicar de un número introducido por
teclado.
R//Algoritmo mostrar_tablas 
	definir num1, a Como Entero
	escribir "ingresa tu numero"
	Leer num1
	para a <-1 Hasta 10 con paso 1 Hacer
		Escribir num1, "x" , a,  "=" num1 * a
	FinPara
	FinAlgoritmo

8) Escribe un programa que pida el límite inferior y superior de un intervalo. Si el límite inferior es
mayor que el superior lo tiene que volver a pedir. A continuación, se van introduciendo
números hasta que introduzcamos el 0. Cuando termine el programa dará las siguientes
informaciones:
La suma de los números que están dentro del intervalo (intervalo abierto).
Cuantos números están fuera del intervalo.
He informa si hemos introducido algún número igual a los límites del intervalo.
R// Algoritmo IntervaloNumeros
    Definir li, ls, num, suma, fuera, limite Como Entero
    suma <- 0
    fuera <- 0
    limite <- 0
    Repetir
        Escribir "Ingrese el límite inferior:"
        Leer li
        Escribir "Ingrese el límite superior:"
        Leer ls
    Hasta Que li < ls
    Repetir
        Escribir "Ingrese un número (0 para salir):"
        Leer num
        Si num <> 0 Entonces
            Si num > li Y num < ls Entonces
                suma <- suma + num
            Sino
                fuera <- fuera + 1
            FinSi
            Si num = li O num = ls Entonces
                limite <- 1
            FinSi
        FinSi
    Hasta Que num = 0
    Escribir "Suma dentro del intervalo: ", suma
    Escribir "Cantidad fuera del intervalo: ", fuera
    Escribir SiNo(limite = 1, "Se ingresó un número igual a los límites.", "No se ingresó ningún número igual a los límites.")
FinAlgoritmo

9) Escribe un programa que, dados dos números, uno real (base) y un entero positivo
(exponente), saque por pantalla el resultado de la potencia. No se puede utilizar el operador
de potencia.
R// Algoritmo porcentaje
	Definir num1, resultado Como real
	Definir num2, a Como Entero
	Escribir "escribe tu numero"
	leer num1
	Escribir "escribe tu numero"
	leer num2
	resultado <-1
	Para a <- 1 hasta num2 Hacer
		resultado = resultado * num1
	FinPara
	Escribir "el resultado de ", num1, " elevado a ", num2, " es " resultado
FinAlgoritmo

10) Algoritmo que muestre la tabla de multiplicar de los números 1,2,3,4 y 5.
R//Algoritmo tablas_multiplicar
	Definir num, i Como Entero
    Para num <- 1 Hasta 5 Hacer
        Escribir "Tabla del ", num, ":"
        Para i <- 1 Hasta 10 Hacer
            Escribir num, " x ", i, " = ", num * i
        FinPara
		Escribir "" 
    FinPara
FinAlgoritmo


