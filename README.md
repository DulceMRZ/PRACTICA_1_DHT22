# Practica 1_ ESP32 con DTH22

**Sensor de Temperatura y Humedad**

En esta práctica podemos programar una ESP32 con el sensor DHT22.

## Contenido 
- 1. Introducción 
    -     1.1 Descripción 
    -     1.1 Especificación 
- 2. Material Requerido
- 3. Procedimiento a realizar 
  



## 1. Introducción

La ```Esp32``` la utilizamos en un entorno de adquision de datos, lo cual en esta practica ocuparemos un sensor (```DTH22```).
### 1.1 Descripción
 El ```DHT22``` utiliza un solo cable digital para la comunicación de datos, lo que hace que su conexión sea sencilla y fácil de implementar en proyectos de electrónica. Este sensor proporciona mediciones de temperatura y humedad de alta precisión, con una precisión de +/-0.5 °C para la temperatura y +/-2-5% para la humedad para adquirir temperatura y humedad del entorno. 
 
 ### 1.2 Especificación 
 Es importante considerar que esta practica se estara realiando en un simulador llamado [WOKWI](https://https://wokwi.com/).


## 2. Material Requerido

Tomar en cuenta el material necesario para realizar esta práctica:

- [WOKWI](https://https://wokwi.com/)
- Tarjeta ESP 32
- Sensor DHT22



## 3. Procedimiento a realizar 

 - Requisitos previos

Para poder usar este repositorio necesitas entrar a la plataforma [WOKWI](https://https://wokwi.com/).


## Paso 1 

1. Abrir la terminal de programación y colocar la siguente programación:

```
#include "DHTesp.h"

const int DHT_PIN = 15;
DHTesp dhtSensor;


void setup() {

  Serial.begin(115200);
  dhtSensor.setup(DHT_PIN, DHTesp::DHT22);
}

void loop() {

  TempAndHumidity  data = dhtSensor.getTempAndHumidity();
  Serial.println("Temp: " + String(data.temperature, 1) + "°C");
  Serial.println("Humidity: " + String(data.humidity, 1) + "%");
  Serial.println("---");
  delay(1000);
}

```
2. Instalar la libreria de **DHT sensor library for ESPx** como se muestra en la siguente imagen.

![](https://github.com/DulceMRZ/EJEMPLO_DIPLOMADO/blob/main/tokikiki.PNG?raw=true)

3. Hacer la conexion de **DHT11** con la **ESP32** como se muestra en la siguente imagen.

![](https://github.com/DiegoJm10/PracticaDHT/blob/main/New%20ESP32%20Project%20-%20Wokwi%20Simulator%20-%20Google%20Chrome%2008_06_2023%2011_10_20%20p.%20m.%20(2).png?raw=true)

### Instrucciónes de operación

1. Iniciar simulador.
2. Visualizar los datos en el monitor serial.
3. Colocar la temperatura y humedad dando *doble click* al sensor **DHT11** 

## Resultados

Cuando haya funcionado, verás los valores dentro del monitor serial como se muestra en la siguente imagen.

![](https://github.com/DiegoJm10/PracticaDHT/blob/main/New%20ESP32%20Project%20-%20Wokwi%20Simulator%20-%20Google%20Chrome%2008_06_2023%2011_10_20%20p.%20m..png?raw=true)




## Evidencias

[Video de Youtube](https://https://wokwi.com/)


# Créditos

Desarrollado por Ing. Diego Jasso Miranda

- [GitHub](https://github.com/DiegoJm10)