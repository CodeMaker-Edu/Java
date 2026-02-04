# Bloque 2 - Estructuras de control

## Concepto
Las estructuras de control permiten **modificar el flujo de ejecución** de un programa.
Con ellas podemos:
- Ejecutar instrucciones de forma secuencial.
- Tomar decisiones (selección).
- Repetir bloques de código (iteración).
- Alterar el flujo con saltos.

Según el teorema de la estructura, todo programa puede construirse únicamente con:
- **Secuencia**: instrucciones ejecutadas en orden.
- **Selección**: permite bifurcaciones en función de condiciones.
- **Iteración**: repite un bloque de instrucciones.

## Operadores

Los operadores son símbolos que indican una operación a realizar sobre uno o varios valores, muy utilizados habitualmente para comprobar condiciones.

### Operadores de comparación
- `==` → igual que  
- `!=` → distinto que  
- `>`  → mayor que  
- `<`  → menor que  
- `>=` → mayor o igual que  
- `<=` → menor o igual que 

### Operadores lógicos

- `&&` → AND (true si ambas condiciones son verdaderas)
- `||` → OR (true si al menos una condición es verdadera)
- `!` → NOT (niega la condición)

## Estructuras condicionales en Java

### Condicional simple – `if`

Cuando solo queremos comprobar si se cumple una condición para realizar una acción.

```java
if (condición) {
   // sentencias si se cumple
}
```

### Condicional doble – `if-else`

Cuando queremos realizar una acción si se cumple la condición, y otra acción si no se cumple.

```java
if (condición) {
   // sentencias si es verdadera
} else {
   // sentencias si es falsa
}
```
### Condicional múltiple - `if - else if - else`

Cuando queremos realizar diferentes acciones en función del resultado de la condición.

```java
if (condición) {
    // sentencias si es verdadera
} else if (otra condición) {
    // sentencias si es verdadera esta otra condicion
} else {
    // sentencias si es falsa
}
```

### Condicinoal múltiple – `switch`

Permite múltiples caminos de ejecución en función del valor que tenga una variable. Similar al `if - else if - else`, pero aquí no se compara (no hay símbolos `<`, `>`, `==`, etc.), solo se mira qué hay en la variable y en cada caso se realiza una acción.

```java
switch (variable) {
   case valor1:
      // sentencias
      break;
   case valor2:
      // sentencias
      break;
   default:
      // sentencias por defecto
}
```

### Operador ternario

Es una forma compacta de hacer un if-else.

```java
variable = (condición) ? valor_si_verdadero : valor_si_falso;
```

## Estructuras iterativas (bucles)

### Bucle `while`

Se trata de un bucle que se repite mientras se cumpla una determinada condición. Deja de repetirse la instrucción cuando la condición deje de repetirse.


```java
while (condición) {
   // sentencias
}
```

### Bucle `do-while`

Exactamente igual que el bucle `while`, con la única diferencia de que primero ejecuta la instrucción que tiene en su interior, y después comprueba si la condición se cumplía. Esto asegura que las instrucciones internas se ejecuten al menos una vez.

```java
do {
   // sentencias
} while (condición);
```

### Bucle `for`

Se usa cuando se conoce el número de iteraciones (repetir x veces).

```java
for (inicialización; condición; actualización) {
   // sentencias
}
```

### Sentencias de salto

Un bucle, e incluso otras estructuras, pueden interrumpirse con las siguientes instrucciones:

- `break` → interrumpe un bucle o switch.
- `continue` → salta a la siguiente iteración del bucle.
- `return` → devuelve un valor y finaliza un método (este lo veremos más adelante).
- `goto` → manda la ejecución del código a otra parte, pero su uso está ya obsoleto y desaconsejado.


### Equivalencias entre bucles

Todos los bucles (while, do-while, for) son equivalentes en potencia. Es decir, un mismo problema podrá resolverse con diferentes bucles. Se recomienda elegirlos según el problema:
- `for` → número de iteraciones conocido.
- `while` → número de repeticiones indeterminado.
- `do-while` → número de repeticiones indeterminado y debe ejecutarse al menos una vez.
