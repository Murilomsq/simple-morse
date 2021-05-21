#include "mbed.h"
#include "string.h"

DigitalOut led(LED1);

void MorseBlinkLetterS(DigitalOut& led){
    printf("Blinking S\n");
    for(int i = 0; i < 6; i++){
        led = !led;
        wait_ms(200);
    }
    wait_ms(200);
}

void MorseBlinkLetterO(DigitalOut& led){
    
    printf("Blinking O\n");
    for(int i = 0; i < 6; i++){
        led = !led;
        wait_ms(400);
    }
    wait_ms(200);
}

void BlinkWord(char* word, DigitalOut& led){
    for(int i = 0; i < strlen(word) + 1; i ++){
        switch(word[i]){
            case 'S':
            MorseBlinkLetterS(led);
            break;
            case 'O':
            MorseBlinkLetterO(led);
            break;
        }
    }
}

int main() {
    
    char word[20] = "SOS";
    
    BlinkWord(word, led);
    
}
