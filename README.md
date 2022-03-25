Aluno: Henrique Balardin
Turma: 4INF
Ano: 2022

# IFSUL-Calculadora-C#
Atividade para o IFSUL. Calculadora feita em C#

```C#
using System;

namespace Calculator{
	public class Program
	{
		public static void Main()
		{
			Selector();
		}
		
		public static void Selector(){
			Console.WriteLine("============ Calculadora do Balada =============");
			Console.WriteLine("Escolha uma das opções");
			Console.WriteLine("1 - Adição");
			Console.WriteLine("2 - Subtração");
			Console.WriteLine("3 - Divisão");
			Console.WriteLine("4 - Multiplicação");
			
			int option = int.Parse(Console.ReadLine());
			
			while (option < 1 || option > 4){
				Console.WriteLine("Por favor escolha uma opção válida");
				option = int.Parse(Console.ReadLine());
			}
			
			Console.WriteLine("Digite o primeiro valor");
			double n1 = double.Parse(Console.ReadLine());
			
			Console.WriteLine("Digite o segundo valor");
			double n2 = double.Parse(Console.ReadLine());
			
			if (option == 1){
				Sum(n1, n2);
			}
			if (option == 2){
				Subtract(n1, n2);
			}
			if (option == 3){
				Divide(n1, n2);
			}
			if (option == 4){
				Multiply(n1, n2);
			}
			
			Console.WriteLine();
			Console.WriteLine("Obrigado pela preferência! ;)");
			Console.WriteLine("=================================================");
		}
		
		public static void Sum(double n1, double n2){
			double result = n1 + n2; 
			Console.WriteLine("O resultado da soma dos dois valores é " + result);
		}
		
		public static void Subtract(double n1, double n2){
			double result = n1 - n2; 
			Console.WriteLine("O resultado da subtração dos dois valores é " + result);
		}
		
		public static void Divide(double n1, double n2){
			double result = n1 / n2; 
			Console.WriteLine("O resultado da divisão dos dois valores é " + result);
		}
		
		public static void Multiply(double n1, double n2){
			double result = n1 * n2; 
			Console.WriteLine("O resultado da multiplicação dos dois valores é " + result);
		}
	}
}

```
