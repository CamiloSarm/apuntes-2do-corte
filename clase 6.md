# Introducción al Análisis en Frecuencia

El análisis en frecuencia permite observar el comportamiento de un sistema a partir de variaciones en la frecuencia de la señal de entrada. Utilizando señales sinusoidales, se observan cambios en la amplitud y la fase de la señal de salida, lo que permite inferir las características del sistema.

## 1. Definición

🔑 *Definición: El *análisis en frecuencia es un método para estudiar el comportamiento dinámico de un sistema mediante señales periódicas y la variación de su frecuencia.

## 2. Representación con Fasores

Las señales sinusoidales se representan como fasores, los cuales contienen información sobre la magnitud y la fase de la señal, facilitando el análisis matemático.

### 2.1. Procedimiento

Para un sistema con una entrada sinusoidal \( R(t) = A \sin (\omega kT + \theta) \), su representación en fasores es \( R = A \angle \theta \). Esto simplifica el análisis de sistemas en el dominio de la frecuencia.

## 3. Diagramas de Bode

El diagrama de Bode muestra la magnitud y el desfase de un sistema en función de la frecuencia. Se utilizan escalas logarítmicas para representar la ganancia del sistema y la variación de la fase.

### 3.1. Características de los Diagramas de Bode

- *Escala logarítmica*: La magnitud se mide en decibelios (dB) y se calcula como:

$$ A_{dB} = 20 \log_{10} (A) $$

- *Fase*: El desfase entre la señal de entrada y la de salida se expresa en grados (°).

💡 *Ejemplo 1*:
Para una función de transferencia discreta \( H(z) \), el diagrama de Bode se calcula usando \( H(e^{j \omega T}) \):

$$ H(e^{j \omega T}) = \frac{1}{(e^{j \omega T} - 0.1)(e^{j \omega T} - 5)} $$

## 4. Análisis Frecuencial en Tiempo Discreto

Para sistemas discretos, se utiliza la transformación bilineal (Tustin) para aproximar el análisis en tiempo continuo.

### 4.1. Transformación Bilineal

La transformación bilineal se define como:

$$ w = \frac{2}{T} \frac{z - 1}{z + 1} $$

Esto permite transformar una función de transferencia continua al dominio discreto.

## 5. Consideraciones de Implementación

- *Frecuencia de Nyquist*: Los compensadores deben ser diseñados para operar efectivamente hasta esta frecuencia.
- *Causalidad y estabilidad*: El sistema debe ser causal y estable en el lazo cerrado.

## 6. Ejercicios

### 📚 *Ejercicio 1*:
Encontrar el equivalente de la función de transferencia para un sistema con \( G(s) = \frac{8}{s^2 + 6} \) y un tiempo de muestreo \( T = 0.9 \text{s} \).

*Solución*:
Aplicamos la transformación bilineal:

1. Reescribimos \( s = \frac{2}{T} \frac{z - 1}{z + 1} \), donde \( T = 0.9 \).
2. Sustituimos en \( G(s) \):

$$ G(s) = \frac{8}{s^2 + 6} \quad \text{se convierte en} \quad G(z) = \frac{8}{\left( \frac{2}{0.9} \frac{z - 1}{z + 1} \right)^2 + 6} $$

3. Simplificando obtenemos la función de transferencia en \( z \).

## 7. Conclusiones

El análisis en frecuencia es una herramienta fundamental para evaluar y diseñar controladores en sistemas digitales. Los diagramas de Bode permiten visualizar la estabilidad y el comportamiento dinámico del sistema.

## 8. Referencias

- Nise, N. Ingeniería de Sistemas de Control, 6ta edición.
- Material de clase de Control Digital.