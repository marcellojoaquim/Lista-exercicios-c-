# Exercícios Comandos Condicionais

#### Ler um valor e escrever a mensagem É MAIOR QUE 10! se o valor lido for maior que 10, caso contrário escrever NÃO É MAIOR QUE 10!

using System;

  namespace ListaExercici

  {

​    class exercicio

​    {

​      static void Main(string[] args)

​      {

​        double numero;

​        Console.WriteLine("Digite um numero:");

​        numero=Convert.ToInt32(Console.ReadLine());

​        if(numero>10){

​          Console.WriteLine("É MAIOR QUE DEZ!");

​        }else{

​          Console.WriteLine("NÃO É MAIOR QUE DEZ!");

​        }

​      }

​    }

  }



#### Ler um valor e escrever se é positivo ou negativo (considere o valor **zero como positivo**).

  using System;

  namespace listaExercic

  {

​    class exercicio

​    {

​      static void Main(string[] args)

​      {

​        double numero;



​        Console.WriteLine("Digite um numero: ");

​        numero=Convert.ToInt32(Console.ReadLine());



​        if (numero>=0){

​          Console.WriteLine("NUMERO POSITIVO!");

​        }

​      }

​    }

  }



  #### Ler o ano atual e o ano de nascimento de uma pessoa. Escrever uma mensagem que diga se ela poderá ou não votar este ano *(não é necessário considerar o mês em que a pessoa nasceu).*
  using System;

  namespace program

  {

​    class program

​    {

​      static void Main(string[] args)

​      {

​        int anoAtual, anoNasc, idadeMinima;

​        Console.WriteLine("Informe seu ano de Nascimento: ");

​        anoNasc=Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("Informe o ano Atual: ");

​        anoAtual=Convert.ToInt32(Console.ReadLine());   

​        idadeMinima=anoAtual-anoNasc;

​        if(idadeMinima<16){

​          Console.WriteLine("Voce ainda não possue a idade minima para votar.");

​        }else{

​          Console.WriteLine("Parabéns, voce está apto a exercer sua cidadania!");

​        }         

​      }

​    }

  }



  #### Faça um programa para ler: número da conta do cliente, saldo, débito e crédito. Após, calcular e escrever o saldo atual (saldo atual = saldo - débito + crédito). Também testar se saldo atual for maior ou igual a zero escrever a mensagem 'Saldo Positivo', senão escrever a mensagem 'Saldo Negativo'.
  using System;

  namespace listaExercic

  {

​    class exercicio

​    {

​      static void Main(string[] args)

​      {

​        double conta, saldo, credito, debito, saldoAtual;

​        Console.WriteLine("Informe o numero da conta:");

​        conta=Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("Informe o saldo atual de sua conta:");

​        saldo=Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("Informe o valor do credito:");

​        credito=Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("Informa o valor debitado:");

​        debito=Convert.ToInt32(Console.ReadLine());

​        saldoAtual=((saldo-debito)+credito);

​        if(saldoAtual >0){

​          Console.WriteLine("Conta "+conta+" Saldo positivo: "+saldoAtual+"R$");

​        }else if(saldoAtual==0){

​          Console.WriteLine("Conta "+conta+" Conta com valor zero: "+saldoAtual+"R$");

​        }

​        if(saldoAtual<0){

​          Console.WriteLine("Conta "+conta+" Saldo negativo: "+saldoAtual+"R$");

​        }

​      }

​    }

  }



#### Para o enunciado a seguir foi elaborado um algoritmo em Português Estruturado que **contém erros**, identifique os erros no algoritmo apresentado abaixo:
**Enunciado:** Tendo como dados de entrada o nome, a altura e o sexo (M ou F) de uma pessoa, calcule e mostre
seu peso ideal, utilizando as seguintes fórmulas:
\- para sexo masculino: peso ideal = (72.7 * altura) - 58
\- para sexo feminino: peso ideal = (62.1 * altura) - 44.7
  using System;

  namespace program

  {

​    class program

​    {

​      static void Main(string[] args)

​      {

​        double altura, peso_ideal=0;

​        string nome, sexo;

​        Console.WriteLine("Informe seu nome:");

​        nome=Console.ReadLine();

​        Console.WriteLine("Informe seu sexo: M para Masculino e F para Feminino");

​        sexo=Console.ReadLine();

​        Console.WriteLine("Informe sua altura: Utilize a vígula para separar casas decimais.");

​        altura=Convert.ToDouble(Console.ReadLine()); 

​        if(sexo=="M"){

​          peso_ideal=((altura*72.7)-58);

​        }

​        if(sexo=="F"){

​          peso_ideal=(62.1*altura)-44.7;

​        }              

​        Console.WriteLine(peso_ideal);

​      }

​    }

  }



#### Ler dois valores e imprimir uma das três mensagens a seguir:
##### Números iguais’, caso os números sejam iguais
##### Primeiro é maior’, caso o primeiro seja maior que o segundo;
##### Segundo maior’, caso o segundo seja maior que o primeiro.

  using System;

  namespace program

  {

​    class program

​    {

​      static void Main(string[] args)

​      {

​        int num1, num2;

​        num1=Convert.ToInt32(Console.ReadLine());

​        num2=Convert.ToInt32(Console.ReadLine());

​        if(num1==num2){

​          Console.WriteLine("Os numeros são iguais.");

​        }

​        if(num1>num2){

​          Console.WriteLine("O primeiro é maior.");

​        }else if(num1<num2){

​          Console.WriteLine("Segundo numero é maior.");

​        }       

​      }

​    }

  }



#### Escreva um algoritmo que leia o número de litros vendidos e o tipo de combustível *(codificado da seguinte* *forma:* ***A\****-álcool,* ***G\****-gasolina),* calcule e imprima o valor a ser pago pelo cliente sabendo-se que o preço do litro da gasolina é R$ 3,30 e o preço do litro do álcool é R$ 2,90.

#### Atribuir descontos!

  using System;

  namespace listaExercici

  {

​    class exercicio

​    {

​      static void Main(string[] args)

​      {

​        double qtdLitros, gasolina=3.3, alcool=2.9, totalPagar,descontoG, descontoA; 

​        string tipoCombustivel;   

​        Console.WriteLine("Informe o tipo de combustivel: A-alcool ou G-gasolina");

​        tipoCombustivel=Console.ReadLine();

​        Console.WriteLine("Informe a quantidade Litros que deseja comprar: ");

​        qtdLitros=Convert.ToInt32(Console.ReadLine());

​        if ((tipoCombustivel=="G")&&(qtdLitros<=20)){

​          descontoG=(gasolina*0.04);

​          totalPagar=(gasolina-descontoG)*qtdLitros;

​          Console.WriteLine("Total a pagar é: "+totalPagar);

​        } else if((tipoCombustivel=="G")&&(qtdLitros>20)){

​          descontoG=(gasolina*0.06);

​          totalPagar=(gasolina-descontoG)*qtdLitros;

​          Console.WriteLine("Total a pagar é: "+totalPagar);

​        }

​        if ((tipoCombustivel=="A")&&(qtdLitros<=20)){

​          descontoA=alcool*0.03;

​          totalPagar=(alcool-descontoA)*qtdLitros;

​          Console.WriteLine("Total a pagar é: "+totalPagar);

​        } else if((tipoCombustivel=="A")&&(qtdLitros>20)){

​          descontoA=alcool*0.05;

​          totalPagar=(alcool-descontoA)*qtdLitros;

​          Console.WriteLine("Total a pagar é: "+totalPagar);}

​      }

​    }

  }



#### Faça um algoritmo para ler um número que é um código de usuário. Caso este código seja diferente de um código armazenado internamente no algoritmo (igual a 1234) deve ser apresentada a mensagem ‘Usuário inválido!’. Caso o Código seja correto, deve ser lido outro valor que é a senha. Se esta senha estiver incorreta (a certa é 9999) deve ser mostrada a mensagem ‘senha incorreta’. Caso a senha esteja correta, deve ser mostrada a mensagem ‘Acesso permitido’.

  using System;

  namespace listaExercici

  {

​    class exercicio

​    {

​      static void Main(string[] args)

​      {

​        int usuario, senha;

​        Console.WriteLine("Informe o codigo do usuario:");

​        usuario=Convert.ToInt32(Console.ReadLine());

​          if(usuario!=1234){

​            Console.WriteLine("Usuario Invalido! Digite novamente:");

​             usuario=Convert.ToInt32(Console.ReadLine());

​          }if(usuario==1234){

​            Console.WriteLine("Informe a senha:");

​            senha=Convert.ToInt32(Console.ReadLine());

​            if(senha!=9999){

​              Console.WriteLine("Senha incorreta! Digite novamente:");

​              senha=Convert.ToInt32(Console.ReadLine());    

​            }if(senha==9999){

​              Console.WriteLine("Acesso permitido!");

​            }

​          }

​      }

​    }

  }



#### Faça um algoritmo para ler as 3 notas obtidas por um aluno nas 3 verificações e a média dos exercícios que fazem parte da avaliação. Calcular a média de aproveitamento, usando a fórmula abaixo e escrever o conceito do aluno de acordo com a tabela de conceitos mais abaixo:
  using System;

  namespace listaExercic2_31

  {

​    class exercicio

​    {

​      static void Main(string[] args)

​      {

​        double nota1, nota2, nota3, mediaExercicio, mediaAproveitamento;

​        Console.WriteLine("Informe a primeira nota:");

​        nota1=Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("Informe a segunda nota:");

​        nota2=Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("Informe a terceira nota:");

​        nota3=Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("Informe a media dos exercicios");

​        mediaExercicio=Convert.ToInt32(Console.ReadLine());

​        mediaAproveitamento = (nota1+(nota2*2)+(nota3*3)+mediaExercicio)/7;

​        if(mediaAproveitamento>=9){

​          Console.WriteLine("Conceito A");

​        }if((mediaAproveitamento>=7.5)&&(mediaAproveitamento<9)){

​          Console.WriteLine("Conseito B");

​        }if((mediaAproveitamento>6)&&(mediaAproveitamento<7.5)){

​          Console.WriteLine("Conceito C");

​        }if(mediaAproveitamento<6){

​          Console.WriteLine("Conseito D");

​        }

​      }

​    }

  }



#### Uma empresa quer verificar se um empregado está qualificado para a aposentadoria ou não. Para estar em condições, um dos seguintes requisitos deve ser satisfeito:
\- Ter no mínimo 65 anos de idade.
\- Ter trabalhado no mínimo 30 anos.
\- Ter no mínimo 60 anos **e** ter trabalhado no mínimo 25 anos.
Com base nas informações acima, faça um algoritmo que leia: o número do empregado (código), o ano
de seu nascimento e o ano de seu ingresso na empresa. O programa deverá escrever a idade e o tempo
de trabalho do empregado e a mensagem 'Requerer aposentadoria' ou 'Não requerer'.


  using System;

  namespace ListaExercici

  {

​    class exercicio

​    {

​      static void Main(string[] args)

​      {

​        int anoAtual=2021, tempoDeTraba, matricula, nascimento, admissao, idade;

​        Console.WriteLine("Informe o numero de sua matricula:");

​        matricula=Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("Informe sua data de nascimento: ");

​        nascimento=Convert.ToInt32(Console.ReadLine());

​        Console.WriteLine("Informe o ano de admissão:");

​        admissao=Convert.ToInt32(Console.ReadLine());

​        idade=anoAtual-nascimento;

​        tempoDeTraba=anoAtual-admissao;

​        if(idade>=65){

​          Console.WriteLine("Matricula "+matricula+" Requerer Aposentadoria!");

​        } else if((idade>=60)&&(tempoDeTraba>=25)){

​          Console.WriteLine("Matricula "+matricula+" Requerer Aposentadoria!");

​        } else if(tempoDeTraba>=30){

​          Console.WriteLine("Matricula "+matricula+" Requerer Aposentadoria!");           

​        }else{

​          Console.WriteLine("Matricula "+matricula+" Não Requerer Aposentadoria!");

​        }

​      }

​    }

  }