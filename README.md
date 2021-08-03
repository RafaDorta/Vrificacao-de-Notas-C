# Vrificacao-de-Notas-C-
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <ctype.h>

int main()
{

    int ra[100], i, malu, passou = 0, alunosqpassaram[100], n=0;
    float nota[100];
    char alunos[100][60];
    printf("Quantos alunos ser\306o avaliados: ");
    scanf("%d", &malu);
    fflush(stdin);
    system("cls");
    for(i=0; i<malu; i++){
    printf("Nome do aluno: ");
    gets(alunos[i]);
    fflush(stdin);
    printf("RA: ");
    scanf("%d", &ra[i]);
    fflush(stdin);
    printf("Nota do %s: ", alunos[i]);
    scanf("%f", &nota[i]);
    fflush(stdin);
    if(nota[i] >= 5){
        passou++;
        alunosqpassaram[n]=i;
        n++;
    }
    printf("==========================================\n");
    }
    printf("            RELATORIO FINAL\n");
    printf("\n");
    printf("       %d alunos passaram na prova\n", passou);
    printf("==========================================\n");
    for(i=0;i<passou; i++){
    printf("       Nome: %s\n", alunos[alunosqpassaram[i]]);
    printf("       RA: %d\n", ra[alunosqpassaram[i]]);
    printf("       Nota:%.2f\n", nota[alunosqpassaram[i]]);
    printf("==========================================\n");

    }
    printf("\n\n\n");
    return 0;
}
