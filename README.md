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

* Soma `+` 
* Subtração `-`  
* Multiplicação `*` 
* Divisão `/` 
* Módulo/resto da divisão `%` 

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
# Estruturas Condicionais
## Operadores Lógicos
`>`: Maior que
`<`: Menor que
`==`: Igual
`!=`: Diferente de
`>=`: Maior ou igual a
`<=`: Menor ou igual a
`&&`: E
`||`: Ou
`!`: Negação

```
public class Main {
  public static void main(String[] args) {
    int a, b;
    a = 4;
    b = 8;

    System.out.println(a > b);  
    //Resposta: false
    System.out.println(a > b || b == 8);
    //Resposta: true
    System.out.println(a > b && b == 8);
    //Resposta: false
  }
}
```
## Estrutura condicional simples

```
public class Main {
  public static void main(String[] args) {
    //Notas de faculdade
    int nota = 6;

    if(nota >= 5){
      System.out.println("O aluno está provado");          
      System.out.println("Parabéns!");
    }
  }
}
```
## Estrutura condicional composta

```
public class Main {
  public static void main(String[] args) {
    //int nota = 6;
    int nota = 2;

    if(nota >= 5){
      System.out.println("O aluno foi aprovado");
    } else {
      System.out.println("O aluno foi reprovado");  
    }
  }
}
```

## Estrutura condicional aninhada

```
public class Main {
  public static void main(String[] args) {
    //int nota = 6;
    //int nota = 4;
    int nota = 2;

    if( nota >= 5 ){
      System.out.println("O aluno foi aprovado");
    } else if( nota > 3 && nota < 5 ){
      System.out.println("O aluno está de recuperação");
    } else {
      System.out.println("O aluno foi reprovado");
    }
  }
}
```

## Estrutura de múltipla escolha

```
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    Scanner entrada = new Scanner(System.in);
    System.out.println("Escolha uma opção: ");
    System.out.println("1 - Cadastro de Aluno: ");
    System.out.println("2 - Cadastro de Nota: ");
    System.out.println("3 - Listar Aluno e Nota");

    int numero = entrada.nextInt();

    switch(numero){
      case 1:
        System.out.println("Vamos cadastrar o aluno");
      break;
      case 2:
        System.out.println("Camos cadastrar a nota");
      break;
      case 3:
        System.out.println("Listar aluno e nota");
      break;
      default:
        System.out.println("O número é inválido");
    }
  }
}
```

```
//Exemplo prático
import java.util.Scanner;
import java.util.Random;

public class Main {
  public static void main(String[] args) {
    Random gerador = new Random();
    int x = gerador.nextInt(100);

    Scanner entrada = new Scanner(System.in);
    System.out.println("Adivinhe o número que estou pensando");
    int numero = entrada.nextInt();

    if( numero == x ){
      System.out.println("Parabéns, você acertou! Eu pennsei no " + x);
    } else {
      System.out.println("Você errou! Eu pensei no " + x);
    }
  }
}
```





  


