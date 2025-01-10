#include <stdio.h>
#include <stdlib.h>

void guardarElementos(int *pv, int qtd) {
    for (int k = 0; k < qtd; k++) {
    printf("Insira o elemento %d do vetor:\n", k);
    scanf("%d", &pv[k]);
    }
}

void imprimirVetor(int *pv, int qtd) {
    for (int k = 0; k < qtd; k++) {
        printf("[%p] %d\n", (pv + k), *(pv + k));
    }
}

int main (){
    int n;
    int *pv;
    
    pv = malloc(n * sizeof(int));
    
        if (!pv) {
        puts("Memória insuficiente");
        exit(1);
    }

    printf("Insira a quantidade de elementos do vetor:\n");
    scanf("%d", &n);
    
    guardarElementos(pv, n);
    imprimirVetor(pv, n);

    return 0;
}

//Fiz esse código com valores da categoria "int", mas percebi que os endereços são moldados conforme o tamanho da memória que cada dado ocupa ao alterar para outros tipos.
