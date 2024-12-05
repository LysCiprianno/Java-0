## Lógica de Programação Básica em Java

 1 - Baby Steps

Pergunta:  
Escreva um programa em Java e crie uma variável chamada "Planeta" e atribua-a um valor "Plutão". Exiba o valor para o usuário.

```java
public class Main {
    public static void main(String[] args) {
        String Planeta = "Plutão";
        System.out.println(Planeta);
    }
}



2 - Hello Clarice
Pergunta: 
Escreva um programa em Java em que o usuário informe o seu nome e exiba a mensagem "Olá, [NomeDoUsuario]".

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Qual é o seu nome? ");
        String nome = scanner.nextLine();
        
        System.out.println("Olá, " + nome);
    }
}



3 - A Bit of Information
Pergunta:
Escreva um programa em Java em que o usuário informe o seu nome e em seguida o programa perguntará a idade do usuário. Agora o programa deve exibir a mensagem "Olá, [NomeDoUsuario], sua idade é [idade]".

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Qual é o seu nome? ");
        String nome = scanner.nextLine();
        
        System.out.print("Qual é a sua idade? ");
        int idade = scanner.nextInt();
        
        System.out.println("Olá, " + nome + ", sua idade é " + idade);
    }
}



4 - 1, 2 e 3
Pergunta:
Faça um programa que leia um valor informado pelo usuário e diga se o valor informado é positivo, negativo ou neutro.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Digite um número: ");
        int numero = scanner.nextInt();
        
        if (numero > 0) {
            System.out.println("O número é positivo.");
        } else if (numero < 0) {
            System.out.println("O número é negativo.");
        } else {
            System.out.println("O número é neutro.");
        }
    }
}



5 - Qual o maior?
Pergunta:
Faça um programa para ler 3 valores (considere que não serão informados valores iguais) e escrever o maior deles.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Digite o primeiro valor: ");
        int a = scanner.nextInt();
        
        System.out.print("Digite o segundo valor: ");
        int b = scanner.nextInt();
        
        System.out.print("Digite o terceiro valor: ");
        int c = scanner.nextInt();
        
        int maior = a;
        if (b > maior) maior = b;
        if (c > maior) maior = c;
        
        System.out.println("O maior valor é: " + maior);
    }
}



5.1 - Qual o maior? (4 vezes pior)
Pergunta:
Faça um programa para ler 4 valores (considere que não serão informados valores iguais) e escrever o maior deles.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Digite o primeiro valor: ");
        int a = scanner.nextInt();
        
        System.out.print("Digite o segundo valor: ");
        int b = scanner.nextInt();
        
        System.out.print("Digite o terceiro valor: ");
        int c = scanner.nextInt();
        
        System.out.print("Digite o quarto valor: ");
        int d = scanner.nextInt();
        
        int maior = a;
        if (b > maior) maior = b;
        if (c > maior) maior = c;
        if (d > maior) maior = d;
        
        System.out.println("O maior valor é: " + maior);
    }
}




6 - Qual o quê?
Pergunta:
Faça um programa que leia 3 valores (considere que não serão informados valores iguais) e escrever a soma dos 2 maiores.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Digite o primeiro valor: ");
        int a = scanner.nextInt();
        
        System.out.print("Digite o segundo valor: ");
        int b = scanner.nextInt();
        
        System.out.print("Digite o terceiro valor: ");
        int c = scanner.nextInt();
        
        int[] valores = {a, b, c};
        java.util.Arrays.sort(valores);
        
        System.out.println("A soma dos dois maiores valores é: " + (valores[1] + valores[2]));
    }
}



6.1 - 5 vezes?
Pergunta:
Faça um programa que leia 5 valores (considere que não serão informados valores iguais) e escrever a soma dos 2 maiores.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        int[] valores = new int[5];
        
        for (int i = 0; i < 5; i++) {
            System.out.print("Digite o " + (i + 1) + "º valor: ");
            valores[i] = scanner.nextInt();
        }
        
        java.util.Arrays.sort(valores);
        
        System.out.println("A soma dos dois maiores valores é: " + (valores[3] + valores[4]));
    }
}



7 - Enquanto isso
Pergunta:
Faça um programa para ler 2 valores informados pelo usuário e se o segundo valor informado for neutro, deve ser lido um novo valor - ou seja, para o segundo valor não pode ser aceito o valor zero nem um valor negativo. O programa deve imprimir o resultado da divisão do primeiro valor lido pelo segundo valor lido.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Digite o primeiro valor: ");
        double a = scanner.nextDouble();
        
        double b;
        do {
            System.out.print("Digite o segundo valor (não pode ser zero ou negativo): ");
            b = scanner.nextDouble();
        } while (b <= 0);
        
        System.out.println("Resultado da divisão: " + (a / b));
    }
}



8 - Cansar de Digitar
Pergunta:
Faça um programa que leia 10 valores informados pelo usuário, calcule, exiba os números informados e escreva a média aritmética desses valores lidos.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        double soma = 0;
        
        for (int i = 0; i < 10; i++) {
            System.out.print("Digite o " + (i + 1) + "º valor: ");
            double valor = scanner.nextDouble();
            soma += valor;
        }
        
        System.out.println("Os valores digitados foram: ");
        for (int i = 0; i < 10; i++) {
            System.out.print(soma / 10 + " ");
        }
        
        System.out.println("\nA média aritmética é: " + (soma / 10));
    }
}



9 - Parabéns
Pergunta:
Escreva um programa para ler as notas das 4 avaliações de um aluno no semestre, calcular e escrever a média do semestre e a seguinte mensagem: PARABÉNS! Você foi aprovado! somente se o aluno foi aprovado (considere 6.0 a média mínima para aprovação e 4 notas informadas).

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        double somaNotas = 0;
        
        for (int i = 1; i <= 4; i++) {
            System.out.print("Digite a " + i + "ª nota: ");
            somaNotas += scanner.nextDouble();
        }
        
        double media = somaNotas / 4;
        System.out.println("Média do semestre: " + media);
        
        if (media >= 6.0) {
            System.out.println("PARABÉNS! Você foi aprovado!");
        } else {
            System.out.println("Você não foi aprovado.");
        }
    }
}



10 - BOOOOMMM
Pergunta:
Crie uma bomba relógio (usando somente código - para deixar claro!) cuja contagem regressiva vá de 30 a 0. Escreva a contagem em tela e no final da repetição escreva "EXPLOSÃO".

```java
public class Main {
    public static void main(String[] args) {
        for (int i = 30; i >= 0; i--) {
            System.out.println(i);
        }
        System.out.println("EXPLOSÃO");
    }
}

### 11 - 10, 9, 8, 7, 6, 5, 4, 3, 2, 1...
Pergunta:
Escreva um algoritmo para imprimir os números de 1 (inclusive) a 10 (inclusive) em ordem decrescente.

```java
public class Main {
    public static void main(String[] args) {
        for (int i = 10; i >= 1; i--) {
            System.out.println(i);
        }
    }
}



12 - De quanto até quanto?
Pergunta:
Faça um algoritmo que calcule e escreva a média aritmética dos dois números inteiros informados pelo usuário e todos os números inteiros entre eles. Considere que o primeiro sempre será menor que o segundo.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Digite o primeiro número: ");
        int a = scanner.nextInt();
        
        System.out.print("Digite o segundo número: ");
        int b = scanner.nextInt();
        
        int soma = 0;
        int count = 0;
        
        for (int i = a; i <= b; i++) {
            soma += i;
            count++;
        }
        
        double media = (double) soma / count;
        System.out.println("A média aritmética dos números entre " + a + " e " + b + " é: " + media);
    }
}



13 - Passou no Teste?
Pergunta:
Escreva um programa para ler 6 notas de um aluno, calcular e imprimir a média final. Considere que a nota de aprovação é 6,5. Logo após escrever a mensagem "Calcular a média de outro aluno Sim/Não?" e solicitar uma resposta. Se a resposta for "S", o programa deve ser executado novamente, caso contrário deve ser encerrado exibindo a quantidade de alunos aprovados.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        int alunosAprovados = 0;
        
        while (true) {
            double somaNotas = 0;
            
            for (int i = 1; i <= 6; i++) {
                System.out.print("Digite a " + i + "ª nota: ");
                somaNotas += scanner.nextDouble();
            }
            
            double media = somaNotas / 6;
            System.out.println("Média final: " + media);
            
            if (media >= 6.5) {
                alunosAprovados++;
                System.out.println("Aluno aprovado!");
            } else {
                System.out.println("Aluno reprovado.");
            }
            
            System.out.print("Calcular a média de outro aluno (Sim/Não)? ");
            String resposta = scanner.next();
            
            if (resposta.equalsIgnoreCase("Não")) {
                break;
            }
        }
        
        System.out.println("Quantidade de alunos aprovados: " + alunosAprovados);
    }
}



14 - Uma Brincadeira Sobre Alturas
Pergunta:
Anacleto tem 1,50 metro e cresce 2 centímetros por ano, enquanto Felisberto tem 1,10 metro e cresce 3 centímetros por ano. Construa um algoritmo que calcule e imprima quantos anos serão necessários para que Felisberto seja maior que Anacleto.

```java
public class Main {
    public static void main(String[] args) {
        double anacletoAltura = 1.50;
        double felisbertoAltura = 1.10;
        int anos = 0;
        
        while (felisbertoAltura <= anacletoAltura) {
            anacletoAltura += 0.02;
            felisbertoAltura += 0.03;
            anos++;
        }
        
        System.out.println("Serão necessários " + anos + " anos para Felisberto ser maior que Anacleto.");
    }
}
