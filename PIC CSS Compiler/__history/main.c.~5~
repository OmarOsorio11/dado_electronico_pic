#include <16F1827.h>
#device ADC=16
#FUSES NOWDT                    //No Watch Dog Timer
#FUSES NOBROWNOUT               //No brownout reset
#use delay(crystal=4MHz)
#use standard_io(a)
#use standard_io(b) 
#define RAND_MAX 6 
#include <stdlib.h> // DEBE IR DESPUES DESPUES DE RAND_MAX 
void main()
{
   set_tris_a(0b11111111);
   set_tris_b(0b00000000);
   int numeros[6]={0x6,0x5B,0x4F,0x66,0x6D,0x7D};
   int contar = 0;
   output_b(0x7F);
   srand(1);
   while(TRUE)
   {
      if(input_state(PIN_A0))
      {
         while(input(PIN_A0)){}
         contar = rand();
         output_b(numeros[contar]);
      }
   }
}

