# sistema-de-lanchonet
Este projeto é um programa simples em C# que simula o sistema de pedidos de bebidas em uma lanchonete. O
usuário pode escolher bebidas de um cardápio, adicionar ao pedido e no final ver o valor total da compra.
É um exercício prático para treinar a estrutura switch case e o uso de loops.
Funcionalidades
Exibe um menu de bebidas com preços.
Permite que o usuário escolha quantas bebidas quiser.
Calcula o valor total do pedido automaticamente.
Finaliza o pedido ao selecionar a opção “Sair/Finalizar".
Cardápio de Bebidas 1 - Coca-Cola (R$ 5,00) 2 - Suco de Laranja (R$ 6,00) 3 - Água (R$ 3,00) 4 - Café (R$ 4,00) 5-
Finalizar pedido


using System;

class Program
{
	static void Main()
	{
		int opcao;
		double total = 0;

		do
		{
			Console.WriteLine("\n===== LANCHONETE =====");
			Console.WriteLine("1 - Coca-Cola (R$ 5,00)");
			Console.WriteLine("2 - Suco de Laranja (R$ 6,00)");
			Console.WriteLine("3 - Água (R$ 3,00)");
			Console.WriteLine("4 - Café (R$ 4,00)");
			Console.WriteLine("5 - Finalizar Pedido");
			Console.WriteLine("===============================");

			Console.Write("Escolha uma opção: ");
			opcao = int.Parse(Console.ReadLine());

			switch (opcao)
			{
				case 1:
					Console.WriteLine("Coca-Cola adicionada ao pedido.");
					total += 5.00;
					break;

				case 2:
					Console.WriteLine("Suco de Laranja adicionado ao pedido");
					total += 6.00;
					break;

				case 3:
					Console.WriteLine("Água adicionada ao pedido");
					total += 3.00;
					break;

				case 4:
					Console.WriteLine("Café adicionado ao pedido ");
					total += 4.00;
					break;

				case 5:
					Console.WriteLine("\nFinalizando pedido...");
					break;

				default:
					Console.WriteLine("Opção inválida!");
					break;
			}

		} while (opcao != 5);

		
		Console.WriteLine($"Valor total do pedido: R$ {total:F2}");

		Console.WriteLine("Obrigado pela preferência!");
	}
}
