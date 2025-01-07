#include <stdio.h>

int main() {
    int x, y, soma = 0;
    int *px, *py, *ps;

    printf("Digite o primeiro valor:\n");
    scanf("%d", &x);
    
    printf("Digite o segundo valor:\n");
    scanf("%d", &y);

    px = &x;
    py = &y;
    ps = &soma;

    *ps = *px + *py;

    printf("[%p] %d\n", ps, *ps);

    return 0;
}
