# Exercícios Funções

#### Criar um programa calculadora que apresente um menu de seleções no programa principal. Esse menu deverá dar ao usuário a possibilidade de escolher uma entre quatro operações aritméticas. Escolhida a opção desejada, deverá ser solicitada à entrada de dois números, e processada a operação deverá ser exibido o resultado.

using System;

using System.Linq;

  namespace listaexercicio

  {

​    class exercicio

​    {

//Funções       

​      static int Adicao(int n1,int n2){

​        int resultado;

​        resultado=(n1+n2);

​        return resultado;

​      }

​      static int Subtracao(int n1, int n2){

​        int resultado;

​        resultado=(n1-n2);

​        return resultado;

​      }

​      static int Multiplicação(int n1, int n2){

​        int resultado;

​        resultado=(n1*n2);

​        return resultado;

​      }

​      static int Divisao(int n1, int n2){

​        int resultado;

​        resultado=(n1/n2);

​        if((n1==0)||(n2==0)){

​          resultado=0;

​        }

​        return resultado;

​      }

//Bloco Principal

​      static void Main(string[] args)

​      {

​        int resultado, Operacao=0;

​        while(Operacao!=5)

​        {

​          Console.WriteLine("Informe os números que deseja operar: ");

​        int n1=Convert.ToInt32(Console.ReadLine());

​        int n2=Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("Informe a Operação que deseja realizar: ");

​        Console.WriteLine(" 1- Adição");

​        Console.WriteLine(" 2- Subtração");

​        Console.WriteLine(" 3- Multiplicação");

​        Console.WriteLine(" 4- Divisão");

​        Console.WriteLine(" 5- Fim Programa");

​        Operacao=Convert.ToInt32(Console.ReadLine());    

//Chamada das Funções 

​        switch (Operacao)

​        {

​          case 1:

​          resultado=Adicao(n1, n2);

​          Console.WriteLine("Reasultado da Operação: "+resultado);

​          break;

​          case 2:

​          resultado=Subtracao(n1, n2);

​          Console.WriteLine("Resultado da Operação: "+resultado);

​          break;

​          case 3:

​          resultado=Multiplicação(n1,n2);

​          Console.WriteLine("Resultado da Operação: "+resultado);

​          break;

​          case 4:

​          resultado=Divisao(n1, n2);

​          Console.WriteLine("Resultado da Operação: "+resultado);

​          break;

​          case 5:

​          break;

​        } 

​        }      

​      }

​    }

  }

#### Desenvolva um algoritmo que crie uma sub-rotina para calcular e apresentar o valor de uma potência de um número qualquer. Ou seja, ao informar para a sub-rotina o número e sua potência, deverá ser apresentado o seu resultado. Por exemplo, se for mencionado no programa principal a sub-rotina POTENCIA(2, 3), deverá ser apresentado o valor 8.

using System;

using System.Linq;

  namespace exercicio

  {

​    class exercicio

​    {

​      static double potencia(double n1, double n2)

​      {

​        double result;

​        result=Math.Pow(n1, n2);

​        return result;

​      }

​      static void Main(string[] args)

​      {

​        Console.WriteLine("Informe a base da potência: ");

​        double n1=Convert.ToDouble(Console.ReadLine());

​        Console.WriteLine("Informe o expoente: ");

​        double n2=Convert.ToDouble(Console.ReadLine());

​        double resultado= potencia(n1, n2);

​        Console.WriteLine("Resultado da operação: "+resultado);

​      }

​    }

  }

#### Elaborar um programa que por meio de sub-rotina efetue a apresentação do valor da conversão em real (R$) de um valor lido em dólar (US$). Deverá ser solicitado por meio do programa principal o valor da cotação do dólar e a quantidade de dólar disponível.

using System; 

using System.Linq;

  namespace listaexercicio

  {

​    class exercicio

​    {

​      static Double conversor(double n1, double n2)

​      {

​        double resultado = (n1 * n2);

​        return resultado;

​      }

​      static void Main(string[] args)

​      {

​        double conversao;

​        Console.WriteLine("Informe a atual cotação do dolar: ");

​        double cotacaoDolar = Convert.ToDouble(Console.ReadLine());

​        Console.WriteLine("Informe o valor em dolar que deseja converter: ");

​        double valorDolar = Convert.ToDouble(Console.ReadLine());

​        conversao=conversor(cotacaoDolar,valorDolar);

​        Console.WriteLine("valor do dolar atual: "+cotacaoDolar);

​        Console.WriteLine(valorDolar+" dolares convertidos em reais é "+conversao);      

​      }

​    }

  }

#### Para demonstrar o uso de sub-rotina com passagem de parâmetro, considere a leitura de 10 valores em um vetor e os coloque em ordem crescente. A ordenação deve ser executada por uma sub-rotina apropriada para este fim.

using System;

using System.Linq;

  namespace listaExercicio

  {

​    class exercicio

​    {

​      static void ordenacao(int[] vetor, int i)

​      {

​        int[] vetor1 = new int[10];       

​        for (int k = 0; k < 10; k++)

​        {

​          vetor1[k]=Convert.ToInt32(Console.ReadLine()); 

​        }

​        Array.Sort(vetor1);

​        Console.WriteLine("Vetor ordenado: ");

​        for (int j=0; j<10; j++)

​        {

​          Console.WriteLine(vetor1[j]);          

​        }                    

​      }

​      static void Main(string[] args)

​      {

​        Console.WriteLine("Informe os valores do vetor: ");                 

​        int[] vetor1= new int[10];

​        int i=0;

​        ordenacao(vetor1, i);

​      }

​    }

  }

#### Um determinado estabelecimento fará uma venda com descontos nos produtos A e B. Se forem comprados apenas os produtos A ou apenas os produtos B, o desconto será de 10%. Caso sejam comprados os produtos A e B, o desconto será de 15%. O custo da unidade de cada produto é dado, respectivamente, para os produtos A e B como sendo de R$ 10,00 e R$ 20,00. Elaborar um programa que por meio de sub-rotina calcule e apresente o valor da despesa do freguês na compra dos produtos. Lembre-se que o freguês poderá levar mais de uma unidade de um determinado produto.

using System;

using System.Linq;

  namespace listaExercicio

  {

​    class exercicio

​    {

​      static double descontoDoisProdutos(int qtd1,int qtd2)

​      {

​      int v1=10, v2=20;

​      double desc2=0.15;

​        double desconto=((qtd1*v1)+(qtd2*v2))*desc2;

​        double result=(((qtd1*v1)+(qtd2*v2))-desconto);

​        return result;

​      }

​      static double descontoProd(int qtd, int v)

​      {

​        double desconto=((qtd*v)*0.1);

​        double valor=((qtd*v)-desconto);

​        return valor;

​      }

​      static void Main(string[] args)

​      {

​        int qtdA, qtdB, valorA=10, valorB=20;

​        double valorFinal;

​        Console.WriteLine("Informe a quantidade de Produto A que deseja adquirir:");

​        qtdA= Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("Informe a quantidade de Produto B que deseja adquirir:");

​        qtdB=Convert.ToInt32(Console.ReadLine());

​        if((qtdA>0)&&(qtdB<=0))

​        {

​          double aPagar=descontoProd(qtdA, valorA);

​          Console.WriteLine("Total a Pagar: "+aPagar);

​        }

​        if((qtdA<=0)&&(qtdB>0))

​        {

​         double aPagar=descontoProd(qtdB, valorB);

​         Console.WriteLine("Total a pagar "+aPagar);  

​        }

​        if((qtdA>0)&&(qtdB>0))

​        {

​          valorFinal=descontoDoisProdutos(qtdA, qtdB);

​          Console.WriteLine("Total a pagar: "+valorFinal);

​        }

​      }

​    }

  }

#### 