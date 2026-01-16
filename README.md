#include <stdio.h>
int main() {
   int m[4][4]={{1,2,3,4},{7,38,9,10},{51,13,20,21},{20,44,2,5}};
   char colonias[4][4][40]={{"26 de Mayo","27 de febrero","Ampliación México","Ampliación Oaxaquenos Iluestres"},{"Arboledas","Benito Juarez","Del Sol","Derechos Humanos"},{"Ejidal","El Obispo","Emiliano Zapata","Felix Gayot"},{"Floresta","Frumencio Pulido Mina","Hermanos Gutierrez","Ignacio Zaragoza"}};
   int fila,col,x=0,y=0;
   int mayor=m[0][0];
   //imprimir matriz
   for(fila=0;fila<4;fila++){
      for(col=0;col<4;col++){
         printf("%d ",m[fila][col]);
      }
      printf("\n");
   }
   for(fila=0;fila<4;fila++){
       for(col=0;col<4;col++){
           if(m[fila][col]>mayor){
               mayor=m[fila][col];
               x=fila;
               y=col;
           }
       }
   }
   printf("%d %s",mayor,colonias[x][y]);
   return 0;
}
