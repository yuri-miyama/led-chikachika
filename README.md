# led-chikachika
RasberryPiにてLEDがチカチカするプログラムです
#include <wiringPi.h>

#define LED_PORT 4		

int main (void) {
	int a;

	
	if(wiringPiSetupGpio() == -1) return 1;
	pinMode(LED_PORT, OUTPUT);

	for (a=0; a<10; a++) {
		
		digitalWrite(LED_PORT, 1);
		delay(500);

		
		digitalWrite(LED_PORT, 0);
		delay(500);
	}

	return 0;
}
