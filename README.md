# Programa-PetShop
#include <stdio.h>
#include <stdlib.h>
#define tam 20
#define quant 10
#define banhop 20
#define banhom 30
#define banhog 40
#define tosa 20

    void menuprincipal();
    void menualteracao ();
    void opcaoporte ();
    float banhoetosap(float valor_total);
    float banhoP(float valor_total);
    float banhoetosam(float valor_total);
    float banhoM(float valor_total);
    float banhoetosag(float valor_total);
    float banhoG(float valor_total);


int main()
{

   struct { // Struct de vetores para cadastro
    char nome[tam];
    char cpf[tam];
    char telefone[tam];
    char endereco[tam];
    char nomepet[tam];
    char animal [tam];
    char raca[tam];
    int idade[tam];
    }cadastro[quant];

    int op, op2, op3, op4;
    int i=1, j;
    char porte[tam];
    float valor_total;



    FILE *file;
    file=fopen("C:\\Users\\Jéssica\\OneDrive\\Área de Trabalho\\arquivocadastros.txt", "w");


    system("color F4"); // Função para mudar as cores do fundo e letras
    fprintf(file, "Cadastros realizados");
    while (op!=0){ //Estrutura de repetição do menu
        menuprincipal();
        scanf("%d", &op);
        system("cls"); // Função para limpar a tela

       if (op==1){ // Operação 1 do menu principal

        printf("Realizando Cadastro %d\n", i);
        fprintf(file, "\n Cadastro %d \n \n", i);
        printf("Nome : \t");
        fflush(stdin);
        scanf("%s", cadastro[i].nome);
        fprintf(file,"Nome: %s \n", cadastro[i].nome);

        printf("\nCPF : \t");
        fflush(stdin);
        scanf("%s", cadastro[i].cpf);
        fprintf(file,"CPF: %s \n", cadastro[i].cpf);

        printf("\nTelefone: \t");
        fflush(stdin);
        scanf("%s", cadastro[i].telefone);
        fprintf(file,"Telefone: %s \n", cadastro[i].telefone);

        printf("\nCidade : \t");
        fflush(stdin);
        scanf("%s", cadastro[i].endereco);
        fprintf(file,"Cidade: %s \n", cadastro[i].endereco);

        printf("\nTipo animal (Gato ou Cachorro): \t");
        fflush(stdin);
        scanf("%s", cadastro[i].animal);
        fprintf(file,"Tipo animal: %s \n", cadastro[i].animal);

        printf("\nNome do Pet: \t");
        fflush(stdin);
        scanf("%s", cadastro[i].nomepet);
        fprintf(file,"Nome do Pet: %s \n", cadastro[i].nomepet);

        printf("\nRaca: \t");
        fflush(stdin);
        scanf("%s", cadastro[i].raca);
        fprintf(file,"Raca: %s \n", cadastro[i].raca);

        printf("\nIdade do Pet: \t");
        scanf("%s", cadastro[i].idade);
        fprintf(file,"Idade do Pet: %s \n", cadastro[i].idade);
        fflush(stdin);
        i++;
        system("cls");
       }

       if (op==2){ // Operação 2 do menu
       system("cls");
         for(j=1;j<=quant;j++){
            if(j<i){
            printf("\t ------- Dados do cadastro %d ----------",j);
            printf("\nNome: \t %s\n", cadastro[j].nome);
            printf("\nCPF: \t %s\n", cadastro[j].cpf);
            printf("\nTelefone: \t %s\n", cadastro[j].telefone);
            printf("\nCidade: \t %s\n", cadastro[j].endereco);
            printf("\nNome Pet: \t %s \n", cadastro[j].nomepet);
            printf("\nPet: \t %s\n", cadastro[j].animal);
            printf("\nRaca: \t %s\n", cadastro[j].raca);
            printf("\nIdade: \t %s\n", cadastro[j].idade);
            system("pause");
            system("cls");

            }
        }
       }

       if (op==3){ // Operação 3 do menu
        system("cls");
        menualteracao();
        scanf("%d", &op2);
        system("cls");

        if (op2==1){ // Operação 1 do menu alteração
            system("cls");

            for (j=1;j<=quant;j++){
            if(j<i){
            printf("Alteracao do nome no cadastro ", i);
            printf("\nNome atual: %s", cadastro[j].nome);
            printf("\nNovo nome: \t");
            scanf("%s", cadastro[j].nome);
            printf("O nome foi alterado para %s com sucesso\n!", cadastro[j].nome);
            system("pause");
            system("cls");
            }
        }
    }

    if (op2==2){ // Operação 2 do menu alteração
            system("cls");
            for (j=1;j<=quant;j++){
            if(j<i){
            printf("Alteracao do CPF no cadastro ");
            printf("\nCPF atual: %s", cadastro[j].cpf);
            printf("\nNovo CPF: \t");
            scanf("%s", cadastro[j].cpf);
            printf("O CPF foi alterado para %s com sucesso\n!", cadastro[j].cpf);
            system("pause");
            system("cls");
            }
        }
    }
    if (op2==3){ // Operação 3 do menu alteração
            system("cls");
            for (j=1;j<=quant;j++){
            if(j<i){
            printf("Alteracao do cadastro de Telefone " );
            printf("\nTelefone atual: %s", cadastro[j].telefone);
            printf("\nNovo Telefone: \t");
            scanf("%s", cadastro[j].telefone);
            printf("O telefone foi alterado para %s com sucesso\n!", cadastro[j].telefone);
            system("pause");
            system("cls");
            }
        }
    }


    if (op2==4){ // OPeração 4 do menu alteração
            system("cls");
            for (j=1;j<=quant;j++){
            if(j<i){
            printf("Alteracao da Cidade no cadastro ");
            printf("\nCidade atual: %s", cadastro[j].endereco);
            printf("\nNovo Cidade: \t");
            scanf("%s", cadastro[j].endereco);
            printf("A cidade foi alterado para %s com sucesso\n!", cadastro[j].endereco);
            system("pause");
            system("cls");
            }
        }
    }
    if (op2==5){ //Operação 5 no menu alteração
            system("cls");
            for (j=1;j<=quant;j++){
            if(j<i){
            printf("Alteracao do Pet no cadastro ");
            printf("\nPet atual: %s", cadastro[j].animal);
            printf("\nNovo Pet: \t");
            scanf("%s", cadastro[j].animal);
            printf("O PEt foi alterado para %s com sucesso\n!", cadastro[j].animal);
            system("pause");
            system("cls");
            }
        }
    }
    if (op2==6){ // Operação 6 do menu alteração
            system("cls");
            for (j=1;j<=quant;j++){
            if(j<i){
            printf("Alteracao do cadastro do nome do pet");
            printf("\nNome do pet atual: %s", cadastro[j].nomepet);
            printf("\nNovo nome do Pet: \t");
            scanf("%s", cadastro[j].nomepet);
            printf("O nome do Pet foi alterado para %s com sucesso\n!", cadastro[j].nomepet);
            system("pause");
            system("cls");
            }
        }
    }
    if (op2==7){ // Operação 7 do menu alteração
            system("cls");
            for (j=1;j<=quant;j++){
            if(j<i){
            printf("Alteracao no cadastro do raca ");
            printf("\nRaca atual: %s", cadastro[j].raca);
            printf("\nNova raca do Pet: \t");
            scanf("%s", cadastro[j].raca);
            printf("A raca foi alterado para %s com sucesso\n!", cadastro[j].raca);
            system("pause");
            system("cls");
            }
        }
    }
    if (op2==8){ // Operação 8 do menu alteração
            system("cls");
            for (j=1;j<=quant;j++){
            if(j<i){
            printf("Alteracao do cadastro da idade do Pet");
            printf("\nIdade atual: %s", cadastro[j].idade);
            printf("\nNova idade: \t");
            scanf("%s", cadastro[j].idade);
            printf("A idade foi alterado para %s com sucesso\n!", cadastro[j].idade);
            system("pause");
            system("cls");
            }
        }
    }
       }


    if(op==4){ // OPeração 4 do menu
        system("cls");
        for(j=1;j<=quant;j++){
        if (j<i){
        printf("\t Adicinar banho no animal \n \n");
        printf("\nNome: \t %s\n", cadastro[j].nome);
        printf("\nCPF: \t %s\n", cadastro[j].cpf);
        printf("\nTelefone: \t %s\n", cadastro[j].telefone);
        printf("\nCidade: \t %s\n", cadastro[j].endereco);
        printf("\nNome Pet: \t %s \n", cadastro[j].nomepet);
        printf("\nPet: \t %s\n", cadastro[j].animal);
        printf("\nRaca: \t %s\n", cadastro[j].raca);
        printf("\nIdade: \t %s\n", cadastro[j].idade);
        printf("\n \n Adicionar banho nesse animal ?");
        printf("\n 1 - SIM \t 2 - NAO \n \n");
        scanf("%d", &op3);

        if (op3==1){ // Perguntas da operação 4
            system("cls");
        opcaoporte ();
        scanf("%s", &porte[i]);



        printf("\n No banho com tosa? \n");
        printf("\n 1 - SIM \t 2 - NAO \n \n");
        scanf("%d", &op4);
        system("cls");


        if(porte[i]=='P'){ // Condições para valor final do banho de acordo com o porte
            if(op4==1){
                valor_total= banhoetosap(valor_total);
                printf("\n O valor total a ser pago e: \n Banho + Tosa =  R$ %1.f reais \n\n", valor_total);
                fprintf(file,"\n Realizado Banho + Tosa = R$ %1.f reais \n", valor_total);
                system("pause");
                system("cls");
            }

            if (op4==2){
                valor_total = banhoP(valor_total);
                printf("\nO valor total a ser pago e: \n Banho = R$ %1.f reais \n\n", valor_total);
                fprintf(file,"\n Realizado Banho = R$ %1.f reais \n", valor_total);
                system("pause");
                system("cls");
            }

        }
                if(porte[i]=='M'){ //Condições para valor final do banho de acordo com o porte
            if(op4==1){
                valor_total = banhoetosam(valor_total);
                printf("\nO valor total a ser pago e: \n Banho + Tosa = R$%1.f reais \n\n", valor_total);
                fprintf(file,"\n Realizado Banho + Tosa = R$ %1.f reais \n", valor_total);
                system("pause");
                system("cls");
            }

            if (op4==2){
                valor_total = banhoM(valor_total);
                printf("O valor total a ser pago e: \n Banho = R$ %1.f reais \n\n", valor_total);
                fprintf(file,"\n Realizado Banho = R$ %1.f reais \n", valor_total);
                system("pause");
                system("cls");
            }

        }
          if(porte[i]=='G'){ //Condições para valor final do banho de acordo com o porte
            if(op4==1){
                valor_total = banhoetosag(valor_total);
                printf("\nO valor total a ser pago e:\n Banho + Tosa = R$ %1.f reais \n \n", valor_total);
                fprintf(file,"\n Realizado Banho + Tosa = R$ %1.f reais \n", valor_total);
                system("pause");
                system("cls");
            }

            if (op4==2){
                valor_total = banhoG(valor_total);
                printf("\nO valor total a ser pago e: \n Banho= R$ %1.f reais \n \n ", valor_total);
                fprintf(file,"\n Realizado Banho = R$ %1.f reais \n", valor_total);
                system("pause");
                system("cls");

            }

        }

        }
       if(op3==2){
            system("pause");
           system("cls");

        }
    }
    }
    }
    }

   fclose(file);
    return 0;
}

void menuprincipal (){

     printf("\t------- MENU -------- \n");
        printf("1 - Cadastros \n");
        printf("2 - Consultas \n");
        printf("3 - Alteracoes \n");
        printf("4 - Adicinar Banho\n");
        printf("0 - Sair\n");
}
void menualteracao (){

    printf (" \t Alteracao \n");
        printf ("Escolha uma opcao que deseja alterar \n \n");
        printf ("1 - Nome do Proprietario \n");
        printf ("2 - CPF \n");
        printf ("3 - Telefone\n");
        printf ("4 - Cidade \n");
        printf ("5 - Tipo de Pet \n");
        printf ("6 - Nome do Pet \n");
        printf ("7 - Raca \n");
        printf ("8 - Idade \n");
        printf ("0 - Cancelar \n");

}

void opcaoporte(){
    printf("Adicionando banho \n");
        printf("\nInsira o Porte do animal: \n");
        printf("\n P - Para animais de porte pequeno (de 2kg a 15 kg)");
        printf("\n M - Para animais de porte medio (de 15kg a 25kg)");
        printf("\n G - Para animais de porte grande (superior a 25kg)\n");
}

float banhoetosap(float valor_total){
    valor_total= banhop+tosa;
    return valor_total;
}

float banhoP( float valor_total){
    valor_total= banhop;
    return valor_total;
}
float banhoetosam(float valor_total){
   valor_total = banhom+tosa;
   return valor_total;
}
float banhoM(float valor_total){
    valor_total = banhom;
    return valor_total;
}
float banhoetosag(float valor_total){
   valor_total = banhog+tosa;
   return valor_total;
}
float banhoG(float valor_total){
    valor_total = banhog;
    return valor_total;
}
