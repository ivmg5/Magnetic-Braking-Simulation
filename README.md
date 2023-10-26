# Simulación de Movimiento Magnético en MATLAB

## Desarrolladores:
- **Fernanda Reyes Martínez** - A01637163
- **Karen Corona Espinoza** - A01642461
- **Diego Ivan Morales Gallardo** - A01643382
- **Joel Antonio Palomera Corona** - A01644003

## Contexto:
La torre de caída (también conocida como "freefall ride" o "drop tower") es una atracción muy popular en parques de diversiones. En ella, los pasajeros ingresan a una góndola a nivel del suelo y, tras ser asegurados en sus asientos, son elevados a lo largo de una torre vertical. Posteriormente, la góndola se libera en caída libre y justo antes de llegar al suelo, los frenos se activan para detenerla. Este proceso permite que los pasajeros experimenten una sensación de caída libre, seguida de una fuerte desaceleración.

## Reto:
Desarrollar una simulación computacional en MATLAB que modele la desaceleración por frenado magnético (a través de las corrientes de Eddy) de una góndola en una torre de caída. La simulación debe especificar la altura total de la torre y la altura de la parte conductora que se utiliza para el frenado magnético. Asimismo, debe mostrar gráficas de la velocidad y aceleración de la góndola en función de su altura.

## Descripción
El código modela cómo un dipolo magnético se mueve en presencia de un campo magnético inducido. Se tienen en cuenta varias constantes físicas, como la permeabilidad del vacío, la gravedad, el momento magnético del dipolo, entre otros. También se establecen ciertos parámetros configurables, como el radio de la espira, el número de vueltas, la resistencia y la masa.

## Corrientes de Eddy:
Las corrientes de Eddy, también conocidas como corrientes de Foucault o corrientes parásitas, se generan cuando un campo magnético variable incide sobre un conductor eléctrico. Estas corrientes presentan las siguientes ventajas:

- El frenado es sin fricción, reduciendo el mantenimiento requerido.
- No se necesita una fuente de energía para que los frenos funcionen, aumentando la seguridad.
- El frenado es sin jalones ("jerk"), ofreciendo mayor comodidad para los pasajeros.

## Principios Físicos:
- **Ley de Faraday:** El movimiento relativo entre un conductor y un campo magnético induce una circulación de electrones dentro del conductor.
- **Ley de Lenz:** Las corrientes generadas crean electroimanes con campos magnéticos que se oponen al efecto del campo magnético aplicado.

## Ecuación:
La simulación se basa en la segunda Ley de Newton. La ecuación considera la velocidad de la góndola (`v`), la fuerza de gravedad (`Fg`), la fuerza debido a las corrientes de Eddy (`Fz`, que es proporcional a la velocidad), la masa de la góndola (`m`) y el tiempo (`t`). El código incluye la derivación de constantes basadas en las ecuaciones del movimiento magnético y luego resuelve un sistema de ecuaciones diferenciales para obtener la posición, velocidad, aceleración, fuerza y corriente inducida.

## Funciones utilizadas en MATLAB:

- **ODE45:** Esta función precargada en MATLAB permite resolver sistemas de ecuaciones diferenciales.
  
- **ACELERACIÓN (`A`):** Función anónima que modela la aceleración de la góndola en función de su posición y velocidad.

- **DYDT:** Función anónima que representa el sistema de ecuaciones diferenciales que se busca resolver.

## Cómo Ejecutar

1. Asegúrese de tener MATLAB instalado en su computadora.
2. Clone o descargue este repositorio.
3. Abra el archivo principal `Reto.mlx` en MATLAB.
4. Ejecute el script.

---

**Nota:** Para utilizar este proyecto, se recomienda tener un conocimiento básico de MATLAB y de las leyes físicas mencionadas anteriormente. Por favor, consulte la documentación de MATLAB y las referencias proporcionadas para más detalles.
