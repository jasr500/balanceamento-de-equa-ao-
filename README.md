#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main()
{
    char op;
    int qtde;
    int eqtde[20];
    int pqtde[20];
    char reagente[20][2];
    char produto[20][2];
    int i;
    printf("[A]reagente\n");
    printf("[B]produtos\n");
    printf("[esc] para finalizar\n");
    fflush(stdin);
    op=toupper(getche());
    while(op!=27){
        switch(op){
    case 'A':
        system("cls");
        printf("Digite quantos elementos existe nos reagentes:\n");
        fflush(stdin);
        scanf("%d",&qtde);
        for(i=0;i<qtde;i++){
        printf("%dº elemento do reagente:\n",i+1);
        fflush(stdin);
        gets(reagente[i]);
        printf("digite o coeficiente estequiometrico do %dº elemento:\n",i+1);
        fflush(stdin);
        scanf("%d",&eqtde[i]);
        }
        system("cls");
        printf("o elemento digitado foi:\n");
        for(i=0;i<qtde;i++){
        printf(" %s %d",reagente[i],eqtde[i]);
        }
        getch();

        system("cls");
        break;
    case 'B':
        system("cls");
        for(i=0;i<qtde;i++){
        printf("%dº elemento do reagente:\n",i+1);
        fflush(stdin);
        gets(produto[i]);
        printf("digite o coeficiente estequiometrico do %dº elemento:\n",i+1);
        fflush(stdin);
        scanf("%d",&pqtde[i]);
        }
        system("cls");
        printf("o elemento digitado foi:\n");
        for(i=0;i<qtde;i++){
        printf(" %s %d",produto[i],pqtde[i]);
        }
        getch();

        system("cls");
    break;

    }
    system("cls");
 printf("[A]reagente\n");
    printf("[B]produtos\n");
    printf("[esc] para finalizar\n");
    fflush(stdin);
    op=toupper(getche());

    }
    return 0;
}

