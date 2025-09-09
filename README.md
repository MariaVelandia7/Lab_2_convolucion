# Laboratorio 2 - Convolución, Correlación y Transformada de Fourier
**Universidad Militar Nueva Granada**  
**Asignatura:** Laboratorio de Procesamiento Digital de Señales  
**Estudiantes:** [Maria Jose Peña Velandia, Joshara Valentina Palacios, Lina Marcela Pabuena]  
**Fecha:** Septiembre 2025  
**Título de la práctica:** Convolución, correlación y transformada de Fourier

## Objetivos
•	Comprender la convolución como una operación que permite obtener la respuesta de un sistema discreto ante una entrada determinada.
•	Analizar la correlación como medida de similitud entre dos señales.
•	Aplicar la Transformada de Fourier como herramienta de análisis en el dominio de la frecuencia.

# PARTE A

## Resumen

Este repositorio documenta la primera fase de un laboratorio enfocado en el procesamiento de señales discretas. El objetivo principal fue calcular la convolución de dos señales, $x[n]$ y $h[n]$, definidas a partir de datos personales (cédula y código estudiantil, respectivamente). El proceso incluyó una **convolución manual**, seguida de una **verificación computacional** utilizando Python.

### 1. Definición de Señales y Convolución Manual

Las señales de entrada, **$x[n]$** y **$h[n]$**, se definieron usando los dígitos de la cédula y el código estudiantil de cada una de las integrantes. La convolución, $y[n] = x[n] * h[n]$, se calculó paso a paso de forma manual, documentando cada operación.

- **Señal $y[n]$**: María José 
- **Señal $y[n]$**: Valentina 
- **Señal $y[n]$**: Lina

### 2. Representación Gráfica y Secuencial

Se generaron las representaciones gráficas y secuenciales de las señales originales ($x[n]$, $h[n]$) y de la señal resultante ($y[n]$). Este paso se realizó a mano para visualizar el desplazamiento y la superposición de las señales.

- **Gráfica señal $y[n]$**: María José 
- **Gráfica señal $y[n]$**: Valentina 
- **Gráfica señal $y[n]$**: Lina

### 3. Verificación Computacional con Python

Para validar los resultados manuales, se implementó el cálculo de la convolución en Python. Se utilizó la librería **NumPy** para manipular las señales como arreglos y verificar la precisión del cálculo.

<pre>
  # Datos Majo
x = np.array([1,0,1,1,0,8,5,6,7,9])   # cédula
h = np.array([5,6,0,0,8,7,6])         # código estudiantil

# Gráfica de h[n]
t = np.arange(len(h))
plt.figure(figsize=(8, 4))
plt.stem(t, h)
plt.xlabel('n')
plt.ylabel('h [n]')
plt.title('h [n] María José')
plt.grid()
plt.show()

# Gráfica de x[n]
t = np.arange(len(x))
plt.figure(figsize=(8, 4))
plt.stem(t, x)
plt.xlabel('n')
plt.ylabel('x [n]')
plt.title('x [n] María José')
plt.grid()
plt.show()

# Convolución
y = np.convolve(x, h, mode='full')
print("Señal convolución entre h [n] y x [n], María José:")
print(y)

# Gráfica de y[n]
t = np.arange(len(y))
plt.figure(figsize=(10, 4))
plt.stem(t, y)
plt.xlabel('n')
plt.ylabel('y [n]')
plt.title('Convolución y [n] = x [n] * h [n]')
plt.grid()
plt.show()
</pre> 

## Gráfica Código Estudiantil María José
<img width="678" height="394" alt="Grafica Codigo estudiantil majo" src="https://github.com/user-attachments/assets/1aaf8e9b-b287-4250-b6c0-6ca1ea3164a4" />
## Gráfica Cédula María José
<img width="678" height="394" alt="Grafica cedula majo" src="https://github.com/user-attachments/assets/6bef032c-da47-4662-96d0-f239514e7249" />
## Gráfica Convolución María José
<img width="850" height="394" alt="convolución Majo" src="https://github.com/user-attachments/assets/7a8b5d55-60a3-4030-b6a4-b4961f4605ad" />

<pre>

</pre> 

<pre>
# Datos de Lina
x = np.array([1,0,1,1,0,8,2,1,5,0])   # cédula
h = np.array([5,6,0,0,8,2,2])         # código estudiantil

# Gráfica de h[n]
t = np.arange(len(h))
plt.figure(figsize=(8, 4))
plt.stem(t, h)
plt.xlabel('n')
plt.ylabel('h[n]')
plt.title('h[n] Lina')
plt.grid()
plt.show()

# Gráfica de x[n]
t = np.arange(len(x))
plt.figure(figsize=(8, 4))
plt.stem(t, x)
plt.xlabel('n')
plt.ylabel('x[n]')
plt.title('x[n] Lina')
plt.grid()
plt.show()

# Convolución
y = np.convolve(x, h, mode='full')
print("Señal convolución entre h[n] y x[n], Lina:")
print(y)

# Gráfica de y[n]
t = np.arange(len(y))
plt.figure(figsize=(10, 4))
plt.stem(t, y)
plt.xlabel('n')
plt.ylabel('y[n]')
plt.title('Convolución y[n] = x[n] * h[n]')
plt.grid()
plt.show()
</pre> 

