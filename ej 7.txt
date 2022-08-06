#include <stdio.h>
typedef struct persona{
    int edad;
    char nombre[30];
} persona;
int main (){
    
    persona personas[6];
    int col = 0;
    int col2 = 0;
    for (int i = 1; i < 6; i++){
        printf("\nIngrese el nombre de la persona %d: ", i);
        scanf("%s", personas[i].nombre);
        printf("Ingrese la edad de la persona %d: ", i);
        scanf("%d", &personas[i].edad);
    }
    col = personas[1].edad;
    col2 = 1;
    for (int i = 1; i < 6; i++){
        if (personas[i].edad < col){
            col = personas[i].edad;
            col2 = i;
        }
    }
    printf("Persona mas joven: %s", personas[(col2)].nombre);
}