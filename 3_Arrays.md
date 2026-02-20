## 1. Arrays Unidimensionales (Vectores)
Un array (también llamado vector) es una estructura de datos que nos permite almacenar un conjunto de elementos del mismo tipo en posiciones de memoria contiguas.
Piénsalo como un archivador con un número fijo de cajones:
- El archivador es el array.
- Cada cajón es una posición o índice.
- Lo que guardas en cada cajón es el elemento.
- Todos los cajones guardan el mismo tipo de cosa (ej. todos guardan números enteros).

### Declaración e Inicialización (sin valores)
Para usar un array, debemos seguir dos pasos: declararlo y luego inicializarlo (reservar su espacio en memoria, ya que su tamaño es fijo).

```java

// 1. Declaración (Le decimos a Java que 'notas' será un array de enteros)
int[] notas;

// 2. Inicialización (Reservamos 5 espacios en memoria para 5 enteros, tamaño que no se puede cambiar después).
notas = new int[5]; 

// O todo en una línea (lo más común)
double[] precios = new double[10]; // Un array para 10 precios
```

### Inicialización con valores (Estática)
Si ya sabes qué valores va a contener, puedes inicializarlo directamente:

```java
// Java crea automáticamente un array de tamaño 4
String[] diasSemana = {"Lunes", "Martes", "Miércoles", "Jueves", "Viernes"}; 
```

### Acceso y Modificación (Índices)

Accedemos a cada "cajón" (elemento) usando su índice, que se escribe entre corchetes [].

¡Importante! Los índices en Java (y en la mayoría de lenguajes) empiezan siempre en 0.

Si un array tiene 5 elementos, sus índices van del 0 al 4.
- `notas[0]` es el primer elemento.
- `notas[4]` es el último elemento.

Para saber el tamaño de un array, usamos la propiedad `.length` (sin paréntesis).

### Recorriendo un array (Bucle for)

La forma más común y eficiente de "visitar" cada elemento de un array es usando un bucle for. Combinamos el bucle con la propiedad .length para que se repita la cantidad exacta de veces (tantas como elementos tenga el array).

```java
for (int i = 0; i < notas.length; i++) {
System.out.print(notas[i]);
}
```

### Recorriendo un array (Bucle for-each)

Existe una variante más moderna y legible del bucle for, conocida como for-each (o "bucle mejorado"). Esta estructura está diseñada específicamente para recorrer todos los elementos de un array, desde el primero hasta el último, sin necesidad de manejar contadores ni índices manualmente.

```java
double[] notas = {4.5, 8.0, 6.5, 9.0};

for (double nota : notas) {
//La variable 'nota' va tomando el valor de cada posición
System.out.print(nota + " ");
} 
```

### ¿Cuándo usar un bucle u otro?

Usa el for normal (con índice i) cuando:
- Necesitas saber la posición del elemento (por ejemplo, para decir "La nota del alumno 1 es...").
- Necesitas modificar el contenido del array (ej: notas[i] = 5;).
- No quieres recorrer el array completo (por ejemplo, solo la mitad inversa).

Usa el for-each cuando:
- Solo quieres leer todos los datos uno por uno.
- Quieres un código más limpio y evitar errores de "índice fuera de límites".

¡Ojo! En un bucle for-each, la variable temporal (ej. nota) es una copia del valor. Si modificas nota dentro del bucle, NO se modifica el array original. Para modificar el array, necesitas obligatoriamente el índice (i) del bucle for clásico.

## 2. Arrays Bidimensionales (Matrices)

Un array bidimensional es, simplemente, un "array de arrays". Nos sirve para representar datos en una cuadrícula (filas y columnas).
Piénsalo como un tablero de ajedrez o una hoja de cálculo.

### Declaración e Inicialización

Usamos dobles corchetes [][].
```java
// Declaración
int[][] tablero;

// Inicialización (3 filas, 4 columnas)
tablero = new int[3][4];

// Acceso (fila 1, columna 2) (Recuerda: índice 0)
tablero[1][2] = 100;

// Inicialización estática
int[][] matriz = {
    {1, 2, 3},  // Fila 0
    {4, 5, 6},  // Fila 1
    {7, 8, 9}   // Fila 2
};
```

### Recorrido de Matrices (Bucles anidados)

Para recorrer una matriz, necesitamos un bucle for anidado:
- El bucle exterior recorre las filas.
- El bucle interior recorre las columnas de cada fila.
```java
public class EjemploMatriz {
    public static void main(String[] args) {


        int[][] matriz = {
            {1, 2, 3},
            {4, 5, 6}
        };

        for (int i = 0; i < matriz.length; i++) {
            for (int j = 0; j < matriz[i].length; j++) {
                System.out.print("Posición [" + i + "][" + j + "] = " + matriz[i][j] + "\t");
            }
            System.out.println(); 
        }
    }
}
```
