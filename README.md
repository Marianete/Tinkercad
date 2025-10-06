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
