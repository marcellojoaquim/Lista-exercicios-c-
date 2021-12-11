# Exercícios Vetor

#### Escreva um programa que permita a leitura dos nomes de 10 pessoas e armaze-os nomes lidos em um vetor. Após isto, o programa deve permitir a leitura de mais 1 nome qualquer de pessoa e depois escrever a mensagem ACHEI, se o nome estiver entre os 10 nomes lidos anteriormente (guardados no vetor), ou NÃO ACHEI caso contrário.

using System;
using System.Linq;
 namespace listaExercicio_4
 {
 class exercicio
 {
 static void Main(string[] args)
 {
 string[] nomes=new string[10];
 string nome;
 Console.WriteLine("Informes a lista nomes:");
 for(int i=0; i<10; i++){
 nomes[i]=Console.ReadLine();
  }
 Console.WriteLine("Certo, agora informe um outro nome qualquer: ");
 nome=Console.ReadLine();
 for(int i=0; i<10; i++){
 if(nomes[i]==nome){
 Console.WriteLine("Achei!");
 break;
 }else if(nomes[i]!=nome){
 Console.WriteLine("Não achei!");
 break;
 }
 }
 }
 }
 }

####  Escreva um programa que permita a leitura das notas de uma turma de 20 alunos. Calcular a média da turma e contar quantos alunos obtiveram nota acima desta média calculada. Escrever a média da turma e o resultado da contagem.

using System;
using System.Linq;
 namespace listaExercicio
 {
 class exercicio
 {
 static void Main(string[] args)
 {
 double[] notas= new double[20];
 double media=0, cont=0, soma;
 Console.WriteLine("Informe as notas dos alunos:");
 for(int i=0; i<20; i++){
 notas[i]=Convert.ToDouble(Console.ReadLine());
 }
 soma=notas.Sum();
 media=soma/notas.Length;
 for(int i=0; i<20; i++)
 {
 if(notas[i]> media){
 cont++;
 }
 }
 Console.WriteLine("media da turma: "+media);
  Console.WriteLine("Numero de alunos acima da média: "+cont);
 }
 }
 }

####  Ler um vetor Q de 20 posições (aceitar somente números positivos). Escrever a seguir o valor do maior elemento de Q e a respectiva posição que ele ocupa no vetor.

using System;
using System.Linq;
 namespace listaexercicio
 {
 class exercicio
 {
 static void Main(string[] args)
 {
 int[] Q= new int[20];
 int maior=0, posicao=0;
 Console.WriteLine("Informe a sequancia de numeros inteiro e positivos: ");
 for(int i=0; i<20; i++){
 Q[i]=Convert.ToInt32(Console.ReadLine());
 if(i == 0 ){
 maior=Q[i];
 posicao=i;
 }else if(Q[i]>maior){
 maior=Q[i];
 posicao=i;
 }
 }
  Console.WriteLine("Maior elemento do vetor: "+maior);
 Console.WriteLine("Aposição que ele ocupa no vetor é: "+posicao);
}
 }
 }

#### O mesmo exercício anterior, mas agora deve escrever o menor elemento do vetor e a respectiva posição dele nesse vetor.

using System;
using System.Linq;
 namespace listaexercicio
 {
 class exercicio
 {
 static void Main(string[] args)
 {
 int[] Q= new int[20];
 int menor=0, posicao=0;
 Console.WriteLine("Informe a sequancia de numeros inteiro e positivos: ");
 for(int i=0; i<20; i++){
 Q[i]=Convert.ToInt32(Console.ReadLine());
 if(i == 0 ){
 menor=Q[i];
 posicao=i;
 }else if(Q[i]<menor){
 menor=Q[i];
 posicao=i;
 }
 }
 Console.WriteLine("O menor valor é: "+menor);
 Console.WriteLine("A posição que ele ocupa é: "+posicao);
}
 }
 }

####  Ler um vetor A de 10 números. Após, ler mais um número e guardar em uma variável X. Armazenar em um vetor M o resultado de cada elemento de A multiplicado pelo valor X. Logo após,imprimir o vetor M.

using System;
using System.Linq;
 namespace listaexercicio
 {
 class exercicio
 {
 static void Main(string[] args)
 {
 double[] A= new double[10];
 double[] M= new double[10];
 double x;
 Console.WriteLine("Digite os numeros: ");
 for(int i=0; i<10;i++){
 A[i]=Convert.ToDouble(Console.ReadLine());
 }
 Console.WriteLine("Digite o numero da variavel 'X': ");
 x=Convert.ToDouble(Console.ReadLine());
 for(int i=0; i<10; i++){
 M[i]=A[i]*x;
  }
  for(int i=0; i<10; i++)
 {
 Console.Write(M[i]+" ");
 }
 }
 }
 }

#### Faça um programa para ler 20 números e armazenar em um vetor. Após a leitura total dos 20 números, o programa deve escrever esses 20 números lidos na ordem inversa.

using System;
using System.Linq;
 namespace listaexercicio
 {
 class exercicio
 {
 static void Main(string[] args)
 {
 double[] num= new double[20];
 Console.WriteLine("Digite os numeros: ");
 for(int i=0; i<20; i++){
 num[i]=Convert.ToDouble(Console.ReadLine());
 }
 for(int i = 19; i>-1; i--){
 Console.Write(num[i]+" ");
 }
  }
 }
 }

#### Faça um programa para ler um valor N qualquer (que será o tamanho dos vetores). Após, ler dois vetores A e B (de tamanho N cada um) e depois armazenar em um terceiro vetor Soma a soma dos elementos do vetor A com os do vetor B (respeitando as mesmas posições) e escrever o vetor Soma.

using System;
using System.Linq;
 namespace listaexercicio
 {
 class exercicio
 {
 static void Main(string[] args)
 {
 int N=0;
 Console.WriteLine("Informe o valor de 'N' que definira o tamanho o array 'A'e 'B'.");
 N=Convert.ToInt32(Console.ReadLine());
 int[] A = new int[N];
 int[] B = new int[N];
  int[] soma = new int[N];
 Console.WriteLine("Informe os valores do array 'A': ");
 for(int i=0; i<N; i++){
 A[i]= Convert.ToInt32(Console.ReadLine());
 }
 Console.WriteLine("Informe os valores do array 'B': ");
 for(int i=0; i<N; i++){
 B[i]= Convert.ToInt32(Console.ReadLine());
 }
  Console.WriteLine("Resultado do somatório dos vetores:");
 for(int i=0; i<N; i++){
 soma[i] = A[i]+B[i];
 Console.WriteLine(soma[i]);
 }
 }
 }
 }

 #### Faça um programa para ler e armazenar em um vetor a temperatura média de todos os dias do ano. Calcular e escrever:
##### a) Menor temperatura do ano
##### b) Maior temperatura do ano
##### c) Temperatura média anual
##### d) O número de dias no ano em que a temperatura foi inferior a média anual

using System;
using System.Linq;
 namespace listaexercicio
 {
 class exercicio
 {
 static void Main(string [] args)
 {
 double[] temp= new double[365];
 double media, tempMaior, tempMenor;
 int tempMenorMedia=0;
 Console.WriteLine("Informe as temperaturas diárias: ");
 for(int i=0; i<365; i++){
 temp[i]=Convert.ToDouble(Console.ReadLine());
 }
 tempMaior=temp.Max();
 tempMenor=temp.Min();
 media=temp.Sum()/temp.Length;
 foreach (double T in temp)
 {
 if(T<media){
 tempMenorMedia++;
 }
 } 
 Console.WriteLine("Menor temperatura registrada: "+tempMenor);
 Console.WriteLine("Maior temperatura registrada: "+tempMaior);
 Console.WriteLine("Média de temperatura anual "+media);
 Console.WriteLine("Números de dias que a temperatura foi menor que a media: "+tempMenorMedia);
 }
 }
 }

#### Faça um programa para ler 10 números e armazenar em um vetor. Após isto, o programa deve ordenar os números no vetor em ordem crescente. Escrever o vetor ordenado.

using System;
using System.Linq;
 namespace listaexercicio
 {
 class exercicio
 {
 static void Main(string[] args)
 {
 int[] numero= new int[10];
 Console.WriteLine("Informe a sequencia de números: ");
 for(int i=0; i<10; i++){
 numero[i]=Convert.ToInt32(Console.ReadLine());
 }
 Array.Sort(numero);
 Console.WriteLine("Ordem Crescente ");
 foreach (int N in numero)
 {
 Console.WriteLine(N);
 }
 }
 }
 }

#### O mesmo exercício anterior, mas depois de ordenar os elementos do vetor em ordem crescente, deve ser lido mais um número qualquer e inserir esse novo número na posição correta, ou seja,mantendo a ordem crescente do vetor.

using System;
using System.Linq;
 namespace listaexercicio
 {
 class exercicio
 {
 static void Main(string[] args)
 {
 int[] numero= new int[10];
 int ordem;
 Console.WriteLine("Digite os numeros do vetor:");
 for(int i=0; i<10; i++)
 {
 numero[i]=Convert.ToInt32(Console.ReadLine());
 }
 Console.WriteLine("Em Ordem:");
 Array.Sort(numero);
 foreach (int N in numero)
  {
 Console.WriteLine(N);
 }
 Console.WriteLine("Insira um novo número no vetor:");
 numero[1]=Convert.ToInt32(Console.ReadLine());
 Array.Sort(numero);
  Console.WriteLine("Em Ordem com o novo número: ");
 foreach (int N2 in numero)
 {
 Console.WriteLine(N2);
 }
 }
 }
 }

#### Faça um programa para ler um vetor de 20 números. Após isto, deverá ser lido mais um número qualquer e verificar se esse número existe no vetor ou não. Se existir, o programa deve gerar um novo vetor sem esse número. (Considere que não haverão números repetidos no vetor).

using System;
using System.Linq;
 namespace listaexercicio
 {
 class exercicio
 {
 static void Main(string[] args)
 {
 int[] V= new int[20];
  int num;
 Console.WriteLine("Informe os numeros do Array: ");
 for(int i=0; i<20; i++)
 {
 V[i]=Convert.ToInt32(Console.ReadLine());
 }
 Console.WriteLine("Informe um número qualquer: ");
 num=Convert.ToInt32(Console.ReadLine());
 for(int i =0; i<20; i ++)
 {
 if(num==V[i]){
 continue;
  }
 Console.Write(V[i]+" ");
 }
 }
 }
 }

#### Faça um programa para ler dois vetores V1 e V2 de 15 números cada. Calcular e escrever a quantidade de vezes que V1 e V2 possuem os mesmos números e nas mesmas posições.

using System;
using System.Linq;
 namespace listaexercicio
 {
 class exercicio
 {
 static void Main(string[] args)
 {
 int[] V1= new int[15];
 int[] V2= new int[15];
 int cont=0;
  Console.WriteLine("Informes os numeros de V1: ");
 for(int i=0; i<15; i++)
 {
 V1[i]=Convert.ToInt32(Console.ReadLine());
 }
 Console.WriteLine("Informes os numeros de V2: ");
 for(int j=0; j<15; j++)
 {
 V2[j]=Convert.ToInt32(Console.ReadLine());
 }
 for(int i=0; i<15; i++)
 {
 for(int j=0; j<15; j++)
  {
 if((V1[i]==V2[j])&&(i==j)){
 cont++;
 }
 }
 }
Console.WriteLine("Quantidade de vezes que V1 e V2 possuem os mesmos números e nas mesmas posições: "+cont);
 }
 }
 }

#### Faça um programa para ler um vetor de 30 números. Após isto, ler mais um número qualquer, calcular e escrever quantas vezes esse número aparece no vetor.

using System;
using System.Linq;
 namespace listaexercicio
 {
 class exercicio
 {
  static void Main(string[] args)
 {
 double[] Vetor=new double[30];
 double num;
 int cont=0;
 Console.WriteLine("Informe os números do Array: ");
  for(int i=0; i<30; i++)
 {
 Vetor[i]=Convert.ToInt32(Console.ReadLine());
 }
 Console.WriteLine("Informe um número qualquer: ");
 num=Convert.ToDouble(Console.ReadLine());
 for(int i=0; i<30; i++)
 {
 if(Vetor[i]==num){
 cont++;
 }
  }
 Console.WriteLine("Qtd de vezes que o número 'num' aparece no Vetor: "+cont);
 }
 }
 }

####  Faça um programa para ler 50 números e armazenar em um vetor VET, verificar e escrever se existem números repetidos no vetor VET e em que posições se encontram.

using System;
using System.Linq;
 namespace listaexercicio
 {
 class exercicio
 {
 static void Main(string[] args)
 {
  int[] VET= new int[50];
 Console.WriteLine("Digite os números: ");
 for(int i=0; i<50; i++)
 {
 VET[i]=Convert.ToInt32(Console.ReadLine());
 }
 Console.WriteLine("Posição que os números se repetem:");
 for(int i= 0; i<VET.Length; i++)
 {
 for(int j=i; j<VET.Length-1; j++)
 {
 if(VET[i]==VET[j+1])
 {
  Console.WriteLine("Posição: "+i);
 i++;
 }
 }
 }
 }
 }
