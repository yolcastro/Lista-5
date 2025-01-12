#include <stdio.h>
#include <string.h>

#define TAM 100

int main() {
    char str[TAM];
    int x;
    int *p;

    printf("Escreva algo:\n");
    fgets(str, TAM, stdin);
    
    str[strcspn(str, "\n")] = '\0';
    
    x = strlen(str);

    p = &x;

    printf("[%p] %d\n", p, *p);

    return 0;
}
