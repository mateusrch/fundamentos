# Norma IEEE 754

- A norma IEEE 754 apresenta um padrão a ser seguido pelos fabricantes de computadores e pelas empresas reponsáveis pela construção de compiladores e linguagens científicas no que se refere ao uso da linguagem binária.

- Essa norma surgiu pela necessidade de condicionamento que geram erros indesejados por questões de armazenamento de dados numéricos, métodos de arredondamento, procedimentos de realização de operações aritméticas básicas (soma, subtração, divisão, multiplicação).

- Com o uso da norma IEEE 754, a precisão numérica para a representaçãode números reais é definida como sendo simples, dupla ou estendida.

- O conjunto de números reais pe formado pela união do conjunto dos números racionais e e conjunto de números irracionais.

- Um número racional é um número que pode ser expresso como a razão (ou fração) de dois números inteiros, onde o denominador é diferente de zero. Ou seja, um número racional pode ser escrito na forma \( \frac{a}{b} \), onde \( a \) e \( b \) são inteiros e \( b \neq 0 \). Exemplos de números racionais incluem 1/2, 3/4, 5, e -7 (pois -7 pode ser escrito como -7/1).

- Um número irracional, por outro lado, é um número que não pode ser expresso como a razão de dois números inteiros. Números irracionais têm uma expansão decimal que é não periódica e infinita, o que significa que eles não têm um padrão repetitivo nos seus dígitos. Exemplos de números irracionais incluem \( \pi \) (pi), \( \sqrt{2} \) (a raiz quadrada de 2) e o número \( e \) (a base dos logaritmos naturais).

Os computadores geralmente utilizam a base binária para a representação de números, isso acarreta em uma quantidade fixa de bits e, consequentemente, um conjunto finito de números que podem ser representados por meio de computadores.

## Notação científica normalizada

A mantissa (ou significando) em matemática refere-se à parte de um número que contém seus dígitos significativos. Na notação científica normalizada, um número é expresso na forma:

\[ N = M \times 10^E \]

Exemplo: *normalização científica*
- Manter 1 dpigito na mantissa
- 210,687 = 2,10687 x 10^2 *exemplo de normalização, deixando 1 digito antes da vírgula*
- 3242 = 3,242 x 10^3 *a virgula foi deslocada 3 casas para que a normalização ocorra*

Exemplo: *escrever na forma decimal os npumeros que estão na notação científica*
- 5,4323 x 10^5 = 5,4323 x 100000 = 543230

Onde:

- \( N \) é o número original.
- \( M \) é a mantissa (ou significando), um número decimal maior ou igual a 1 e menor que 10.
- \( E \) é o expoente, um número inteiro que indica a potência de 10 pela qual a mantissa é multiplicada.

A notação científica é útil para representar números muito grandes ou muito pequenos de uma maneira compacta e padronizada.

### Notação científica em Python
```py
a = 3242
print('%.10e' % a) # 3.2420000000+03

b = 0.23241
print('%.4e' % a) # 2.3241e-01, definindo 4 casas decimais.

# 0,0000054 = 5,4 x 10^-6
c = 0.0000054
print('%.4e' % c) # 5.4000e-06
```

- **quando o expoente for negativo, deslocamos a vírgula da direita para a esquerda**
- **quando o expoente for positivo, deslocamos a vírgula da esquerda para a direita.**

## Formas simples, dupla ou estendida

- Representação simples: **32 bits** em que *o primeiro bit está associado ao sinal* do número(0 para positivo e 1 para ngativo), *os 8 bits seguintes se referem ao expoente* que podem variar de **-126 até 127** e os **23 bits restantes correspondem a mantissa**.

| sinal | expoente | mantissa                |
|--------------------------------------------|
| 1     | 11111111 | 11111111111111111111111 |
