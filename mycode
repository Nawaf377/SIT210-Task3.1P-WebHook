#include <Adafruit_DHT.h>
#define DHTPIN D2    
#define DHTTYPE DHT11


String Data;
DHT dht(DHTPIN, DHTTYPE);


void setup() {

 Serial.begin(9600); 
 
 dht.begin();

}

void loop() {
   
    
    float t2 = dht.getTempCelcius();
    float h2 = dht.getHumidity();
 
    
    Data = String::format("%.1f C, %.1f %", t2, h2);    
    
    Particle.publish("temp", Data, PRIVATE);
    delay(20000);


}
