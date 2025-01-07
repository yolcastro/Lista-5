#include <stdio.h>

int main() {
    int x, y, z;
    int *px, *py, *pz;

    printf("Digite o primeiro valor:\n");
    scanf("%d", &x);
    
    printf("Digite o segundo valor:\n");
    scanf("%d", &y);
    
    px = &x;
    py = &y;

    printf("[%p] %d\n", px, *px);
    printf("[%p] %d\n", py, *py);

    pz = px;
    px = py;
    px = pz;

    puts("Após a troca:");
    printf("[%p] %d\n", px, *px);
    printf("[%p] %d\n", py, *py);

    return 0;
}
