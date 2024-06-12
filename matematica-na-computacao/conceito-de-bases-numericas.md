# Conceito

Bases numéricas são sistemas de contagem que utilizam diferentes conjuntos de símbolos para representar números. 
A **base 60**, conhecida como *hexagesinal* foi utilizada pelos Bbilônicos e ainda é usada hoje em unidades de tempo(60 segundos em 1 minutos, 60 minutos em 1 hora). A **base binária**, ou *sistema de base 2*, é fundamental para a computação e usa apenas os dígitos 0 e 1, representando a forma mais simples de armazenamento e processamento de dados por computadores.
A **base hexadecimal** ,ou *sistema de base 16*, utiliza os dígitos de 0 a 9 e as letras de A a F, facilitando a representação compacta de grandes números binários, como endereços de memória e cores.

| Base Numérica | Nome             | Símbolos Utilizados                        | Exemplos de Uso                          |
|---------------|------------------|--------------------------------------------|------------------------------------------|
| Base 2        | Binária          | 0, 1                                       | Computação, eletrônica                   |
| Base 16       | Hexadecimal      | 0-9, A-F                                   | Programação, endereçamento de memória    |
| Base 60       | Sexagesimal      | 0-59                                       | Unidades de tempo, divisão de ângulos    |
| Base 360      | Sistema circular | 1-360                                      | Geometria, astronomia                    |

# Base binária

- A base binária é um sistema posicional de nueração que conta com dois símbolos, *0* e *1*. 
- Representação de números decimais, binários e bytes.

| Decimal | Binário | Byte     |
|---------|---------|----------|
| 0       | 0       | 00000000 |
| 1       | 1       | 00000001 |
| 2       | 10      | 00000010 |
| 3       | 11      | 00000011 |
| 4       | 100     | 00000100 |
| 5       | 101     | 00000101 |
| 6       | 110     | 00000110 |

## Conversão de número binário em decimal
1. Obter o número binário a ser convertido.
2. A cada dígito, da direita para a esquerda, escrevemos as respectivas potências da base b=2 com os expoentes variando de 0, 1, 2 e assim por diante, ou seja,2°, 2¹, 2² ... 
3. Multiplicamos os dígitos pelas respectivas potências e somamos os resultados.
4. O número obtido é o decimal equivalente ao número binário.

Exemplo:

- Número binário **110101**.
- N = (1 * 2⁵)+(1 * 2⁴)+(0 * 2³)+(1 * 2²)+(0 * 2¹)+(1 * 2°)
- N = (1 * 32)+(1 * 16)+(0 * 8)+(1 * 4)+(0 * 2)+(1 * 1)
- N = 32 + 16 + 0 + 4 + 0
- N = 53

# Conversão de número Decimal para binário

1. Obter o número decimal a ser convertido.
2. Dividir o número por 2 e anotar o *quociente* e o *resto*.
3. Anotar o resto. Este será o dígito binário menos significativo (o último dígito).
4. Atualizar o número a ser dividido, utilizando o quociente obtido na divisão anterior.
5. Repetir os passos 2 a 4 até que o quociente seja 0.
6. Os restos anotados em cada passo, lidos de baixo para cima, formam o número binário.

Exemplo:

- Número decimal **25**.
- 25 ÷ 2 = 12(quociente), resto 1
- 12 ÷ 2 = 6(quociente), resto 0
- 6 ÷ 2 = 3(quociente), resto 0
- 3 ÷ 2 = 1(quociente), resto 1
- 1 ÷ 2 = 0(quociente), resto 1

### Os 6 restos resultantes das divisões, anotados de trás para frente **11001** é o quivalente ao decimal 25.
| Divisão | Quociente | Resto |
|---------|-----------|-------|
| 25 ÷ 2  | 12        | 1     |
| 12 ÷ 2  | 6         | 0     |
| 6 ÷ 2   | 3         | 0     |
| 3 ÷ 2   | 1         | 1     |
| 1 ÷ 2   | 0         | 1     |

# Base Hexadecimal

A base numérica hexadecimal é um sistema posicional em que a base é 16. Para a representação de números hexadecimais são utilizados os símbolos **0, 1, 2, 3, 4, 5, 6, 7, 8, 9**, **A, B, C, D, E**, e **F**. A base hexadecimal é uma representação compácta do número binário.

O número decimal **1504** precisa de 11 dígitos para ser representado na forma **binária(10111100000)** e de apenas 3 dígitos para ser representado na forma **hexadecimal(5e0)**.
| Decimal | Hexadecimal |
|---------|-------------|
| 0       | 0           |
| 1       | 1           |
| 2       | 2           |
| 3       | 3           |
| 4       | 4           |
| 5       | 5           |
| 6       | 6           |
| 7       | 7           |
| 8       | 8           |
| 9       | 9           |
| 10      | A           |
| 11      | B           |
| 12      | C           |
| 13      | D           |
| 14      | E           |
| 15      | F           |
| 16      | 10          |
| 17      | 11          |
| 18      | 12          |
| 19      | 13          |
| 20      | 14          |
| 21      | 15          |
| 22      | 16          |
| 23      | 17          |
| 24      | 18          |
| 25      | 19          |
| 26      | 1A          |
| 27      | 1B          |
| 28      | 1C          |
| 29      | 1D          |
| 30      | 1E          |

## Conversão de um número hexadecimal em número decimal:

1. Obter o número decimal a ser convertido.
2. Transformar cada dígito **A, B, C, D, E** e **F** para o respectivo decimal.
3. Para cda dígito da *DIRETA* para a *ESQUERDA* escrever as respectivas potências da **base b=16** com os expoentes variando de 0, 1, 2, 3, 4 e assim por diante, ou seja, **16°, 16¹, 16², 16³** ...
4. Multiplicar os dígitos pelas suas respectivas potências somando os resultados.
5. O número obtido é o número decimal equivalente ao número hexadecimal.


Exemplo:

- Número hexadecimal **2e5c**.
- 2 14 5 12
- N = (2 x 16³) + (14 x 16²) + (5 x 16¹) + (12 x 16°)
- N = (2 x 4096) + (14 x 256) + (5 x 16) + (12 x 1)
- N = 8192 + 3584 + 80 + 12
- N = 11868

O número 11868 é o número decimal equivalente ao número hexadecimal 2e5c.

## Conversão de um número decimal em hexadecimal
1. Obter o número decimal.
2. Dividir o número decimal pelo valor da base hexadecimal (16):
3. Divida 11868 por 16. O quociente será usado para a próxima divisão.
4. Registrar o resto da divisão:
5. O resto da divisão de 11868 por 16 é 12 (correspondente ao dígito hexadecima C).
6. Continue dividindo o quociente pelo valor da base (16) até que o quociente seja zero. Registre os restos da divisão em ordem inversa.

- N = O número decimal é 11868
- N = 11868 ÷ 16 = 741(quociente) + 12(resto, C)
- N = 741 ÷ 16 = 46(quociente) + 5(resto, 5)
- N = 46 ÷ 16 = 2(quociente) + 14(resto, E)
- N = 2 ÷ 16 = 0(quociente) + 2(resto, 2)
 
Converter os restos em dígitos hexadecimais:
Os restos são 12, 5, 14 e 2. Em hexadecimal, eles correspondem a C, 5, E e 2, respectivamente.

Concatene os dígitos hexadecimais na ordem inversa em que foram obtidos. Isso nos dá o equivalente hexadecimal do número decimal.

Então, 11868 em decimal é igual a 2E5C em hexadecimal.

# Aritimética Binária

A soma de números binários segue o mesmo princípio da soma de números decimais, porem como só temos 2 símbolos(0 e 1) 1 + 1 = 1 seguido de 0.

Exemplo: 1001 + 0101 = 1110

Precisamos considerar que em um sistema com 8 bits, não seria possível somar 10000000 + 10000000, sendo necessário 9 bits para armazenar o número obtido, ultrapassando o limite do sistema, causando inconsistências no valor.

  10000000 + 10000000 = 100000000

Porem como o sistema é 8 bits o valor armazenado será os primeiros 8 dígitos da direita para a esquerda resultando no valor 00000000 ao invés de 100000000.

## Representação de números binários negativos

### Complemento de um(gera problemas)
1. Utiliza a primeira posição de um conjunto de bits para indicar se o número é positivoou negatvo.
2. Se o número for positivo o primeiro caractere do conjunto será 0, se o número for negativo o primeiro catactere será 1.

### Complemento de dois
1. Obter o respectivo binário positivo
2. Inverter cada bit, ou seja, no lugar de 0 trocar por 1 e no lugar do 1 trocar por 0.
3. Somar 1 ao resultado.

Exemplo:

- obter o binário de -4
- 00000100
- 11111011
- 11111011 + 1 = 11111100

calculo final:
  11111011 + 1 = 11111100

### Subtração de binários
Exemplo 5 - 4:
- Primeiro passo inverter o valor de 4 para -4
- somar os dois binários

A soma de um bínario positivo com um binário negativo é correspondente a 5+(-4) da forma decimal.

calculo final:
00000101 + 11111100 = 00000001

00000001 é a representação binária de 1 decimal.
