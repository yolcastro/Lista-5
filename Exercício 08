#include <stdio.h>
#include <string.h>

#define TAM 100

void encontrarCaractere(char *str, char c) {
    int encontrado = 0;

    while (*str != '\0') {
        if (*str == c) {
            printf("Caractere [%p] '%c' encontrado.", str, *str);
            encontrado = 1;
            break;
        }
        str++;
    }
    
    if (!encontrado) {
        puts("Caractere não encontrado.");
    }
}

int main() {
    char str[TAM];
    char caractere;
    printf("Digite algo:\n");
    fgets(str, TAM, stdin);

    str[strcspn(str, "\n")] = '\0';

    printf("Digite um caractere específico:\n");
    scanf(" %c", &caractere);

    encontrarCaractere(str, caractere);

    return 0;
}
