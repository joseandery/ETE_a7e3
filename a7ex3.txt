// c#

using System;

class Program
{
    static string nome1, nome2, nome3, nome4, nome5;
    static string poder1, poder2, poder3, poder4, poder5;
    static int pontuacao1, pontuacao2, pontuacao3, pontuacao4, pontuacao5;
    static int equipe1, equipe2, equipe3;
    static int pontuacaoTotal = 0;

    static void Main(string[] args)
    {
        int escolha;

        do
        {
            Console.WriteLine("\nMenu:");
            Console.WriteLine("1. Cadastro de Heróis");
            Console.WriteLine("2. Seleção de Equipe");
            Console.WriteLine("3. Pontuação Total da Equipe");
            Console.WriteLine("4. Exibição da Equipe");
            Console.WriteLine("0. Sair");
            Console.Write("Escolha uma opção: ");
            escolha = int.Parse(Console.ReadLine());

            switch (escolha)
            {
                case 1:
                    cadastrarHeroi();
                    break;
                case 2:
                    selecionarEquipe();
                    break;
                case 3:
                    calcularPontuacaoTotal();
                    break;
                case 4:
                    exibirEquipe();
                    break;
                case 0:
                    Console.WriteLine("Saindo...");
                    break;
                default:
                    Console.WriteLine("Opção inválida! Tente novamente.");
                    break;
            }
        } while (escolha != 0);
    }

    static void cadastrarHeroi()
    {
        if (nome1 != null && nome2 != null && nome3 != null && nome4 != null && nome5 != null)
        {
            Console.WriteLine("Limite de heróis cadastrados alcançado.");
            return;
        }

        Console.WriteLine("Cadastro de Herói:");
        Console.Write("Nome: ");
        string nome = Console.ReadLine();
        Console.Write("Poder: ");
        string poder = Console.ReadLine();
        Console.Write("Pontuação: ");
        int pontuacao = int.Parse(Console.ReadLine());

        if (nome1 == null)
        {
            nome1 = nome;
            poder1 = poder;
            pontuacao1 = pontuacao;
        }
        else if (nome2 == null)
        {
            nome2 = nome;
            poder2 = poder;
            pontuacao2 = pontuacao;
        }
        else if (nome3 == null)
        {
            nome3 = nome;
            poder3 = poder;
            pontuacao3 = pontuacao;
        }
        else if (nome4 == null)
        {
            nome4 = nome;
            poder4 = poder;
            pontuacao4 = pontuacao;
        }
        else if (nome5 == null)
        {
            nome5 = nome;
            poder5 = poder;
            pontuacao5 = pontuacao;
        }

        Console.WriteLine("Herói cadastrado com sucesso!");
    }

    static void selecionarEquipe()
    {
        Console.WriteLine("Seleção de Equipe:");

        if (nome1 == null || nome2 == null || nome3 == null || nome4 == null || nome5 == null)
        {
            Console.WriteLine("Cadastre pelo menos três heróis antes de selecionar a equipe.");
            return;
        }
        
        if(nome1 != null){
            Console.WriteLine($"1. {nome1} - {poder1} - Pontuação: {pontuacao1}");}
        if(nome2 != null){
            Console.WriteLine($"2. {nome2} - {poder2} - Pontuação: {pontuacao2}");}
        if(nome3 != null){
            Console.WriteLine($"3. {nome3} - {poder3} - Pontuação: {pontuacao3}");}
        if(nome4 != null){
            Console.WriteLine($"4. {nome4} - {poder4} - Pontuação: {pontuacao4}");}
        if(nome5 != null){
            Console.WriteLine($"5. {nome5} - {poder5} - Pontuação: {pontuacao5}");}

        Console.Write("Selecione o herói 1: ");
        equipe1 = int.Parse(Console.ReadLine());
        Console.Write("Selecione o herói 2: ");
        equipe2 = int.Parse(Console.ReadLine());
        Console.Write("Selecione o herói 3: ");
        equipe3 = int.Parse(Console.ReadLine());

        Console.WriteLine("Equipe selecionada com sucesso!");
    }

    static void calcularPontuacaoTotal()
    {   
        int p1 = 0, p2 = 0, p3 = 0;
        switch(equipe1){
            case 1: p1 = pontuacao1; break;
            case 2: p1 = pontuacao2; break;
            case 3: p1 = pontuacao3; break;
            case 4: p1 = pontuacao4; break;
            case 5: p1 = pontuacao5; break;
        }
        switch(equipe2){
            case 1: p2 = pontuacao1; break;
            case 2: p2 = pontuacao2; break;
            case 3: p2 = pontuacao3; break;
            case 4: p2 = pontuacao4; break;
            case 5: p2 = pontuacao5; break;
        }
        switch(equipe3){
            case 1: p3 = pontuacao1; break;
            case 2: p3 = pontuacao2; break;
            case 3: p3 = pontuacao3; break;
            case 4: p3 = pontuacao4; break;
            case 5: p3 = pontuacao5; break;
        }
        pontuacaoTotal = p1 + p2 + p3;
        Console.WriteLine($"Pontuação total da equipe: {pontuacaoTotal}");
    }

    static void exibirEquipe()
    {
        Console.WriteLine("Equipe:");
        switch(equipe1){
            case 1: Console.WriteLine(nome1); break;
            case 2: Console.WriteLine(nome2); break;
            case 3: Console.WriteLine(nome3); break;
            case 4: Console.WriteLine(nome4); break;
            case 5: Console.WriteLine(nome5); break;
        }
        switch(equipe2){
            case 1: Console.WriteLine(nome1); break;
            case 2: Console.WriteLine(nome2); break;
            case 3: Console.WriteLine(nome3); break;
            case 4: Console.WriteLine(nome4); break;
            case 5: Console.WriteLine(nome5); break;
        }
        switch(equipe3){
            case 1: Console.WriteLine(nome1); break;
            case 2: Console.WriteLine(nome2); break;
            case 3: Console.WriteLine(nome3); break;
            case 4: Console.WriteLine(nome4); break;
            case 5: Console.WriteLine(nome5); break;
        }
    }
}
