# Tinkercad
## Crear una ventana con Tkinter

Este es un ejemplo simple de cómo crear una ventana en Python utilizando la librería `tkinter`.

### Código en Python:

```python
import tkinter as tk

ventana = tk.Tk()  # Crear la ventana
ventana.title("Mi ventana")  # Establecer el título de la ventana
ventana.geometry("400x300")  # Establecer el tamaño de la ventana
ventana.mainloop()  # Ejecutar la aplicación

def saludar():
    print("Hola")

boton = tk.Button(ventana,text="saludar", command=saludar)
boton.pack()

label = tk.label(root, text = "Hola", font = ("Arial", 14))
label.pack()
label.config(text="mela")
entrada = tk.Entry(root)
entrada.pack()

texto = entrada.get()
```


### Código en Python pero con IA:
```python


import tkinter as tk

# Colores y estilos
FONDO = "#f0f4f8"
COLOR_BOTON = "#4CAF50"
COLOR_TEXTO = "#333333"
FUENTE = ("Helvetica", 12)

# Crear ventana principal
ventana = tk.Tk()
ventana.title("Mi primera app")
ventana.geometry("400x300")
ventana.configure(bg=FONDO)

# Frame para organizar elementos
marco = tk.Frame(ventana, bg=FONDO)
marco.pack(pady=20)

# Etiqueta de bienvenida
etiqueta = tk.Label(marco, text="¡Hola, mundo!", font=("Helvetica", 16, "bold"), bg=FONDO, fg=COLOR_TEXTO)
etiqueta.pack(pady=10)

# Función al hacer clic en el botón
def saludar():
    nombre = entrada.get()
    if nombre:
        print(f"Hola, {nombre}")
    else:
        print("Hola")

# Entrada de texto
entrada = tk.Entry(marco, font=FUENTE, width=30)
entrada.pack(pady=5)

# Botón
boton = tk.Button(marco, text="Saludar", command=saludar, bg=COLOR_BOTON, fg="white", font=FUENTE, padx=10, pady=5)
boton.pack(pady=10)

# Etiqueta adicional
label = tk.Label(marco, text="Escribe tu nombre arriba y presiona el botón", font=("Arial", 10), bg=FONDO, fg="#666666")
label.pack(pady=10)

# Iniciar el bucle de la ventana
ventana.mainloop()
```

### Código en Python COMBOBOX
```python
import tkinter as tk
from tkinter import ttk

# Función para realizar las operaciones matemáticas
def calcular():
    try:
        num1 = float(entry_num1.get())
        num2 = float(entry_num2.get())
        operacion = combo_operacion.get()
        
        if operacion == "+":
            resultado = num1 + num2
        elif operacion == "-":
            resultado = num1 - num2
        elif operacion == "*":
            resultado = num1 * num2
        elif operacion == "/":
            if num2 != 0:
                resultado = num1 / num2
            else:
                resultado = "Error: División por cero"
        else:
            resultado = "Operación no válida"
        
        label_resultado.config(text=f"Resultado: {resultado}")
    except ValueError:
        label_resultado.config(text="Error: Ingresa números válidos")

# Crear ventana principal
root = tk.Tk()
root.title("Calculadora Básica")
root.geometry("300x200")

# Crear y posicionar los elementos de la interfaz
label_num1 = tk.Label(root, text="Primer número:")
label_num1.pack(pady=5)

entry_num1 = tk.Entry(root)
entry_num1.pack(pady=5)

label_num2 = tk.Label(root, text="Segundo número:")
label_num2.pack(pady=5)

entry_num2 = tk.Entry(root)
entry_num2.pack(pady=5)

label_operacion = tk.Label(root, text="Operación:")
label_operacion.pack(pady=5)

# Combobox para seleccionar la operación
combo_operacion = ttk.Combobox(root, values=["+", "-", "*", "/"])
combo_operacion.current(0)  # Selecciona "+" por defecto
combo_operacion.pack(pady=5)

# Botón para calcular
boton_calcular = tk.Button(root, text="Calcular", command=calcular)
boton_calcular.pack(pady=10)

# Etiqueta para mostrar el resultado
label_resultado = tk.Label(root, text="Resultado: ")
label_resultado.pack(pady=5)

# Ejecutar la aplicación
root.mainloop()
```
