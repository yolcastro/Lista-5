#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define TAM 100

void copiarString(char *str1, char *str2) {
    while (*str1 != '\0') {
        *str2 = *str1;
        str1++;
        str2++;
    }
}

int main() {
    char str1[TAM];
    char str2[TAM];
    char *pstrs;

    printf("Digite a primeira string: ");
    fgets(str1, TAM, stdin);

    printf("Digite a segunda string: ");
    fgets(str2, TAM, stdin);
    
    str1[strcspn(str1, "\n")] = '\0';
    str2[strcspn(str2, "\n")] = '\0';

    pstrs = (char*)malloc(strlen(str1) + strlen(str2) + 1);
    
    if (!pstrs) {
        puts("Memória insuficiente");
        exit(1);
    }
    
    copiarString(str1, pstrs);
    strcat(pstrs, str2);

    printf("[%p] %s", pstrs, pstrs);
    
    free(pstrs);
    
    return 0;
}
