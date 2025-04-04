Explicación del código:

Configuración de Hardware:

Los pines del motor están configurados para controlar dirección y velocidad

Se usa PWM para control de velocidad mediante los canales LEDC del ESP32

Los sensores IR se leen como entradas digitales

Los sensores de proximidad se leen como entradas analógicas

Lógica Principal:

Primero verifica obstáculos con los sensores de proximidad

Si detecta obstáculo, se detiene por 500ms

Si no hay obstáculos, lee los sensores de línea

Toma decisiones de movimiento basado en los sensores IR

Funciones de Movimiento:

moverAdelante(): Ambos motores hacia adelante

girarDerecha(): Motor izquierdo adelante, derecho atrás

girarIzquierda(): Motor derecho adelante, izquierdo atrás

detenerMotores(): Detiene ambos motores

Ajustes Necesarios:

Pines:

Verificar que la asignación de pines coincide con tu conexión física

Sensores IR:

Invertir la lógica (HIGH/LOW) según el tipo de sensor y superficie

Ajustar la posición física de los sensores para mejor seguimiento

Sensores de Proximidad:

Calibrar el UMBRAL_OBSTACULO según tus sensores y distancia deseada

Si usas sensores digitales, cambiar analogRead por digitalRead

Velocidades:

Ajustar VELOCIDAD_NORMAL y VELOCIDAD_GIRO (0-255)

Modificar la diferencia de velocidad para ajustar giros
