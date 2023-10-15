# Bilheteria-museu

#include <stdlib.h>
#include <stdio.h>
#include <conio.h>
#include <time.h>
#include <locale.h>
#include <windows.h>

int main(void)
{
    setlocale(LC_ALL, "Portuguese_Brazil");
    int  num, pagamento, museu1, quantidade, introducao;
    float preco_total;
    float museu_inteira = 10.0;
    float museu_meia = 5.0;
    char nome[5];

    printf("\tInforme o seu nome: ");
    scanf("\t\n\n%s", nome);
    system("cls");
    printf("\tOlá %s, é uma prazer recebe-lo(a) em nosso Museu!!!\n", nome);


    printf("\t---------------------------------------\n");
    printf("\t SELECIONE O TIPO DE INGRESSO: \n\n");


    do
    {
        printf("\t [1]Inteira: 10,00 R$ \n");
        printf("\t [2]Meia: 5,00 R$ \n");
        scanf("%i",&museu1); //variavel forma de pagament
        if (museu1 == 0)  //se o usuário digitar nenhum dos numeros espepcificados
        {
            museu1 = 3;
        }
        if (museu1 > 2)
        {
            printf("Opção invalida, tente novamente.\n"); // repetição até ele digitar corretamente
        }

    }
    while(museu1 > 2 );
    (museu1 < 1);
    printf("\t---------------------------------------\n");


    printf("Quantos ingressos você deseja comprar? ");
    scanf("%d", &quantidade);


    if ( museu1 ==1 ) //se ele escolher ingresso inteira
    {
        float preco_total = quantidade * museu_inteira;
        printf(" Preço total: R$%.2f\n", preco_total);
    }

    if ( museu1 ==2 )  //se ele escolher ingresso meia
    {
        float preco_total = quantidade * museu_meia;
        printf(" Preço total: R$%.2f\n", preco_total);
    }


    for( ; ;)
    {
        printf("\n\n\tQual será a forma de pagamento?\n\t[1] PIX\n\t[2] Dinheiro\n\t[3] Débito\n\t[4] Crédito\n");
        scanf("%d", &pagamento);
        if (pagamento == 1)
        {
            system("cls");

            printf("\tPagamento sendo processado...\n");
            Sleep(3000);
            system("cls");
            printf("\tPagamento aprovado!\n");
            printf("\tGerando seu Token...\n");
            Sleep(1000);
            break;
        }
        if (pagamento == 2)
        {
            system("cls");

            printf("\tPagamento sendo processado...\n");
            Sleep(3000);
            system("cls");
            printf("\tPagamento aprovado!\n");
            printf("\tGerando seu Token...\n");
            Sleep(1000);
            break;
        }

        if (pagamento == 3)
        {
            system("cls");

            printf("\tPagamento sendo processado...\n");
            Sleep(3000);
            system("cls");
            printf("\tPagamento aprovado!\n");
            printf("\tGerando seu Token...\n");
            Sleep(1000);
            break;
        }

        if (pagamento == 4)
        {
            system("cls");

            printf("\tPagamento sendo processado...\n");
            Sleep(3000);
            system("cls");
            printf("\tPagamento aprovado!\n");
            printf("\tGerando seu Token...\n");
            Sleep(1000);
            break;
        }
        else
        {
            printf("\nOpção invalida, tente novamente.\n");
        }
    }


    /* Função srand vai utilizar a leitura do relogio do sistema*/
    srand(time(NULL));
    num = rand() % 100000; /* Função para escolher um numéro aleatória (token)*/
    printf("\n\tSeu token é o N° %d\n", num);

    int verificar;

    printf("\n\n\n\t\t\t\t\t\t\tCarregando...\n");
    Sleep(2000);
    for( ; ; )
    {
        printf("\t\nInforme o seu token: ");
        scanf("%d", &verificar);
        system("cls");
        printf("Validando...");
        Sleep(1500);

        if(verificar != num)
        {
            system("cls");
            Sleep(4000);
            printf("Acesso negado!");
            printf("\n\n\t\t\t\t\t\t\tToken inválido. Tente novamente:     Pedido: N° %d", num);
        }
        else
        {
            printf("\n\t\t\t\t\t\tAcesso autorizado...  ", verificar);
            Sleep(1500);
            printf("\n\t\t\t\t\tSeja bem vindo(a) ao nosso Museu, %s!!!", nome);
            break;
        }
    }

    printf("\n\n\n-----------------------------------------------------------------------------------------\n");

    for ( ; ;){
        printf("O Museu FNSDH apresentará 4 temas, a seguir uma ");
        printf("breve introdução sobre cada um deles...\n");
        printf("\n\n[1] 100 anos da semana da arte\n[2] 150 anos de Santos Dumond\n[3] Jogos Olímpicos de Paris 2024\n[4] Evolução dos Hardwares e Softwares\n");
        scanf("%d", &introducao);

        if(introducao == 1)
        {
            printf("\nA Semana de Arte Moderna é considerada o marco oficial do Modernismo no Brasil. \nEla foi realizada no Theatro \nMunicipal de São Paulo e");
            printf(" \n reuniu artistas de diversas áreas, como pintores, escritores, músicos e escultores, \n");
            printf("para expor suas artes com forte influência das vanguardas europeias.");
            printf("\n\n\n-----------------------------------------------------------------------------------------");
            break;
        }

        if (introducao == 2)
        {
            printf("\nHá 150 anos, nascia no interior de Minas Gerais um dos maiores inventores brasileiros: \nO notável Alberto Santos Dumont,\n");
            printf("considerado um dos precursores da aviação e da criação de aeronaves no mundo.");
            printf("\n\n\n-----------------------------------------------------------------------------------------");
            break;
        }

        if (introducao == 3)
        {
            printf("\nApresentaremos os Jogos Olímpicos de 2024 conhecidos oficialmente como os Jogos da XXXIII Olimpíada,");
            printf("\ncomumente chamado Paris 2024, é um evento multiesportivo futuro a ser realizado no segundo semestre de 2024, na");
            printf("\ncidade de Paris. Será a terceira vez que a cidade será sede dos jogos.\n");
            printf("\n\n\n-----------------------------------------------------------------------------------------");
            break;
        }

        if (introducao == 4)
        {
        printf("\nApresentaremos como o nosso cotidiano mudou e chegou ao patamar que se encontra atualmente,");
        printf("\graças as evoluções dos Softwares e Hardware, mostraremos desde o celular que só fazia ligações até os atuais smartphones.");
        printf("\n\n\n-----------------------------------------------------------------------------------------");
        break;
        }
        else
        {
            printf("\nOpção invalida, tente novamente.\n\n");
        }
    }

}
