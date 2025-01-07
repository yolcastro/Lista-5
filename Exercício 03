#include <stdio.h>

int main() {
    int n, menor;
    int *pmenor = NULL;

    puts("ATENÇÃO: O valor 0 encerra o programa.");
    
    printf("Insira um número:\n");
    scanf("%d", &n);
    
    if (n == 0) {
        printf("Inicialize com um valor diferente de zero.");
        return 0;
    }
    else {
        menor = n;
    }
    
    do {
        printf("Insira um número:\n");
        scanf("%d", &n);
        
        if (n == 0) {
        break;
        }
        else if (n < menor) {
            menor = n;
        }
        
    } while (1);
 
    pmenor = &menor;
    
    printf("[%p] %d\n", pmenor, *pmenor);

    return 0;
}
