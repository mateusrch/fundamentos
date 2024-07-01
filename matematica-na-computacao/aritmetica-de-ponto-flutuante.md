# Soma
-  Nesse exemplo como os expoentes são iguais, eu mantenho a base com os expoentes e somo a mantissa.

1. a+b = 2,3421 x 10² + 3,5154 x 10²
2. a+b = (2,3421 + 3,5154) x 10²
3. a+b = 5,8575 x 10²

- Nesse exemplo os expoentes são diferentes, então preciso deixa-los iguais, **sempre preciso elevar o menor expoente até ele ficar igual o maior**, lembrando que a virgula vai deslocando conforme o expoente vai alterando.

1. a+b = 2,3421 x 10^2 + 3,5154 x 10^4
2. a+b = 0,023421 x 10^4 + 3,5154 x 10^4  
3. a+b = (0,02342 + 3,5154) x 10^4
4. a+b = 3,538821 x 10^4

# subtração

-  Nesse exemplo como os expoentes são iguais, eu mantenho a base com os expoentes e subtraio a mantissa.

1. a-b = 2,3421 x 10^2 - 3,5154 x 10^2
2. a-b = (2,3421 - 3,5154) x 10^2
3. a-b = -1,1733 x 10^2

# Multiplicação

-  Nesse exemplo como os expoentes são iguais, eu mantenho a base com os expoentes e multiplico a mantissa e somo os expoentes.

1. a.b = (2,3421 . 10^2) . (3,5154 . 10^2)
2. a.b = (2,3421 . 3,5154) x (10^2 + 10^2)
3. a.b = 8,23341834 x 10^4

# Divisão

-  Nesse exemplo como os expoentes são iguais, eu mantenho a base com os expoentes e multiplico a mantissa e subtrair os expoentes.

1. a.b = (2,3421 x 10^2) / (3,5154 x 10^2)
2. a.b = (2,3421 / 3,5154) x (10^2 / 10^2)
3. a.b = 0,66623997269 x 10^0 *preciso normalizar: precisa ficar 1 dígito antes da virgula*
4. a.b = 6,6623997269 x 10^-1

Exemplo em python:
```py
a=2.3421
b=3.5154
c=a/b
print('%.10e' % c) #  6,6623997269e-01
```