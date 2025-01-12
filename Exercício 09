#include <stdio.h>
#include <stdlib.h> 
#include <time.h>

#define MX 100;

int *alocarMemoria(int qtd) {
    int *p = NULL;

    if (!(p = (int*) malloc(qtd * sizeof(int)))) {
        puts("Memória insuficiente");
        exit(1);
    }

    return p;
}

void preencherVetor(int *pv, int qtd) {
    for (int k = 0; k < qtd; k++) {
        *(pv + k) = rand() % MX;
    }
}

void imprimirVetor(int *pv, int qtd) {
    for (int k = 0; k < qtd; k++) {
        printf("[%p] %d\n", pv + k, *(pv + k));
    }
}

void bubbleSort(int *pv, int n) {
    int k, j, temp;

    for (k = n - 1; k > 0; k--) {
        for (j = 0; j < k; j++) {
            if (*(pv + j) > *(pv + (j + 1))) {
                temp = *(pv + j);
                *(pv + j) = *(pv + (j + 1));
                *(pv + (j + 1)) = temp;
            }
        }
    }
}

int main() {
    int *pv;
    int n;

    srand(time(NULL));

    printf("Escreva a quantidade de elementos do vetor:\n");
    scanf("%d", &n);

    pv = alocarMemoria(n);

    preencherVetor(pv, n);
   
    printf("Elementos dos vetores antes de serem ordenados:\n");
    imprimirVetor(pv, n);

    bubbleSort(pv, n);

    printf("Após serem ordenados:\n");
    imprimirVetor(pv, n);

    free(pv);

    return 0;
}
