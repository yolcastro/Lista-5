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

void preencherVetorY(int *px, int *py, int n) {
     printf("Valores de 'r':\n");
     
     for (int k = 0; k < n; k++) {
        int r = rand() % 11;
        printf("r[%d] = %d\n", k, r);

        if (r > 0 && r <= 3) {
            *(py + k) = *(px + k);
        }
        else if (r > 3 && r <= 5) {
            *(py + k) = *(px + k) - 1;
        }
        else if (r > 5 && r <= 7) {
            *(py + k) = *(px + k) + 1;
        }
        else if (r > 8 && r <= 9) {
            *(py + k) = *(px + k) - 2;
        }
        else if (r > 9 && r <= 10) {
            *(py + k) = *(px + k) + 2;
        }
    }
}

void zerarMatriz(int *m, int n) {
    for (int k = 0; k < n * n; k++) {
        *(m + k) = 0;
    }
}

void preencherMatriz(int *m, int *px, int *py, int nxy, int N) {
    for (int k = 0; k < nxy; k++) {
        int lin = *(px + k);
        int col = *(py + k);

        m[lin * N + col]++;
    }
}

void imprimirVetor(int *p, int n) {
    for (int k = 0; k < n; k++) {
        printf("[%p] %d\n", p + k, *(p + k));
    }
}

void imprimirMatriz(int *m, int N) {
    for (int k = 0; k < N; k++) {
        for (int j = 0; j < N; j++) {
            printf("%3d ", m[k * N + j]);
        }
        printf("\n");
    }
}

int main() {
    int *px;
    int *py;
    int *m;
    int tam, N;

    srand(time(NULL));

    printf("Digite o tamanho dos vetores 'X' e 'Y':\n");
    scanf("%d", &tam);

    px = alocarMemoria(tam);
    py = alocarMemoria(tam);

    printf("Digite um 'N' para o intervalo [0, N - 1] do vetor 'X':\n");
    scanf("%d", &N);

    m = alocarMemoria(N * N);

    preencherVetorX(px, tam, N);
    preencherVetorY(px, py, tam);
    zerarMatriz(m, N);

    printf("Vetor 'X':\n");
    imprimirVetor(px, tam);
    printf("Vetor 'Y':\n");
    imprimirVetor(py, tam);

    preencherMatriz(m, px, py, tam, N);

    printf("Matriz 'M':\n");
    imprimirMatriz(m, N);

    free(px);
    free(py);
    free(m);

    return 0;
}
