# Practica 1_ ESP32 con DTH22

**Sensor de Temperatura y Humedad**

En esta práctica podemos programar una ESP32 con el sensor DHT22.

## Contenido 
- Introducción 
- Objetivo
- Material Requerido
- Procedimiento a realizar 


## 1. Introducción

La ```Esp32``` la utilizamos en un entorno de adquision de datos, lo cual en esta practica ocuparemos un sensor (```DTH22```).
### 1.1 Descripción
 El ```DHT22``` utiliza un solo cable digital para la comunicación de datos, lo que hace que su conexión sea sencilla y fácil de implementar en proyectos de electrónica. Este sensor proporciona mediciones de temperatura y humedad de alta precisión, con una precisión de +/-0.5 °C para la temperatura y +/-2-5% para la humedad para adquirir temperatura y humedad del entorno. 
 
 ### 1.2 Especificación 
 Es importante considerar que esta practica se estara realiando en un simulador llamado [WOKWI](https://https://wokwi.com/).

## 2. Objetivo 

Poder diseñar un diagrama con sensor DHT22 de temperatura y humedad que se utilice para medir la temperatura y la humedad relativa del ambiente en el que se encuentra, mediante la utilización de una ESP32.


## 3. Material Requerido

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

#### Nota: Es importante considerar que el "delay(1000); ", se puede programar al tiempo que usted desee estar monitoreando el sensor. 


## Paso 2 

2. Instalar la libreria de **DHT sensor library for ESPx** como se muestra en la siguente imagen.

![](https://github.com/DulceMRZ/PRACTICA_1_DHT22/blob/main/Practica_1_DTH11%20-%20Wokwi%20ESP32,%20STM32,%20Arduino%20Simulator%20-%20Google%20Chrome%2009_06_2023%2008_50_46%20p.%20m..png?raw=true)

## Paso 3

3. Hacer la conexion de **DHT22** con la **ESP32** como se muestra en la siguentes imagenes:

3.1 Es importante considerar que para **ESP32** se maneja un ```Voltaje de trabajo 3.3 VDC```. 

a) Observar conexión de pin del Sensor al **pin 1** de **ESP32**. 

![](https://github.com/DulceMRZ/PRACTICA_1_DHT22/blob/main/Practica_1_DTH22%20diagrama%20(1).PNG?raw=true)

b) 


![](https://github.com/DulceMRZ/PRACTICA_1_DHT22/blob/main/Practica_1_DTH22%20diagrama%20(2)..PNG?raw=true)

c)


![](https://github.com/DulceMRZ/PRACTICA_1_DHT22/blob/main/Practica_1_DTH22%20diagrama..png?raw=true)

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

Desarrollado por Ing. Dulce M Rodriguez Zarate 

- [GitHub](https://github.com/DiegoJm10)