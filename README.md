# Calculadora de Circunferência e Volume

Este programa Java permite calcular a circunferência e o volume de uma esfera com base no raio fornecido pelo usuário. Ele também informa o valor de PI com duas casas decimais.

## Como usar

1. Clone o repositório:

```bash
git clone https://github.com/seuusuario/suorepositorio.git
```

2. Navegue até o diretório do projeto:

```bash
cd suorepositorio
```

3. Compile o programa:

```bash
javac Main.java
```

4. Execute o programa:

```bash
java Main
```

5. Siga as instruções para inserir o raio da esfera quando solicitado.

## Exemplo de Uso

```
Enter radius: 3.0
Circumference: 18.84
Volume: 113.04
PI value: 3.14
```

## Estrutura do Projeto

- `Main.java`: Contém o código-fonte principal do programa.
- `util/Calculator.java`: Classe utilitária para realizar cálculos de circunferência e volume.

## Contribuindo

Contribuições são bem-vindas! Abra um problema ou envie uma solicitação de pull para discutir mudanças importantes.

## Código-fonte

``` bash
  /*
    Problema exemplo:
        Fazer um programa para ler um valor numérico qualquer,
        e daí mostrar quanto seria o valor de uma circunferência
        e do volume de uma esfera para um raio daquele valor.
         Informar também o valor de PI com duas casas decimais

    Exemplo:
        Enter radius: 3.0
        Circumference: 18.84
        Volume: 113.04
        PI value: 3.14
 */

import util.Calculator;
import java.util.Locale;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {


        Locale.setDefault(Locale.US);
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter radius: ");
        double radius = sc.nextDouble();


        double c = Calculator.circumference(radius);

        double v = Calculator.volume(radius);

        System.out.printf("Circumference: %.2f%n", c);
        System.out.printf("Volume: %.2f%n", v);
        System.out.printf("PI value: %.2f%n", Calculator.PI);


        sc.close();

    }
}
```
### Classe
```
  package util;

public class Calculator {

    public static double PI = 3.14;

    public static double circumference(double radius){
        return 2.0 * PI * radius;
    }

    public static double volume(double radius){
        return 4.0 * PI * radius * radius * radius / 3.0;
    }
}
```
