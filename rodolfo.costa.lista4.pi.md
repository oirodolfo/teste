Lista 4 - PI (prática) 2014.2
=================================
Professor Rogério Neves

Rodolfo Costa

Exercício 1
-----------
-   Criar uma calculadora...
-
-   Java:
```java
     float n1, n2, re = 0;
        System.out.println("[ C A L C U L A D O R A ]");
        Scanner n = new Scanner(System.in);
        System.out.print("Insira um número: ");
        n1 = n.nextFloat();
        System.out.print("Insira outro número: ");
        n2 = n.nextFloat();

        System.out.print("Qual é o operador? (São permitidas as operações:  '+', '-', '*', '/' e '%'): ");
        char op = n.next().toLowerCase().replace(" ", "").charAt(0);

        if (op == '+' || op == '-' || op == '*' || op == '/' || op == '%') {
            if (op == '+') {
                re = n1 + n2;
            } else if (op == '-') {
                re = n1 - n2;
            } else if (op == '*') {
                re = n1 * n2;
            } else if (op == '/') {
                re = n1 / n2;
            } else if (op == '%') {
                re = n1 % n2;
            }

            System.out.printf("\nO resultado de %f %c %f = %f.\n", n1, op, n2, re);

        } else {
            System.out.printf("\nO operador '%c' é inválido. Tente novamente!\n", op);
        }

    }

```

Exercício 2
-----------
-   Calcular notas com jOptionPane
-
-   Java:
```java

        String p1 = leia("Entre a nota da Prova 1: ");
        float prova1 = Float.parseFloat(p1);

        String p2 = leia("Entre a nota da Prova 2: ");
        float prova2 = Float.parseFloat(p2);

        String p3 = leia("Entre a nota da Prova Prática: ");
        float provaPratica = Float.parseFloat(p3);

        String p4 = leia("Entre a nota do Projeto Final: ");
        float projetoFinal = Float.parseFloat(p4);

        String p5 = leia("Entre a nota das Atividades: ");
        float atividades = Float.parseFloat(p5);

        double mediaPratica = 0.8 * provaPratica + 0.2 * projetoFinal + 0.1 * atividades;
        double mediaTeorica = 0.4 * prova1 + 0.6 * prova2;
        double notaFinal = 0.4 * mediaPratica + 0.6 * mediaTeorica;

        // Incremento da atividade
        char conceito = 'F';

        if (notaFinal <= 4.5) {
            conceito = 'F';
        } else if (notaFinal >= 4.6 && notaFinal <= 5.5) {
            conceito = 'D';
        } else if (notaFinal >= 5.6 && notaFinal <= 7.5) {
            conceito = 'C';
        } else if (notaFinal >= 7.6 && notaFinal <= 9.5) {
            conceito = 'B';
        } else if (notaFinal > 9.5) {
            conceito = 'A';
        }
        String status = (conceito == 'F' ? "Você foi reprovado com conceito F." : "VOCÊ FOI APROVADO COM O CONCEITO: " + conceito);
        mostre("SUA NOTA FINAL É: " + notaFinal + "\n" + status);

    }

    public static String leia(String t) {
        return javax.swing.JOptionPane.showInputDialog(t);
    }

    public static void mostre(String t) {
        javax.swing.JOptionPane.showMessageDialog(null, t);
    }

```

Exercício 3
-----------
-   Calcular reajuste
-
-   Java:
```java
double reajuste = 0.0, valorFinal, finalReajuste;

        System.out.println("[ R E A J U S T E ]");

        Scanner n = new Scanner(System.in);

        System.out.print("Digite o sexo (M ou F): ");
        char sexo = n.next().replace(" ", "").toLowerCase().charAt(0);

        if (sexo != 'm' && sexo != 'f') {
            System.out.println("Alerta: sexo inválido. Tente novamente!");
        } else {
            System.out.print("Insira o salário: ");
            double salario = n.nextDouble();

            System.out.print("Insira o tempo de casa (em anos): ");
            int tempo = n.nextInt();

            System.out.print("Insira o número de dependentes: ");
            int dependentes = n.nextInt();

            if (sexo == 'm') {
                if (tempo >= 10) {
                    reajuste = 1.05;
                } else if (tempo < 10) {
                    reajuste = 1.03;
                }
            } else if (sexo == 'f') {
                if (tempo >= 8) {
                    reajuste = 1.05;
                } else if (tempo < 8) {
                    reajuste = 1.03;
                }
            }
            valorFinal = (dependentes > 1 ? (salario * reajuste + (salario * 0.02)) : (salario * reajuste));

            finalReajuste = valorFinal - salario;

            System.out.printf("\nO salário terá um reajuste de R$%.2f.\nNOVO SALÁRIO: R$%.2f.\n", finalReajuste, valorFinal);

        }
```

