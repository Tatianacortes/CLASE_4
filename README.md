# CONTROL DIGITAL - CLASE_4
# Manejo de Simscape Multibody

## Definición  
Simscape Multibody es un entorno de simulación para modelar sistemas en 3D a partir de cuerpos rígidos interconectados mediante articulaciones, como de rotación y prismáticas. Estos mecanismos permiten medir variables de movimiento como fuerza, velocidad, torque y aceleración. Además, se pueden aplicar fuerzas en diferentes puntos del mecanismo y visualizar la animación 3D del movimiento esperado del sistema. Se puede integrar con dominios físicos como hidráulicos, eléctricos y neumáticos. El modelado se realiza mediante bloques y permite importar modelos desde software de modelado CAD.  

## Configuración de Solver  

### Método de Integración  
La efectividad y exactitud del método dependen de la frecuencia de la solución:  

- **Frecuencias altas:** `ode15s`, `ode23s`  
- **Sistemas más típicos:** `ode42`, `ode23`, `ode23t`  

### Paso del Tiempo  
Determina cada cuánto se calculará la integral. Un menor tiempo de paso no siempre es mejor, ya que puede hacer la simulación más lenta y requerir mayor capacidad de procesamiento.  

### Tipo de Paso  
- **Paso variable**  
- **Paso fijo:** Si el tiempo de paso es demasiado pequeño, la simulación puede volverse lenta y exigir mayor capacidad de procesamiento.  

## Primer Proyecto  

Para iniciar un nuevo proyecto, utilizar el comando:  
```matlab
>> smnew
```
![Figura de prueba](IMAGES/PIN.png)

**1 Bloque (solver configuration)**  

-Tolerancia  
-Estado transitorio o estacionario  
-Solver  
-Tiempo de muestreo  
-etc  

**2 Bloque (world frame)**  

parámetros preestablecidos  

**3 Bloque - leyes físicas (mechanism configuration)**  
-Aceleración  
-gravedad - eje z por facilidad se configura en el eje y  
##
### Paso 1

Configurar la gravedad en el eje z  
![Figura de prueba](IMAGES/P2.png)
##
### Paso 2
Configurar el tamaño del solido    
![Figura de prueba](IMAGES/P3.png)
##
### Paso 3
Configurar el color y opacidad del solido   
![Figura de prueba](IMAGES/P4.png)
##
### Paso 4
Configurar el frame adicional, el cual posteriormente será usado en la rotación del solido  
![Figura de prueba](IMAGES/P5.png)
![Figura de prueba](IMAGES/P6.png)
##
### Paso 5
Simular el modelado, el cual se observa en la imagen a continuación
![Figura de prueba](IMAGES/P7.png)
##
### Paso 6
Cambiar la vista de ejes  
![Figura de prueba](IMAGES/P77.png)
