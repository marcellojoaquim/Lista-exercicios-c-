#Exercicios Vetor

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
