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
