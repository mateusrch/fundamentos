# Tópicos
- Estatistica descritiva(média, mediana, moda)
- Estatistica descritiva(variância, desvio-padrão)
- Probabilidade(conceitos de probabilidades, distribuição normal)
- Estatistica indutiva(amostrragem)
- Estatistica indutiva(confiança)

# Estatistica descritiva(media, moda, mediana)

**Média:** A média aritmética, comumente conhecida apenas como média, é um valor que representa a soma de todos os elementos de um conjunto de dados dividido pelo número de elementos desse conjunto. É uma medida de tendência central que mostra o valor central típico em um conjunto de dados. A fórmula para calcular a média é:

\[ \text{Média} = \frac{\sum_{i=1}^{n} x_i}{n} \]

onde \( x_i \) são os valores do conjunto de dados e \( n \) é o número total de valores.

**Moda:** A moda é o valor que aparece com mais frequência em um conjunto de dados. Em outras palavras, é o valor mais comum. Um conjunto de dados pode ter mais de uma moda (bimodal, trimodal, etc.) ou nenhuma moda se todos os valores aparecerem com a mesma frequência. A moda é especialmente útil para dados categóricos.

```go
package main

import (
	"fmt"
)

// Função para calcular a moda
func calculateMode(numbers []int) []int {
	// Criar um mapa para armazenar as frequências dos números
	frequency := make(map[int]int)

	// Contar a frequência de cada número
	for _, number := range numbers {
		frequency[number]++
	}

	// Determinar a frequência máxima
	maxFreq := 0
	for _, freq := range frequency {
		if freq > maxFreq {
			maxFreq = freq
		}
	}

	// Identificar a(s) moda(s)
	var modes []int
	for number, freq := range frequency {
		if freq == maxFreq {
			modes = append(modes, number)
		}
	}

	return modes
}

func main() {
	// Exemplo de uso
	numbers := []int{4, 1, 2, 2, 3, 4, 4, 5, 6, 6, 6}
	modes := calculateMode(numbers)
	fmt.Printf("A(s) moda(s) é(são): %v\n", modes)
}

```

**Mediana:** A mediana é o valor que separa a metade superior da metade inferior de um conjunto de dados ordenado. Se o número de valores no conjunto for ímpar, a mediana é o valor do meio. Se for par, a mediana é a média dos dois valores centrais. A mediana é uma medida de tendência central que é menos sensível a valores extremos (outliers) do que a média.

Para calcular a mediana:
1. Ordene os valores do conjunto de dados.
2. Se o número de valores \( n \) for ímpar, a mediana é o valor na posição \( \left(\frac{n+1}{2}\right) \).
3. Se \( n \) for par, a mediana é a média dos valores nas posições \( \left(\frac{n}{2}\right) \) e \( \left(\frac{n}{2} + 1\right) \).

Essas três medidas são usadas para descrever a tendência central de um conjunto de dados e cada uma tem suas próprias vantagens e aplicações dependendo do contexto dos dados.

```go
package main

import (
	"fmt"
	"sort"
)

// Função para calcular a mediana
func calculateMedian(numbers []float64) float64 {
	// Ordenar os números
	sort.Float64s(numbers)

	// Número de elementos
	n := len(numbers)

	// Calcular a mediana
	if n%2 == 1 {
		// Ímpar: a mediana é o valor do meio
		return numbers[n/2]
	} else {
		// Par: a mediana é a média dos dois valores centrais
		middle1 := numbers[(n/2)-1]
		middle2 := numbers[n/2]
		return (middle1 + middle2) / 2.0
	}
}

func main() {
	// Exemplo de uso
	numbers := []float64{7, 3, 1, 4, 6, 5, 2}
	median := calculateMedian(numbers)
	fmt.Printf("A mediana é: %.2f\n", median)
}

```

# Estatistica(Variância, desvio-padrão)
- **Variância Populacional:** A variância populacional mede a dispersão de um conjunto de dados em relação à média da população inteira. É calculada somando-se os quadrados das diferenças entre cada valor e a média, e dividindo-se pelo número total de valores na população.

A fórmula para a variância populacional (\(\sigma^2\)) é:
$$
\sigma^2 = \frac{\sum_{i=1}^{N} (x_i - \mu)^2}{N}
$$

onde:

- \( x_i \) são os valores do conjunto de dados.
- \( \mu \) é a média dos valores.
- \( N \) é o número total de valores na população.

- **Variância Amostral:** A variância amostral é usada quando se calcula a variância de uma amostra de uma população. É semelhante à variância populacional, mas para compensar o fato de estarmos lidando com uma amostra e não com a população inteira, dividimos pela quantidade de valores na amostra menos um.

A fórmula para a variância amostral (\(s^2\)) é:
$$
s^2 = \frac{\sum_{i=1}^{n} (x_i - \bar{x})^2}{n-1}
$$

onde:

- \( x_i \) são os valores do conjunto de dados.
- \( \bar{x} \) é a média dos valores da amostra.
- \( n \) é o número de valores na amostra.

```go
package main

import (
	"fmt"
)

// Função para calcular a média
func calculateMean(numbers []float64) float64 {
	sum := 0.0
	for _, number := range numbers {
		sum += number
	}
	return sum / float64(len(numbers))
}

// Função para calcular a variância populacional
func calculatePopulationVariance(numbers []float64) float64 {
	mean := calculateMean(numbers)
	sumOfSquares := 0.0
	for _, number := range numbers {
		difference := number - mean
		sumOfSquares += difference * difference
	}
	return sumOfSquares / float64(len(numbers))
}

// Função para calcular a variância amostral
func calculateSampleVariance(numbers []float64) float64 {
	mean := calculateMean(numbers)
	sumOfSquares := 0.0
	for _, number := range numbers {
		difference := number - mean
		sumOfSquares += difference * difference
	}
	return sumOfSquares / float64(len(numbers)-1)
}

func main() {
	// Exemplo de uso
	numbers := []float64{4, 1, 2, 2, 3, 4, 4, 5, 6, 6, 6}
	populationVariance := calculatePopulationVariance(numbers)
	sampleVariance := calculateSampleVariance(numbers)
	fmt.Printf("A variância populacional é: %.2f\n", populationVariance)
	fmt.Printf("A variância amostral é: %.2f\n", sampleVariance)
}

```

# Desvio padrão

- Nada mais é do que obter a raiz quadrada do resultado da variancia populacional ou amostral
- Caso a população seja pequena(30 itens ou menos) devo utilizar a formula da variacia amostral ao inves da populacional
- para obter um faixa de de resultados, somamos o desvio-padrao com a media e diminuimos a media do desvio-padrao

--- media + desvio padrão

--- media    a maior parte dos dados está dentro dessa faixa

--- media - desvio-padrao
