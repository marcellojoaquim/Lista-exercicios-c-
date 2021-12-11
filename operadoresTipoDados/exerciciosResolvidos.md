# Exercícios Operadores e Tipo de Dados

#### Escreva um programa para **ler** um valor (do teclado) e **escrever** (na tela) o seu **antecessor**.

using System;

  namespace listaExerci01

  {

​    class listaExerci

​    {

​      static void Main(string[] args)

​      {

​        int numero;

​        Console.WriteLine("Digite um numero: ");

​        numero=Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("O numero digitado foi: "+numero+" Seu antecessor é: "+(numero-1));

​      }

​    }

  }

#### Escreva um programa para ler as dimensões de um retângulo (base e altura), calcular e escrever a área do retângulo.

using System;

  namespace ListaExerci1_02

  {

​    class Exercicio

​    {

​      static void Main(string[] args)

​      {

​        double Base, altura, area;

​        Console.WriteLine("Informe o comprimento da Base: ");

​        Base=Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("Informe o comprimento da altura: ");

​        altura=Convert.ToInt32(Console.ReadLine());

​        area=(Base*altura);

​        Console.WriteLine("A área deste retângulo é: "+area);

​      }

​    }

  }

#### Faça um programa que leia a idade de uma pessoa expressa em anos, meses e dias e escreva a idade dessa pessoa expressa apenas em dias. Considerar ano com 365 dias e mês com 30 dias.
 using System;

  namespace ListaExerci

  {

​    class Exercicio

​    {

​      static void Main(string[] args)

​      {

​        double idade, idadeD;

​        string forma;

​        Console.WriteLine("Este programa tem por finalidade converter sua idade em dias.");

​        Console.WriteLine("informe a idade que deseja converter: ");

​        idade=Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("Informe qual o formato da idade que digitou: ");

​        Console.WriteLine("D se for em dias, M se for em meses, A se for em anos");

​        forma=Console.ReadLine();

​        if (forma=="D")

​        {

​          Console.WriteLine("a idade em dias é: "+idade);

​        }

​        if(forma=="M")

​        {

​          idadeD=(30*idade);

​          Console.WriteLine("Esta idade em dias é "+idadeD);

​        }

​        if(forma=="A"){

​          idadeD=(365*idade);

​          Console.WriteLine("Esta idade em dias é: "+idadeD);

​        }        

​      }

​    }

  }



#### Escreva um programa para ler o número total de eleitores de um município, o número de votos brancos, nulos e válidos. Calcular e escrever o percentual que cada um representa em relação ao total de eleitores.
using System;

  namespace ListaExerci

  {

​    class Exercicio

​    {

​      static void Main(string[] args)

​      {

​        int totalEleitores; 

​        int votosValidos, votosBrancos, votosNulos;

​        double votosValidosPerc, votosBrancosPerc, votosNulosPerc;

​        Console.WriteLine("Informe o total de Eletores: ");

​        totalEleitores=Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("Informe o total de votos Válidos: ");

​        votosValidos=Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("Informe o total de votos em Branco: ");

​        votosBrancos=Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("Informe a quantidade de votos Nulos: ");

​        votosNulos=Convert.ToInt32(Console.ReadLine());

​        if(votosValidos==0){

​         votosValidosPerc=0;  

​        }

​        if(votosBrancos==0){

​          votosBrancosPerc=0;

​        }

​        if(votosNulos==0){

​          votosNulosPerc=0;

​        }

​        votosNulosPerc=(votosNulos*100)/totalEleitores;

​        votosBrancosPerc=(votosBrancos*100)/totalEleitores;

​        votosValidosPerc=(votosValidos*100)/totalEleitores;

​        Console.WriteLine("Resumo das Eleiçoes:");

​        Console.WriteLine("Total de Eleitores "+totalEleitores);

​        Console.WriteLine("");

​        Console.WriteLine("Total percentual de votos validos: "+votosValidosPerc+"%");

​        Console.WriteLine("");

​        Console.WriteLine("Total percentual de votos em Branco: "+votosBrancosPerc+"%");

​        Console.WriteLine("");

​        Console.WriteLine("Total percentual de votos Nulos "+votosNulosPerc+"%");

​      }

​    }

  }

#### Escreva um programa para ler o salário mensal atual de um funcionário e o percentual de reajuste. Calcular e escrever o valor do novo salário.
using System;

  namespace ListaExercic1

  {

​    class exercicio

​    {

​      static void Main(string[] args)

​      {

​        double salario, novoSalario;

​        int percentual;

​        Console.WriteLine("Infome o salario atual: ");

​        salario=Convert.ToUInt32(Console.ReadLine());

​        Console.WriteLine("Informe o percentual de reajuste: ");

​        percentual=Convert.ToInt32(Console.ReadLine());

​        novoSalario=((salario*percentual)/100)+salario;

​        Console.WriteLine("Novo salario é: "+novoSalario);

​      }

​    }

  }