# arrayPermutation

## Definicion
Una permutación se puede especificar mediante un array P, donde P[i] representa la ubicación del elemento en i en la permutación. Por ejemplo, [2, 1, 0] representa la permutación donde se intercambian elementos en el índice 0 y 2.

Dada un array y una permutación, aplique la permutación al array. Por ejemplo, dado el array ["a", "b", "c"] y la permutación [2, 1, 0], devuelve ["c", "b", "a"].

## Soluciones

### Crear un nuevo array
La primera solución crea una nueva matriz de la misma longitud que la matriz original y asigna los valores de la matriz original en los índices especificados por la matriz de permutación. En [Strong-Typed Languages] (https://en.wikipedia.org/wiki/Strong_and_weak_typing) como Golang, necesitamos usar una matriz separada del tipo que debe devolverse para organizar la entrada y la salida.

Esta implementación se ejecuta en O(n) ya que necesita recorrer la matriz de permutación en su totalidad para establecer los índices correctamente. También incurrimos técnicamente en otro costo 0(n) para crear la nueva matriz, pero O(n) + O(n) se reduce a O(2n), por lo que aún lo consideramos O(n) complejidad.

La complejidad espacial de esta solución también es O(n), ya que creamos una matriz separada para contener todos los valores.

### Modificación de la matriz de permutación
En la segunda solución al problema, usamos la propia matriz de permutación y asignamos los valores apropiados en el índice de permutación de la primera matriz en la matriz de permutación.