#include <stdio.h>
#include <string.h>
int main (){
    int i = 0;
    char col3[30] = {0};
    char col4[30] = {100};
    while(i>=0){
        printf("\nIngrese el nombre de la persona %d o FIN: ", i);
        scanf("%s", col3);
        if (strcmp(col3,"FIN")==0){
            i = -2;
        }
        else{
            if (strcmp(col3,col4)<0){
                strcpy(col4,col3);
            }
        }
        i++;
    }
    printf("\n1er Persona alfabeticamente: %s", col4);
}