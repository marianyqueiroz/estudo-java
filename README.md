# Fundamentos da programação em Java

## Variáveis e tipos de dados

* **Frase:** string
    * Métodos:
        * `length()`: Obter o comprimento da string
        * `concat()`: Juntar duas strings
        * `equals()`: Comparar duas strings
        * `substring()`: Extrair uma substring
        * `contains()`: Verificar se uma string está em outra
        * `replace()`: Substituir uma string por outra
```java

class Main {
 public static void main(String[] args) {
  String valor = "Descomplica - Java";

  System.out.println(valor.contains("Java"));
  System.out.println(valor.length());
 }
}
```
* **Número inteiro:** `int`
* **Boleano:** `boolean`
* **Ponto flutuante:** `double`

## Entrada e saídas

* Escrita com quebra de linha: `System.out.printlm()`
* Escrita sem quebra de linha: `System.out.print()` ou `System.out.printf()`
* Saída: `System.in()`

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Métodos de saída
        System.out.println("Hello world!");
        System.out.print("Hello world!");
        System.out.printf("Hello world!");

        // Exemplo prático
        System.out.println("\nInforme seu nome");
        String palavras;
        Scanner entrada = new Scanner(System.in);
        palavras = entrada.next();

        System.out.println("Nome: " + palavras);
    }
}
```

# Operadores aritméticos

`+` soma
`-` subtração 
`*` multiplicação
`/` divisão
`%` módulo/resto da divisão

```java
class Main {
  public static void main(String[] args) {
    double numA, numB, total;
    //soma
    numA = 8;
    numB = 3;
    total = numA + numB;
    System.out.println(total);

    //multiplicação
    numA = 8;
    numB = 3;
    total = numA * numB;
    System.out.println(total);

    //subtração
    numA = 8;
    numB = 3;
    total = numA - numB;
    System.out.println(total);

    //divisão
    numA = 8;
    numB = 3;
    total = numA / numB;
    System.out.println(total);

    // resto da divisão
    numA = 8;
    total = numA % 2;
    System.out.println(total);
  }
}

//Exemplo prático
class Main {
  public static void main(String[] args) {
    double base, altura, area;

    base = 10;
    altura = 8;

    area = base * altura / 2;
    System.out.println(area);
  }
```






  


