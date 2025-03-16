#include "mbed.h"


DigitalOut ledRed(LED1);   // Use LED1 for the first LED (often predefined)
DigitalOut ledD13(LED2);    // Define the D13 pin (usually pin 13 on most boards)

// Main program loop
int main() {
    while (true) {
    
        switch(states){
        case 0:{
        ledRed = 0;  // LOW
        ThisThread::sleep_for(2000ms);  // Delay for 2000 milliseconds (2 seconds)
    
        // Turn on LED Red
        ledRed = 1;  // HIGH
        ThisThread::sleep_for(2000ms);  // Delay for 2000 milliseconds (2 seconds)}
        break;
        
        case 1:{
        // Turn on D13 LED
        ledD13 = 1;  // HIGH
        ThisThread::sleep_for(5000ms);  // Delay for 5000 milliseconds (5 seconds)

        // Turn off D13 LED
        ledD13 = 0;  // LOW
        ThisThread::sleep_for(5000ms);  // Delay for 5000 milliseconds (5 seconds)}
        break;
    }
}
