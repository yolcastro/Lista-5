#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int *alocarMemoria(int n) {
    int *p = NULL;

    if (!(p = (int*) malloc(n * sizeof(int)))) {
        puts("Memória insuficiente");
        exit(1);
    }

    return p;
}

void preencherVetorX(int *p, int n, int mx) {
    for (int k = 0; k < n; k++) {
        *(p + k) = rand() % mx;
    }
}

void preencherVetorF(int *pf, int *px, int nf, int nx) {
    for (int k = 0; k < nf; k++) {
        *(pf + k) = 0;
    }

    for (int j = 0; j < nx; j++) {
        int num = *(px + j);

        if (num >= 0) {
            pf[num]++;
        }
    }  
}

void imprimirVetor(int *p, int n) {
    for (int k = 0; k < n; k++) {
        printf("[%p] %d\n", p + k, *(p + k));
    }
}

int main() {
    int *px;
    int *pf;
    int tam, N;

    srand(time(NULL));
    
    printf("Digite o tamanho do vetor 'X':\n");
    scanf("%d", &tam);

    px = alocarMemoria(tam);
    pf = alocarMemoria(N);

    printf("Digite um 'N' para o intervalo [0, N - 1] do vetor 'X':\n");
    scanf("%d", &N);

    preencherVetorX(px, tam, N);
    preencherVetorF(pf, px, N, tam);

    printf("Vetor 'X':\n");
    imprimirVetor(px, tam);

    preencherVetorF(pf, px, N, tam);

    printf("Vetor 'F':\n");
    imprimirVetor(pf, N);

    free(px);
    free(pf);

    return 0;
}
