Lista de exercícios 1 - PI 2014.2
=================================
Professor Diogo Santana Martins

Aluno Augusto Manoel Barreto de Abreu - 11058713

Exercício 1
-----------
-   Entrada: numero
-   Saída: anterior, numero, proximo
-   Processamento: descobrir anterior e proximo
-   Algorítmo:
```
    algoritmo anteriorproximo:
    inicio
        inteiro anterior, numero, proximo
        leia numero
        anterior <- numero - 1
        proximo <- numero + 1
        escreva "anterior= ", anterior
        escreva "proximo= ", proximo
    fim
```
-   Java:
```java
    import java.util.Scanner;
    public class Ex1 {
        public static void main(String[] args){
        	/*
        		var ant: número inteiro anterior
        		var num: número inteiro inserido
        		var prox: próximo número inteiro
        	*/
            int ant, num, prox;
 
            // cria um novo Scanner
            Scanner input = new Scanner(System.in);
            
            // recebe o número inteiro
            System.out.println("Digite um número inteiro:");
            num = input.nextInt();

            // encontra o número anterior e o próximo número inteiro e imprime
            ant = num-1;
            prox = num+1;
            System.out.println("Anterior: " + ant + "\nPróximo: " + prox );
        }
    }
```

Exercício 2
-----------
-   Entrada: numero1, numero2
-   Saída: dividendo, divisor, quociente, resto
-   Processamento: calcular quociente e resto
-   Algoritmo:
```
    algoritmo Numeros:
    inicio
        real num1, num2, dividendo, divisor, quociente, resto
        leia num1
        leia num2
        dividento <- num1
        divisor <- num2
        quociente <- num1/num2
        resto <- num1 mod num2
        escreva "Dividendo= ", dividendo
        escreva "Divisor= ", divisor
        escreva "Quociente= ", quociente
        escreva "Resto= ", resto
    fim
```
-   Java:
```java
    import java.util.Scanner;
    public class Ex2 {
        public static void main(String[] args){
        	/*
        		var num1 e num2: recebem números reais
        		var divid: dividendo da divisão
        		var divis: divisor da divisão
        		var quoc: quociente da divisão
        		var rest: resto da divisão
        	*/
            float num1, num2, divid, divis, quoc, rest;

            // cria um novo Scanner
            Scanner input = new Scanner(System.in);
            
            // recebe o num1
            System.out.println("Digite um número:");
            num = input.nextFloat();

            // recebe o num2
            System.out.println("Digite outro número:");
            num = input.nextFloat();

            // efetua operações, atribuições e imprime
            divid = num1;
            divis = num2;
            quoc  = num1 / num2;
            rest  = num1 % num2;
            System.out.println("Dividendo: " + divid + "\nDivisor: " + divis + "\nQuociente: " + quoc + "\nResto: " + rest );
        }
    }
```

Exercício 3
-----------
-   Entrada: valorEmprestimo
-   Saída: divida
-   Processamento: calcular divida após 6 meses com taxa de 5%
-   Algoritmo:
```
    algoritmo calculoDivida:
    inicio
        real valorEmprestimo, divida
        leia valorEmprestimo
        divida <- ( valorEmprestimo * 5 / 100 ) * 6 + valorEmprestimo
        escreva "O valor da sua dívida é de", divida
    fim
```
-   Java:
```java
    import java.util.Scanner;
    public class Ex3 {
        public static void main(String[] args){
        	/*
        		var valor: recebe o valor do empréstimo
        		var divida: valor da dívida final
        	*/
            float valor, divida;

            // cria um novo Scanner
            Scanner input = new Scanner(System.in);

            // recebe o valor do empréstimo
            System.out.println("Digite o valor do empréstimo:");
            valor = input.nextFloat();

            // calcula dívida de 6 meses com taxa de 5% e imprime
            divida = ( valor * 5.0f /100 ) * 6.0f + valor;
            System.out.println("Valor da dívida: " + divida );
        }
    }
```

Exercício 4
-----------
-   Entrada: baseRetangulo, alturaRetangulo
-   Saída: perimetro, area, diagonal
-   Processamento: calcular perimetro(2 vezes base +  2 vezes altura), area(base x altura) e diagonal(pitagoras)
-   Algoritmo:
```
    algoritmo retangulo:
    inicio
        real baseRetangulo, alturaRetangulo, perimetro, area, diagonal
        leia baseRetangulo
        leia alturaRetangulo
        perimetro <- baseRetangulo * 2 + alturaRetangulo * 2
        area <- baseRetangulo * alturaRetangulo
        diagonal <- raiz( baseRetangulo * baseRetangulo + alturaRetangulo * alturaRetangulo )
        escreva "Perímetro= ", perimetro
        escreva "Área= ", area
        escreva "Diagonal= ", diagonal
    fim
```
-   Java:
```java
    import java.util.Scanner;
    public class Ex4 {
        public static void main(String[] args){
        	/*
        		var base: recebe a base
        		var altura: recebe a altura
        		var per: armazena o perímetro
        		var area: armazena a área
        		var diag: armazena a diagonal
        	*/
            float base, altura, per, area, diag;

            // cria um novo Scanner
            Scanner input = new Scanner(System.in);

            // recebe a base
            System.out.println("Digite a base do retângulo:");
            base = input.nextFloat();

            // recebe a altura
            System.out.println("Digite a altura do retângulo:");
            altura = input.nextFloat();

            // calcula perímetro, área, diagonal e imprime
            peri = base * 2.0f + altura * 2.0f;
            area = base * altura;
            /*
            	Método Math.sqrt: raíz quadrada
            	Método Math.pow: potência
            */
            diag = Math.sqrt( Math.pow(base, 2) + Math.pow(altura, 2) );
            System.out.println("Perímetro: " + peri + "Área: " + area + "Diagonal: " + diag );
        }
    }
```

Exercício 5
-----------
-   Entrada: ladoQuadrado
-   Saída: perimetro, area, diagonal
-   Processamento: calcular perímetro(4 vezes lado), area(lado x lado), diagonal(pitágoras)
-   Algoritmo:
```
    algoritmo quadrado:
    início
        real baseQuadrado, perimetro, area, diagonal
        leia baseQuadrado
        perimetro <- 4 * baseQuadrado
        area <- baseQuadrado * baseQuadrado
        diagonal <- raizQuadrada( 2 * baseQuadrado * baseQuadrado )
        escreva "Perímetro= ", perimetro
        escreva "Área= ", area
        escreva "Diagonal= ", diagonal
    fim
```
-   Java:
```java
    import java.util.Scanner;
    public class Ex5 {
        public static void main(String[] args){
        	/*
        		var base: recebe a base
        		var peri: armazena o perímetro
        		var area: armazena a área
        		var diag: armazena a diagonal
            float base, peri, area, diag;

            // cria um novo Scanner
            Scanner input = new Scanner(System.in);

            // recebe a base
            System.out.println("Digite a base do quadrado:");
            base = input.nextFloat();

            // calcula perímetro, área, diagonal e imprime
            peri = base * 4.0f;
            area = base * base;
            diag = Math.sqrt( Math.pow( base, 2 ) * 2 );
            System.out.println("Perímetro: " + peri + "\nÁrea: " + area + "\nDiagonal: " + diag );
        }
    }
```

Exercício 6
-----------
-   Entrada: raioCirculo
-   Saída: perimetro, area
-   Processamento: calcular perímetro(2 * pi * raio) e area(pi * raio * raio)
-   Algoritmo:
```
    algoritmo circulo:
    inicio
        real raioCirculo, pi <- 3.14
        leia raioCirculo
        perimetro <- 2 * pi * raioCirculo
        area <- pi * raioCirculo * raioCirculo
        escreva "Perímetro= ", perimetro
        escreva "Área= ", area
    fim
```
-   Java: 
```java
    import java.util.Scanner;
    public class Ex6 {
        public static void main(String[] args){
        	/*
        		var raio: recebe o raio
        		var perimetro: armazena o perímetro
        		var area: armazena a área
        	*/
            float raio, perimetro, area;

            // cria um novo Scanner
            Scanner input = new Scanner(System.in);

            // recebe o raio
            System.out.println("Digite o raio do círculo:");
            raio = input.nextFloat();

            // calcula perímetro, área e imprime
            perimetro = 2.0f * PI * raio;
            area = PI * Math.pow( raio, 2 );
            System.out.println("Perímetro: " + perimetro + "\nÁrea: " + area );
        }
		
		// defini constante PI
        static final float PI = 3.14159265f;
    }
```

Exercício 7
-----------
-   Entrada: larguraParalelepido, alturaParalelepipedo, profundidadeParalelepipedo
-   Saída: perímetro, área, volume, diagonal
-   Processamento: Calcular perímetro(2 * perimetroBase + 2 * perimetroLateral), area(2 * areaBase + 2 * areaLateral), volume(largura * altura * profundidade), diagonal(raizQuadrada(largura^2 + altura^2 + profundidade^2))
-   Algoritmo:
```
    algorimo paralelepipedo:
    inicio
        real larguraP, alturaP, profundidadeP, perimetro, area, volume, diagonal
        leia larguraP
        leia alturaP
        leia profundidadeP
        perimetro <- ( 2 * larguraP + 2 * profundidadeP ) * 2 + 4 * alturaP 
        area <- 2 * larguraP * profundidadeP + 2 * larguraP * alturaP
        volume <- larguraP * alturaP * profundidadeP
        diagonal <- raizQuadrada(larguraP * larguraP + alturaP * alturaP + profundidadeP * profundidadeP)
        escreva "Perímetro= ", perimetro
        escreva "Área= ", area
        escreva "Volume= ", volume
        escreva "Diagonal= ", diagonal
    fim
```
-   Java:
```java
    import java.util.Scanner;
    public class Ex7 {
        public static void main(String[] args){
        	/*
        		var larg: recebe largura
        		var altu: recebe altura
        		var prof: recebe profundidade
        		var area: armazena area
        		var volu: armazena volume
        		var diag: armazena diagonal
        	*/
            float larg, altu, prof, peri, area, volu, diag;

            // cria um novo Scanner
            Scanner input = new Scanner(System.in);

            // recebe a largura
            System.out.println("Digite a largura do paralelepipedo:");
            larg = input.nextFloat();

            // recebe a altura
            System.out.println("Digite a altura do paralelepipedo:");
            altu = input.nextFloat();

            // recebe a profundidade
            System.out.println("Digite a profundidade do paralelepipedo:");
            prof = input.nextFloat();

            // calcula perímetro, área, volume, diagonal e imprime
            perimetro = ( 2.0f * larg + 2.0f * prof ) * 2.0f + 4.0f * altu;
            area = 2.0f * larg * prof + 2.0f * larg * altu;
            volu = larg * prof * altu;
            diag = Math.sqrt( Math.pow( larg, 2 ) + Math.pow( altu, 2 ) + Math.pow( prof, 2 ) );
            System.out.println("Perímetro: " + perimetro + "\nÁrea: " + area + "\nVolume: " + volu + "Diagonal: " + diag );
        }
    }
```

Exercício 8
-----------
-   Entrada: cateto1, cateto2
-   Saída: hipotenusa
-   Processamento: calcular hipotenusa(pitágoras)
-   Algoritmo:
```
    algoritmo hipotenusa:
    inicio
        real cateto1, cateto2, hipotenusa
        leia cateto1
        leia cateto2
        hipotenusa <- raizQuadrada( cateto1 * cateto1 + cateto2 * cateto2 )
        escreva "Hipotenusa= ", hipotenusa
    fim
```
-   Java:
```java
    import java.util.Scanner;
    public class Ex8 {
        public static void main(String[] args){
        	/*
        		var cat1 e cat2: recebem os catetos
        		var hipo: armazena a hipotenusa
        	*/
            float cat1, cat2, hipo;

            // cria um novo Scanner
            Scanner input = new Scanner(System.in);

            // recebe o cateto 1
            System.out.println("Digite o cateto 1:");
            cat1 = input.nextFloat();

            // recebe o cateto 2
            System.out.println("Digite o cateto 2:");
            cat2 = input.nextFloat();

            // calcula hipotenusa e imprime
            hipo = Math.sqrt( Math.pow( cat1, 2 ) + Math.pow( cat2, 2 ) );
            System.out.println("Hipotenusa: " + hipo );
        }
    }
```

Exercício 9
-----------
-   Entrada: seguimento1, seguimento2, seguimento3
-   Saída: verificaSeguimentos
-   Processamento: verificar se seguimento1 < seguimento2 + seguimento3, seguimento2 < seguimento1 + seguimento3 e seguimento3 < seguimento1 + seguimento2
-   Algoritmo:
```
    algoritmo seguimentos:
    inicio
        real seguimento1, seguimento2, seguimento3
        caracter verificaSeguimentos
        leia seguimento1
        leia seguimento2
        leia seguimento3
        verificaSeguimentos <- "Os seguimentos não formam um triângulo!"
        se seguimento1 < seguimento2 + seguimento3 E seguimento2 < seguimento1 + seguimento3 E seguimento3 < seguimento 1 + seguimento2 então:
            escreva "Os seguimentos formam um triângulo!"
        senão:
            escreva "Os seguimentos não formam um triângulo!"
    fim
```
-   Java:
```java
    import java.util.Scanner;
    public class Ex9 {
        public static void main(String[] args){
        	/*
        		var seg1, seg2 e seg3: recebem 3 segmentos
        	*/
            float seg1, seg2, seg3;

            // cria novo Scanner
            Scanner input = new Scanner(System.in);

            // recebe seguimento 1
            System.out.println("Digite o seguimento 1:");
            seg1 = input.nextFloat();

            // recebe seguimento 2
            System.out.println("Digite o seguimento 2:");
            seg2 = input.nextFloat();

            // recebe seguimento 3
            System.out.println("Digite o seguimento 3:");
            seg3 = input.nextFloat();

            /*
            	Verificação da desigualdade triangular
            */
            if( seg1 < ( seg2 + seg3 ) && seg2 < ( seg1 + seg3 ) && seg3 < ( seg1 + seg2 ) ) {
                System.out.println( "Os seguimentos formam um triângulo!" );
            } else {
                System.out.println( "Os seguimentos não formam um triângulo!" );
            }
        }
    }
```

Exercício 10
------------
-   Entrada: lado1, lado2, lado3
-   Saída: tipo de triângulo(isósceles, escaleno ou equilátero)
-   Processamento: verificar os lados - 3 iguais: equilátero; 2 iguais: isósceles; 3 diferentes: escaleno
-   Algoritmo:
```
    algoritmo triangulo:
    inicio
        real lado1, lado2, lado3
        caracter tipo
        leia lado1
        leia lado2
        leia lado3
        se lado1 = lado2 E lado1 = lado3 E lado2 = lado3 então:
            tipo <- "equilátero"
        senão se lado1 = lado2 OU lado1 = lado3 OU lado2 = lado3 então:
            tipo <- "isósceles"
        senão:
            tipo <- "escaleno"
        escreva "Tipo de triângulo=", tipo
    fim
```
-   Java:
```java
    import java.util.Scanner;
    public class Ex10 {
        public static void main(String[] args){
        	/*
        		var ld1, ld2, ld3: recebe os 3 lados de um triângulo
        		var tipo: armazena o tipo do triângulo
        	*/
            float ld1, ld2, ld3;
            String tipo;

            // cria um novo Scanner
            Scanner input = new Scanner(System.in);

            // recebe lado 1
            System.out.println("Digite o lado 1 do triângulo:");
            ld1 = input.nextFloat();

            // recebe lado 2
            System.out.println("Digite o lado 2 do triângulo:");
            ld2 = input.nextFloat();

            // recebe lado 3
            System.out.println("Digite o lado 3 do triângulo:");
            ld3 = input.nextFloat();

            // verifica qual o tipo do triângulo baseado em seus lados
            if( ld1 == ld2 && ld1 == ld3 && ld2 == ld3 ) {
                tipo = "equilátero";
            } else if( ld1 == ld2 || ld1 == ld3 || ld2 == ld3 ){
                tipo = "isósceles";
            } else {
                tipo = "escaleno";
            }

            // imprime o tipo do triângulo
            System.out.println( "Tipo de triângulo: " + tipo );
        }
    }
```

Exercício 11
------------
-   Entrada: circX, circY, ptX, ptY, raio
-   Saída: localização do ponto em relação a circunferência
-   Processamento: verificar se o ponto está dentro da circunferência através do teorema de pitágoras(hipotenusa <= raio = ponto dentro da circunferência)
-   Algoritmo:
```
    algoritmo ponto_circunferencia:
    inicio
        real circX, circY, ptX, ptY, raio, hipotenusa
        leia circX
        leia circY
        leia ptX
        leia ptY
        leia raio
        hipotenusa <- raizQuadrada( ( ptX - circX ) * ( ptX - circX ) + ( ptY - circY ) * ( ptY - circY ) )
        se hipotenusa <= raio então:
            escreva "O ponto está dentro da circunferência"
        senão:
            escreva "O ponto não está dentro da circunferência"
    fim
```
-   Java:
```java
    import java.util.Scanner;
    public class Ex11 {
        public static void main(String[] args){
        	/*
        		var circX: recebe coordenada X do centro da circunferência
        		var circY: recebe coordenada Y do centro da circunferência
        		var ptX: recebe a coordenada X do ponto
        		var ptY: recebe a coordenada Y do ponto:
        		var raio: recebe o raio da circunferência
        		var hipotenusa: armazena a distância do centro da circunferência até o ponto
            float circX, circY, ptX, ptY, raio, hipotenusa;

            // cria um novo Scanner
            Scanner input = new Scanner(System.in);

            // recebe a coordenada X do centro da circunferência
            System.out.println("Digite a coordenada X do centro da circunferência:");
            circX = input.nextFloat();

            // recebe a coordenada Y do centro da circunferência
            System.out.println("Digite a coordenada Y do centro da circunferência:");
            circY = input.nextFloat();

            // recebe o raio da circunferência
            System.out.println("Digite o raio da circunferência:");
            raio = input.nextFloat();

            // recebe a coordenada X do ponto
            System.out.println("Digite o ponto X do ponto:");
            ptX = input.nextFloat();

            // recebe a coordenada Y do ponto
            System.out.println("Digite o ponto Y do ponto:");
            ptY = input.nextFloat();

            // calcula a distância(hipotenusa) entre o centro e o ponto
            hipotenusa = Math.sqrt( Math.pow( ( ptX - circX ), 2) + Math.pow( ( ptY - circY ), 2) );

            // verifica se o ponto está dentro da circunferência e imprime mensagem
            if( hipotenusa <= raio ) {
                System.out.println( "O ponto está dentro da circunferência" );
            } else {
                System.out.println( "O ponto não está dentro da circunferência" );
            }
        }
    }
```

Exercício 12
------------
-   Entrada: razao da PA, primeiroTermo
-   Saída: 20º termo da PA
-   Processamento: calcular a PA a partir da razao
-   Algoritmo:
```
    algoritmo pa:
    inicio
        real razao, pa <- 0, primeiroTermo
        inteiro contador <- 0
        leia razao
        leia primeiroTermo 
        pa = primeiroTermo + (contador + 1) * razao
        enquanto contador < 20 faça:
        inicio
            pa = primeiroTermo + (contador + 1) * razao
            contador = contador + 1
        fim
        imprima "20º termo= ", pa
    fim
```
-   Java:
```java
    import java.util.Scanner;
    public class Ex12 {
        public static void main(String[] args){
        	/*
        		var razao: recebe a razao da PA
        		var pa: incializa a pa
        		var primerTermo: recebe o primeiro termo da PA
				var contador: contador do loop
        	*/
            float razao, pa=0, primerTermo;
            int contador = 1;

            // cria um novo Scanner
            Scanner input = new Scanner(System.in);

            // recebe a razão da PA
            System.out.println("Digite a razão da PA:");
            razao = input.nextFloat();

            // recebe o primeiro termo da PA
            System.out.println("Digite o primeiro termo da PA:");
            primerTermo = input.nextFloat();

            // calcula o 20º termo da PA e imprime
            while( contador <= 20 ) {
                pa += pa + ( contador - 1 ) * razao;
                contador = contador + 1;
            }
            System.out.println( "20º termo: " + pa );
        }
    }
```

Exercício 13
------------
-   Entrada: primeiroTermo, razao
-   Saída: 20º termo da PG
-   Processamento: calcular 20º termo da PG( An = A1 * razao^An-1 )
-   Algoritmo:
```
    algoritmo pg:
    inicio
        real primeiroTermo, razao, pg, acumulador
        inteiro contador <- 0
        leia primeiroTermo
        leia razao
        enquanto contador < 20 faça:
        inicio
            acumulador <- razao * acumulador
            contador <- contador + 1
        fim
        pg <- primeiroTermo * acumulador
        escreva "20º termo=", pg
    fim
```
-   Java:
```java
    import java.util.Scanner;
    public class Ex13 {
        public static void main(String[] args) {
        	/*
        		var primerTermo: recebe o primeiro termo da PG
        		var razao: recebe a razão da PG
        		var pg: incializa a pg;
        		var acumulador: acumula a potência
        		var contador: contador do loop
        	*/
            float primerTermo, razao, pg, acumulador;
            int contador = 0;

            // cria um novo Scanner
            Scanner input = new Scanner( System.in );

            // recebe o primeiro termo da PG
            System.out.println( "Digite o primeiro termo da PG:" );
            primerTermo = input.nextFloat();

            // recebe a razão da PG
            System.out.println( "Digite a razao da PG:" );
            razao = input.nextFloat();

            // efetua a potência
            while( contador < 20 ) {
                acumulador = razao * acumulador;
                contador++;
            }
            /*
                Loop pode ser substituído por Math.pow( razao, 20 );
            */

            // calcula 20º termo da PG e imprime
            pg = primerTermo * acumulador;
            System.out.println( "20º termo da PG: " + pg );
        }
    }
```

Exercício 14
------------
-   Entrada: hora, minutos, segundos
-   Saída: segundos [desde o começo do dia], minutos [desde o começo do dia]
-   Processamento: somar a quantidade de segundos em cada minuto e hora com os segundos fornecidos e a quantidade de minutos em cada hora com os minutos fornecidos
-   Algoritmo:
```
    algoritmo segundos:
    inicio
        inteiro hora, minutos, segundos
        leia hora
        leia minutos
        leia segundos
        segundos <- segundos + ( hora * 60 * 60 ) + ( minutos * 60 )
        minutos <- minutos + ( hora * 60 )
        escreva "Minutos desde o começo do dia= ", minutos
        escreva "Segundos desde o começo do dia= ", segundos
    fim
```
-   Java:
```java
    import java.util.Scanner;
    public class Ex14 {
        public static void main(String[] args) {
        	/*
        		var hora: recebe a hora 
        		var minutos: recebe os minutos 
        		var segundos: recebe os segundos
        	*/
            int hora, minutos, segundos;
			
			// cria um novo Scanner
            Scanner input = new Scanner( System.in );

            // recebe a hora 
            System.out.println( "Digite a hora atual:" );
            hora = input.nextInt();

            // recebe os minutos
            System.out.println( "Digite o minuto atual:" );
            minutos = input.nextInt();

            // recebe os segundos
            System.out.println( "Digite o segundo atual:" );
            segundos = input.nextInt();

            // calcula quantos segundos e quantos minutos já se passaram desde o início do dia e imprime
            segundos = segundos + ( hora * 60 * 60 ) + ( minutos * 60 );
            minutos  = minutos + ( hora * 60 );
            System.out.println( "Minutos desde o começo do dia: " + minutos );
            System.out.println( "Segundos desde o começo do dia: " + segundos );
        }
    }
```

Exercício 15
------------
-   Entrada: salarioMin, salarioBase
-   Saída: salalariosContidos [no salarioBase]
-   Processamento: dividir salarioBase por salarioMin
-   Algoritmo:
```
    algoritmo salariosMin:
    inicio
        real salarioMin, salarioBase, salariosContidos
        leia salarioMin
        leia salarioBase
        salariosContidos <- salarioBase / salarioMin
        escreva "Estão contidos ", salariosContidos, " salários mínimos no salário base"
    fim
```
-   Java:
```java
    import java.util.Scanner;
    public class Ex15 {
        public static void main(String[] args) {
        	/*
        		var salMini: recebe o salário mínimo
        		var salBase: recebe o salário que servirá de base de comparação
        		var salCont: armazena a quantidade de salários mínimos no salário base
        	*/
            float salMini, salBase, salCont;

            // cria um novo Scanner
            Scanner input = new Scanner( System.in );

            // recebe o salário mínimo
            System.out.println( "Digite o valor do salário-mínimo:" );
            salMini = input.nextFloat();

            // recebe o salário base
            System.out.println( "Digite o valor do salário:" );

            // calcura quantos salários mínimos estão contidos no salário base e imprime
            salBase = input.nextFloat();
            salCont = salBase / salMini;
            System.out.println( "Salários-mínimos contidos no salário informado: " + salCont );
        }
    }
```

Exercício 16
------------
-   Entrada: prova1, prova2, trabalho1, trabalho2
-   Saída: média [ponderada]
-   Processamento: calcular média conforme fórmula: media = ( prova1 * 0.3 + prova2 * 0.4 + trabalho1 * 0.1 + trabalho2 * 0.2 )
-   Algoritmo:
```
    algoritmo mediaPonderada:
    inicio
        real prova1, prova2, trabalho1, trabalho2, media
        leia prova1
        leia prova2
        leia trabalho1
        leia trabalho2
        media <- prova1 * 0.3 + prova2 * 0.4 + trabalho1 * 0.1 + trabalho2 * 0.2
        escreva "Sua média= ", media
    fim
```
-   Java:
```java
    import java.util.Scanner;
    public class Ex16 {
        public static void main(String[] args) {
        	/*
        		var prova1, prova2: recebem as notas das provas
        		var trab1, trab2: recebem as notas dos trabalhos
        		var media: armazena a média ponderada
        	*/
            float prova1, prova2, trab1, trab2, media;

            // cria um novo Scanner
            Scanner input = new Scanner( System.in );

            // recebe a nota da prova 1
            System.out.println( "Digite a nota da prova 1:" );
            prova1 = input.nextFloat();

            // recebe a nota da prova 2
            System.out.println( "Digite a nota da prova 2:" );
            prova2 = input.nextFloat();

            // recebe a nota do trabalho 1
            System.out.println( "Digite a nota do trabalho 1:" );
            trab1  = input.nextFloat();

            // recebe a nota do trabalho 2
            System.out.println( "Digite a nota do trabalho 2:" );
            trab2  = input.nextFloat();

            // calcula média e imprime
            media  = prova1 * 0.3f + prova2 * 0.4f + trab1 * 0.1f + trab2 * 0.2f;
            System.out.println( "Média: " + media );
        }
    }
```

Exercício 17
------------
-   Entrada: largura, comprimento
-   Saída: quantidadeLatas, custoTotal
-   Procedimento: calcular a quantidade de latas para pintar a área sabendo que 1L de tinta pinta 3 metros quadrados; custo total em lata de 5L sabendo que cada lata custa 150 reais
-   Algoritmo:
```
    algoritmo lata:
    inicio
        real largura, comprimento, custoTotal, quantidadeLatas
        leia largura
        leia comprimento
        quantidadeLatas <- teto( ( largura * comprimento )/3 ) // função/método teto arredonda para cima
        custoTotal <- quantidadeLatas * 150
        escreva "Quantidade de latas necessárias para pintar= ", quantidadeLatas
        escreva "Custo total= ", custoTotal
    fim
```
-   Java:
```java
    import java.util.Scanner;
    public class Ex17 {
        public static void main(String[] args) {
        	/*
        		var larg: recebe a largura do piso
        		var compr: recebe o comprimento do piso
        		var custo: armazena o custo total
        		var qnt: armazena a quantidade de latas necessárias para pintar a área
            */
            float larg, compr, custo, qnt;

            // cria um novo Scanner
            Scanner input = new Scanner( System.in );

            // recebe a largura
            System.out.println( "Digite a largura do piso:" );
            larg = input.nextFloat();

            // recebe o comprimento
            System.out.println( "Digite o comprimento do piso:" );
            compr = input.nextFloat();

            // calcula a quantidade, o custo total e imprime
            qnt   = Math.ceil( ( largura * comprimento )/3 ); // método Math.ceil arredonda para cima
            custo = qnt * 150.0f;
            System.out.println( "Quantidade de latas necessárioas: " + qnt );
            System.out.println( "Custo total: " + custo );
        }
    }
```

Exercício 18
------------





