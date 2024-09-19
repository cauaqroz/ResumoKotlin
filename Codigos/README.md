## Conceitos Básicos em Kotlin

#### Multiplicação de dois números
```kotlin
fun main() {
    // Lê dois números fornecidos pelo usuário
    val num1 = readLine()!!.toDouble() 
    val num2 = readLine()!!.toDouble()

    // Calcula a multiplicação dos números
    val multiplicacao = num1 * num2

    // Imprime o resultado
    println("A multiplicação de $num1 e $num2 é: $multiplicacao") 
}
```

#### Conversão de Celsius para Fahrenheit
```kotlin
fun main() {
    // Lê a temperatura em Celsius
    val celsius = readLine()!!.toDouble()

    // Converte para Fahrenheit usando a fórmula
    val fahrenheit = (9 * celsius + 160) / 5

    // Imprime o resultado
    println("$celsius graus Celsius equivalem a $fahrenheit graus Fahrenheit")
}
```
#### Fatorial em Kotlin
```kotlin
fun fatorial(n: Int): Long {
    if (n < 0) {
        throw IllegalArgumentException("Numero Negativo.")
    }
    return if (n == 0) 1 else (1..n).reduce { acc, i -> acc * i }
}

fun main() {
    val numero = 5
    val fatorial = fatorial(numero)
    println("O fatorial de $numero é $fatorial") 
}
```
#### Multiplicação de dois números
```kotlin
fun main() {
    // Lê dois números fornecidos pelo usuário
    val num1 = readLine()!!.toDouble() 
    val num2 = readLine()!!.toDouble()

    // Calcula a multiplicação dos números
    val multiplicacao = num1 * num2

    // Imprime o resultado
    println("A multiplicação de $num1 e $num2 é: $multiplicacao") 
}
```

## Condicionais e Loops em Kotlin

#### Ordenação de três números
```kotlin
fun main() {
    // Lê três números inteiros
    val num1 = readLine()!!.toInt()
    val num2 = readLine()!!.toInt()
    val num3 = readLine()!!.toInt()

    // Cria uma lista com os números e a ordena
    val numeros = listOf(num1, num2, num3)
    val numerosOrdenados = numeros.sorted()

    // Imprime os números ordenados
    println("Números em ordem crescente: $numerosOrdenados")
}
```

#### Cálculo da média e aprovação
```kotlin
fun main() {
    // Lê as quatro notas
    val nota1 = readLine()!!.toDouble()
    val nota2 = readLine()!!.toDouble()
    val nota3 = readLine()!!.toDouble()
    val nota4 = readLine()!!.toDouble()

    // Calcula a média
    val media = (nota1 + nota2 + nota3 + nota4) / 4

    // Verifica se o aluno foi aprovado e imprime a mensagem correspondente
    if (media >= 7) {
        println("Aprovado! Média: $media")
    } else {
        println("Reprovado. Média: $media")
    }
}
```
##  Funções em Kotlin

#### Menu de opções com funções
```kotlin
fun main() {
    while (true) {
        // Exibe o menu de opções
        println("\nEscolha uma opção:")
        println("1 - Fatorial")
        println("2 - Quadrado de um número")
        println("3 - Volume de uma lata")
        println("4 - Sair")

        // Lê a opção escolhida pelo usuário
        val opcao = readLine()!!.toInt()

        // Executa a ação correspondente à opção escolhida
        when (opcao) {
            1 -> calcularFatorial()
            2 -> calcularQuadrado()
            3 -> calcularVolumeLata()
            4 -> break // Sai do loop e encerra o programa
            else -> println("Opção inválida!")
        }
    }
}

fun calcularFatorial() {
    // Implementação da função para calcular o fatorial
    println("Calculando fatorial...")
}

fun calcularQuadrado() {
    // Implementação da função para calcular o quadrado de um número
    println("Calculando quadrado...")
}

fun calcularVolumeLata() {
    // Implementação da função para calcular o volume de uma lata
    println("Calculando volume da lata...")
}
```

##  Coleções em Kotlin

#### Criação e exibição de uma coleção
```kotlin
fun main() {
    // Cria uma lista mutável e adiciona elementos de 1 a 10
    val numeros = mutableListOf<Int>()
    for (i in 1..10) {
        numeros.add(i)
    }

    // Imprime a lista
    println(numeros)
}
```

#### Criação de coleções e manipulação de elementos
```kotlin
fun main() {
    // Cria a coleção A com elementos de 1 a 10
    val colecaoA = List(10) { it + 1 } 

    // Cria a coleção B com elementos da coleção A multiplicados por 2
    val colecaoB = colecaoA.map { it * 2 }

    // Imprime ambas as coleções
    println("Coleção A: $colecaoA")
    println("Coleção B: $colecaoB")
}
```

## Classes em Kotlin

#### Classe ContaCorrente

```kotlin
class ContaCorrente(val numeroConta: Int, val nomeCliente: String, val cpf: String, var saldo: Double) {

    // Método para exibir os dados da conta
    fun exibirDados() {
        println("Número da Conta: $numeroConta")
        println("Nome do Cliente: $nomeCliente")
        println("CPF: $cpf")
        println("Saldo: $saldo")
    }
}

fun main() {
    // Cria uma instância da classe ContaCorrente
    val conta = ContaCorrente(12345, "João Silva", "123.456.789-00", 1000.0)

    // Chama o método para exibir os dados da conta
    conta.exibirDados()
}
```

## Lambdas em Kotlin

####  Exemplo de função anônima

```kotlin
fun main() {
    // Define uma função anônima que calcula o dobro de um número
    val dobrar: (Int) -> Int = { numero -> numero * 2 }

    // Chama a função anônima
    val resultado = dobrar(5) 
    println(resultado) // Saída: 10
}
```

####  Exemplo de filter
```kotlin
fun main() {
    val numeros = listOf(1, 2, 3, 4, 5, 6)

    // Filtra os números pares da lista
    val numerosPares = numeros.filter { it % 2 == 0 }
```





