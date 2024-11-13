# Projeto-Menu
Função que desenhará uma linha na tela.

  {
            Console.WriteLine("===============================================");
        }
        static void Main(string[] args)
        {
            bool inicio = false;
            while (inicio = true)
            {
                Console.Clear();
                int op;

  //criaremos conexões com os arq's (classes)
                ClasseConverteString converte = new ClasseConverteString();
                ClasseOrdena ordena = new ClasseOrdena();

  Linha();
                //trabalharemos com posicionamento do cursor
                Console.SetCursorPosition(15, 1);
                Console.WriteLine("Menu de Opções");
                Linha();
                Console.SetCursorPosition(10, 4);
                Console.WriteLine("1 - Conversão de Strings");
                Console.SetCursorPosition(10, 6);
                Console.WriteLine("2 - Ordenar Numeros");
                Console.SetCursorPosition(10, 8);
                Console.WriteLine("3 - Finalizar - Sair");
                Console.SetCursorPosition(15, 11);
                Console.WriteLine("Opção[ ]");
                Console.SetCursorPosition(21, 11);

  try
                {
                    op = Convert.ToInt32(Console.ReadLine());
                    if (op == 1)
                    {
                        Console.WriteLine("A conversão da frase ->" + converte.entradaDados());
                    }
                    if (op == 2)
                    {
                        ordena.Organizar();//complementa
                    }
                    if (op == 3)
                    {
                        Console.Clear();
                        inicio = true;
                        Console.WriteLine("++++Fim de Execução++++");
                    }
                    else if (op != 1 && op != 2 && op != 3)
                    {
                        Console.WriteLine("++++++Opção Invalida!++++++");
                    }


  }
                catch (Exception ex)
                {
                    Console.Clear();
                    Linha();
                    Console.WriteLine("Insira uma das opções acima!");
                    Linha();
                }
                Console.ReadKey();
            }
        }
    }
}
