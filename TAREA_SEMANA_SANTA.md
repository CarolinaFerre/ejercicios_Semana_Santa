# tarea_Semana_Santa
Ejercicios de repaso mandados como tarea de Semana Santa


        Ejercicios de repaso programación en java 2º EV.						

    1. Realizar los siguientes métodos que trabaja con String.

A)  Dado dos String a y b devolver un nuevo String con el primer carácter  del String a y el último de la cadena b. Si alguno de ellos tiene longitud nula se añadirá el carácter @.

http://codingbat.com/prob/p138183  (Enlace )

public String lastChars(String a, String b)

Ejemplos:

lastChars("last", "chars") → "ls"
lastChars("yo", "java") → "ya"
lastChars("hi", "") → "h@"

SOLUCIÓN:



B) Dado un String devolver true si aparecen el mismo número de veces el  string "cat"  y "dog"

http://codingbat.com/prob/p111624  (Enlace )

public boolean catDog(String str)

catDog("catdog")→ true
catDog("catcat")→ false
catDog("1cat1cadodog") → true

SOLUCIÓN:

C) Dado un String donde puede aparecer un o varios asterisco  devolver true si entre cada asterisco hay dos letras iguales.   Si no hay asteriscos se devolverá true igualmente. O si solo hay asteriscos  al principio o al final.

public boolean sameStarChar(String str)

http://codingbat.com/prob/p194491  (Enlace)

Ejemplos:

sameStarChar("xy*yzz")→true
sameStarChar("xy*zzz")→false
sameStarChar("*xa*az") → true

SOLUCIÓN:


                                                                  
2. Realizar los siguientes métodos que trabaja con vectores.

 A)  Dado el  array de enteros nums devolver un nuevo array con el doble de tamaño donde todos sus valores estén a cero salvo el último que tendrá el mismo valor que último valor de array nums.

public int[] makeLast(int[] nums)

http://codingbat.com/prob/p137188 (Enlace)


makeLast([4, 5, 6]) → [0, 0, 0, 0, 0, 6]
makeLast([1, 2]) → [0, 0, 0, 2]
makeLast([3]) → [0, 3]


SOLUCIÓN:

B) Dado el array de enteros nums devolver true si solo contiene los valores 1 o 4.

public boolean only14(int[] nums)

http://codingbat.com/prob/p186672  (Enlace)

only14([1, 4, 1, 4]) → true
only14([1, 4, 2, 4]) → false
only14([1, 1]) → true


SOLUCIÓN:

C) Dado un número n>= 0, devolver un array que tenga la siguiente serie numérica en función de valor de n {1,  1, 2,  1, 2, 3, ... 1, 2, 3 .. n}. El tamaño de la nueva tabla dependerá de valor n, calculándose  según la formula n*(n + 1)/2.

http://codingbat.com/prob/p104090 (Enlace)

seriesUp(3) → [1, 1, 2, 1, 2, 3]
seriesUp(4) → [1, 1, 2, 1, 2, 3, 1, 2, 3, 4]
seriesUp(2) → [1, 1, 2]



SOLUCIÓN:



Ejercicios sobre clases y objetos
1. Crear una clase PilaEnteros que implemente una pila ( LIFO Último en entrar es el primero en salir)  de números enteros. Para la implementación se utilizará un array de enteros de tamaño fijo que se define cuando se crea el objeto, y un contador que me indica el número de valores introducidos y la posición del siguiente valor a almacenar.

La clase tendrá los siguientes métodos:
•	PilaEnteros (int tamaño) Crea un pila fijando el tamaño máximo.
•	push(int valor) Introduce un entero en la lista. Devuelve verdadero si cabe o falso si la tabla está llena.
•	pop()  Extrae un entero (el último que se ha introducido) de la lista y lo devuelve de la lista, si no hay ningún número devuelve -1;
•	peek() Devuelve el último entero introducido pero sin eliminarlo o -1 si no hay ningún número almacenado.
•	estaLleno() Devuelve verdadero si la capacidad array está completo.
•	estaVacio() Devuelve verdadero si la pila está vacía.
Crea un programa principal que utilice la clase anterior o probar con el Bluej el funcionamiento de la clase.
Ejemplo si creamos una pila  PilaEnteros(5)
  int valores [] → {0,0,0,0,0}
  contador = 0;
y llamamos a los métodos push(5) y push (6)
valores = {5,6,0,0,0}  y contador = 2
Si luego llamamos pop(); → devolvera 6, si luego hacemos push(7); push(4) la tabla se quedara con lo valores:
valores = {5,7,4,0,0} y contador = 3
peek() → me devolvería 4 y estaLleno y estaVacio devolverían false.

SOLUCIÓN:

2. Haz una clase llamada Password que siga las siguientes condiciones:
•	Que tenga solamente un  atributo contraseña (String)
•	Los constructores serán los siguiente:
•	Un constructor por defecto.  Password() genera una contraseña segura de forma automática. (llama a generarPassword)
•	Un constructor a partir de una cadena pasada como parámetro, contraseña cogerá el valor de al cadena.  Password(“Topsecret03”)
•	Los métodos que implementa serán:
•	esFuerte(): devuelve un booleano si es fuerte o no, para que sea fuerte debe cumplir las siguiente condiciones:
•	 Una longitud igual o mayor que 8
•	 Tener alguna mayúsculas y alguna minúscula
•	 Tener algún dígito numérico.
•	 Tener algún carácter no Alfanumérico
•	generarPassword(): genera la contraseña  con una longitud entre 10 y 15, pero garantizando que sea fuerte ( usar random) Este método será privado
•	Método getPassword para obtener el valor de la contraseña.

Ahora, crea una clase llamada PruebaContraseña que solo tiene un método main:
•	Crea un array de Passwords con el tamaño que tu le indiques por teclado.
•	Crea un bucle que cree un objeto Password para cada posición del array.
 Se preguntará al usuario que tipo de contraseña se creará: automática o con un valor concreto.
•	Crea otro array de booleanos donde se almacene si el password del array de Password es o no fuerte (usa el bucle anterior).
•	Al final, muestra la contraseña y si es o no fuerte usando los datos de ambas tablas. Usa este simple formato:
VALOR             FUERTE
	12345             false
	M23iesm20x   true

SOLUCIÓN

3. Gestión de sala de Cine
Se solicita hacer la gestión de un cine que dispone solo de una sala. Para ello se define las siguientes clases: Cine, Espectador, Película, Genero y TestCine
Cine
Atributos:
  Número de filas y número de columnas que especifica el tamaño de la sala  Filas x Columna
 
Tabla de asientos que pues estar libres (null) o tener asignado un espectadores

Los posiciones de los asientos será identificadas  por una letra (columna) y un número (fila), la fila 1 empieza al final de la matriz como se muestra en la tabla. También deberemos saber si está ocupado o no el asiento. Por ejemplo en una sala de 8 filas y 8 columnas la numeración
8 A 8 B 8 C 8 D 8 E 8 F 8 G 8 H 8 I
7 A 7 B 7 C 7 D 7 E 7 F 7 G 7 H 7 I
6 A 6 B 6 C 6 D 6 E 6 F 6 G 6 H 6 I
5 A 5 B 5 C 5 D 5 E 5 F 5 G 5 H 5 I
4 A 4 B 4 C 4 D 4 E 4 F 4 G 4 H 4 I
3 A 3 B 3 C 3 D 3 E 3 F 3 G 3 H 3 I
2 A 2 B 2 C 2 D 2 E 2 F 2 G 2 H 2 I
1 A 1 B 1 C 1 D 1 E 1 F 1 G 1 H 1 I

 Película que se emite
 Precio

Métodos
 Contructor   Cine ( filas, columnas, película, precio)
 String venderAsiento ( Espectador E)
    Asigna al espectador aleatoriamente en una posición libre de la sala
    Descuenta el precio de la película al dinero que posee el espectador
    Devuelve la cadena con la posición:  Ej- “Fila 5 asiento E”
    Devuelve NULL y imprime un mensaje de error si no hay asientos libres, si el espectador no posee dinero suficiente o si no tiene la edad mínima asignada a la película

void InformeSala()
  Muestra un listado de los espectadores y en que posiciones se sientan

int recaudación ()
   Devuelve el dinero recaudado por la película en función de los asientos ocupados.

La Película tienen los atributos  título, duración(minutos), edad mínima, genero.

El genero será un enumerado con los valores : drama, comedia, musical, aventuras, terror,  infantil.

El Espectador, nos interesa saber su nombre, edad y el dinero que tiene.



Realizaremos una pequeña simulación (TestCine), en el que generaremos muchos espectadores y les venderemos asientos
Solo se podrá sentar si tienen el suficiente dinero, hay espacio libre y tiene edad para ver la película, en caso de que el asiento este ocupado le buscamos uno libre.
Al final me tiene que mostrar donde están situados los espectadores y cual ha sido la recaudación mediante el método informeSala
La posición de los espectadores se muestra generado el siguiente informe.

  A B C D E F G H I
8
7           X X
6 X X
5     X X
4
3 X X X X
2             X X X
1

Película: Star wars episodio 572
N.º de espectadores:   13
Recaudación:           65  
Lista de espectadores
------------------------
Nombre            Asiento
Pepe Pérez        2G
Silvia Pérez      2H
...
