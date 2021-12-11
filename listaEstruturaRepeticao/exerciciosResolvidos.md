# Exercícios Estrutura de Repetição

using System;

namespace AvaliacaoLista3

{

  class Program

  {

​    static void Main(string[] args)

​    {      

#### Escreva um algoritmo para imprimir os números de 1 (inclusive) a 10 (inclusive) em ordem crescente.

​      for(int i = 0; i <= 10 ; i++){

​        Console.WriteLine(i);

​      }

#### Escreva um algoritmo para imprimir os números de 1 (inclusive) a 10 (inclusive) em ordem decrescente.

​      for(int i = 10; i >= 0 ; i--){

​        Console.WriteLine(i);

​      }

#### Escreva um algoritmo para imprimir os 10 primeiros números inteiros maiores que 100.

​      for(int i = 101; i <=110; i++){

​        Console.WriteLine(i);

​      }

​      //10) Ler um valor N e imprimir todos os valores inteiros entre 1 (inclusive) e N (inclusive). Considere que o N

​      //será sempre maior que ZERO.

​      Console.WriteLine("Digite um valor inteiro maior que zero");

​      int escolha = int.Parse(Console.ReadLine());      

​      if(escolha == 0){

​        Console.WriteLine("Digite valor maior que zero");

​      }else{

​        for(int i = 1; i <= escolha; i++){

​          Console.WriteLine(i);

​        }

​      }

#### Modifique o exercício anterior para aceitar somente valores maiores que 0 para N. Caso o valor informado (para N) não seja maior que 0, deverá ser lido um novo valor para N.

​      Console.WriteLine("Digite um valor inteiro maior que zero");

​      int nEscolha = int.Parse(Console.ReadLine());      

​      while(nEscolha == 0){

​          Console.WriteLine("Digite novamente valor maior que zero");

​          nEscolha = int.Parse(Console.ReadLine());  

​      }

​      if(nEscolha !=0){

​        for(int i = 1; i <= nEscolha; i++){

​          Console.WriteLine(i);

​        }

​      }

#### Escreva um algoritmo que calcule e imprima a tabuada do 8 (1 a 10).

​      for(int i = 1; i <= 10; i++){

​        Console.WriteLine(i * 8);

​      }

#### Ler um valor inteiro (aceitar somente valores entre 1 e 10) e escrever a tabuada de 1 a 10 do valor lido.

​      Console.WriteLine("Escreva um valor de 1 a 10");

​      int escolhaT = int.Parse(Console.ReadLine());

​      for(int i = 1; i<= 10; i++){

​        Console.WriteLine(i*escolhaT);

​      }

#### Ler 10 valores e escrever quantos desses valores lidos são NEGATIVOS.

​      Console.WriteLine("Digite 10 valores separado por virgula. EX: 10,-5,1,5,10,20");

​      string[] valores = Console.ReadLine().Split(",");

​      int negativo = 0;

​      for(int i = 0; i< valores.Length; i++){

​        int valor = int.Parse(valores[i]);

​        if(valor < 0){

​          negativo++;

​        }

​      }

​      Console.WriteLine($"Foram {negativo} numero negativos");



#### Ler 10 valores e escrever quantos desses valores lidos estão no intervalo [10,20] (inlcuindo os valores 10 e 20 no intervalo) e quantos deles estão fora deste intervalo.

​      Console.WriteLine("Digite 10 valores separado por virgula. EX: 10,-5,1,5,10,20");

​      string[] novosValores = Console.ReadLine().Split(",");

​      int intervalo = 0;

​      int foraIntervalo = 0;

​      for(int i = 0; i< novosValores.Length; i++){

​        int valor = int.Parse(novosValores[i]);

​        if(valor >= 10 && valor <= 20){

​          intervalo++;

​        }else{

​          foraIntervalo++;

​        }

​      }

​      Console.WriteLine($"Foram {intervalo} no intervalor de 10 a 20");

​      Console.WriteLine($"Foram {foraIntervalo} fora do intervalo de 10 a 20");



#### Ler 10 valores, calcular e escrever a média aritmética desses valores lidos.

​      Console.WriteLine("Digite 10 valores separado por virgula. EX: 10,1,5,");

​      string[] calValores = Console.ReadLine().Split(",");

​      int valorTotal = 0;

​      for(int i = 0; i< calValores.Length; i++){

​        valorTotal += int.Parse(calValores[i]);

​      }

​      double totaMedia = valorTotal / calValores.Length;

​      Console.WriteLine($"A média total: {totaMedia}");



#### Ler o número de alunos existentes em uma turma e, após isto, ler as notas destes alunos, calcular e escrever a média aritmética dessas notas lidas.

​      Console.WriteLine("Digite a quanitdade de alunos que a turma tem: ");

​      int qtdAluno = int.Parse(Console.ReadLine());

​      double notas = 0;

​      for(int i = 1; i <= qtdAluno; i++){

​        Console.WriteLine("Digite as notas dos alunos");

​        notas += double.Parse(Console.ReadLine());

​      }

​      double mediaTotal = notas / qtdAluno;

​      Console.WriteLine($"Média total da turma é {mediaTotal}");



#### Escreva um algoritmo para ler 10 números e ao final da leitura escrever a soma total dos 10 números lidos.

​      Console.WriteLine("Digite 10 valores separado por virgula. EX: 10,5,1,5,10,20");

​      string[] qtdN = Console.ReadLine().Split(",");

​      double somaTotal = 0;

​      for(int i = 0; i < qtdN.Length; i++){

​        somaTotal += double.Parse(qtdN[i]);

​      }

​      Console.WriteLine($"Soma total dos valores é: {somaTotal}");

​    }

  }

}