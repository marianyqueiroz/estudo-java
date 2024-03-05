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
* Maior que `>`
* Menor que `<`
* Igual `==`
* Diferente de `!=`
* Maior ou igual a `>=`
* Menor ou igual a `<=`
* E `&&`
* Ou `||`
* Negação `!`

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

# Estrutura de repetição
## For

```
public class Main {
  public static void main(String[] args) {
    //repetição
    for(int cont = 0; cont < 10; cont++){
      System.out.println("oi");
    }

    //repetição com o valor
    for(int cont = 0; cont < 10; cont++){
      System.out.println("oi " + cont);
    }

    //Números de 5 a 20
    for(int cont = 5; cont <= 20; cont++){
      System.out.println("Números de 5 a 20 " + cont);
    }
  }
}
```

## While
Enquanto for true, a estrutura de repetição em questão irá executar.

```
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
    int opcao = 0;
    while(opcao != 99){
      System.out.println("Digite um valor qualquer, ou 99 para sair.");
      Scanner entrada = new Scanner(System.in);
      opcao = entrada.nextInt();
    }
  }
}
```

### Do / While

```
import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
   int opcao;

    do{
      System.out.println("Digite o valor 99 para sair");
      Scanner entrada = new Scanner(System.in);
      opcao = entrada.nextInt();
    } while(opcao != 99);
  }
}
```

## Estrutura de repetição aninhada

```
public class Main {
  public static void main(String[] args) {
    for(int i = 0; i <= 10; i++)
      for(int j = 0; j <= 10; j++)
        System.out.println(i + " x " + j + " = " + (i*j));
  }
}

//i   j
//1 x 0 = 0 
//1 x 1 = 1
//1 x 2 = 2
```

## Método
O método é um bloco de código que executa uma tarefa específica
*Exemplo
 - `class`: dar forma/gerar o objeto;
 - `public`: modificador de acesso.

```
public class Main {
  public static int  somar(int a, int b){
    return (a+b);
  }
  public static void main(String[] args) {
    int total = Main.somar(10, 50);
    System.out.println(total);
  }
}
```
# Vetores e Matrizes
## Vetor
O vetor é nada mais do que uma varável que guarda vários valores, como se fosse um prédio com vários andares.
```
public class Main {
  public static void main(String[] args) {
    int valor;
    int[] dados = new int[5];

    dados[2] = 9;
    dados[3] = 7;
    dados[0] = 6;

    System.out.println(dados[3]);
    System.out.println(dados[2]);
    System.out.println(dados[0]);
    System.out.println(dados);
  }
}
```

## Matriz
```
public class Main {
  public static void main(String[] args) {
    int valor;
    int[][] dados = new int[3][3];

    for(int i=0; i<3; i++)
        for(int j=0; j<3; j++)
          System.out.println(dados[i][j] = j);
  }
}
```

### Exemplo prático
```
public class Main {
  public static void main(String[] args) {
    int[] passarosPorDia = {2, 5, 0, 7, 4, 1, 3, 0, 2, 5, 0, 1, 2, 1};

    int totalPassaros = 0;
    int passarosPrimeiraSemana = 0;
    int passarosSegundaSemana = 0;

    // Total de pássaros
    for(int i = 0; i < 14; i++){
      totalPassaros = totalPassaros + passarosPorDia[i];
    }
    System.out.println("Total de pássaros: " + totalPassaros);

    // Total de pássaros na primeira semana
    for(int i = 0; i < 7; i++){
      passarosPrimeiraSemana = passarosPrimeiraSemana + passarosPorDia[i];
    }
    System.out.println("Total de pássaros na primeira semana: " + passarosPrimeiraSemana);

    // Total de pássaros na segunda semana
    for(int i = 7; i < 14; i++){
      passarosSegundaSemana = passarosSegundaSemana + passarosPorDia[i];
    }
    System.out.println("Total de pássaros na segunda semana: " + passarosSegundaSemana);
  }
}
```

## Matriz
```
public class Main {
  public static void main(String[] args) {
    int [][] matriz = {{9,8,7}, {5,3,2}, {6,6,7}};

    int[] maiorLinha = new int[3];
    int[] menorColuna = new int[3];

    for(int i=0; i<3; i++)
      maiorLinha[i] = 0;

    for(int i=0; i<3; i++)
      menorColuna[i] = 10;

    // Maior elemento na linha 0
    for(int i=0; i<3; i++)
      if(matriz[0][i] > maiorLinha[0])
        maiorLinha[0] = matriz[0][i];

    // Maior elemento na linha 1
    for(int i=0; i<3; i++)
      if(matriz[1][i] > maiorLinha[1])
        maiorLinha[1] = matriz[1][i];

    // Maior elemento na linha 2
    for(int i=0; i<3; i++)
      if(matriz[2][i] > maiorLinha[2])
        maiorLinha[2] = matriz[2][i];

    // Menor elemento na coluna 0
    for(int i=0; i<3; i++)
      if(matriz[i][0] < menorColuna[0])
        menorColuna[0] = matriz[i][0];

    // Menor elemento na coluna 1
    for(int i=0; i<3; i++)
      if(matriz[i][1] < menorColuna[1])
        menorColuna[1] = matriz[i][1];

    // Menor elemento na coluna 2
    for(int i=0; i<3; i++)
      if(matriz[i][2] < menorColuna[2])
        menorColuna[2] = matriz[i][2];

    for(int i=0; i<3; i++)
      for(int j=0; j<3; j++)
        if(maiorLinha[i] == menorColuna[j])
          System.out.println("O ponto de sela é: " + maiorLinha[i]);
  }
}
```

# List e ArrayList
Equanto em um vetor precisamos declarar o tamanho, no array list não precisamos.
## Métodos 
* Para adicionar itens em uma lista
```
estados.add("Pernambuco");
```

* Para remover itens de uma lista
```
estados.remove("São Paulo");
```

* Para verificar se existe algum item
```
estados.contains("Amazonas");
```





  


