#include <stdio.h>
#include <string.h>
int main (){
    char arr[30] = {0};
    printf("Ingrese una palabra de hasta 20 letras en mayúsculas: ");
    scanf("%s", arr);
    for (int i = 0; i < strlen(arr); i++){
        arr[i] = (arr[i] + 3);
        if (arr[i] + 3 > 90){
            arr[i] = arr[i] - 26;
        }
    }
    printf("\nPalabra encriptada: %s", arr);
}
