---
{"dg-publish":true,"dg-path":" 1.1. Cerebro Digital/4. Conversión de textos y libros/Tareas avanzadas (código)/Cómo corregir ART y limpiar código con Notepad++ y Python.md","permalink":"/1-1-cerebro-digital/4-conversion-de-textos-y-libros/tareas-avanzadas-codigo/como-corregir-art-y-limpiar-codigo-con-notepad-y-python/"}
---

# Primer paso eventual: extracción de texto y corrección con GlImageReader

En el evento que la ley o código esté disponible en un archivo individual tipo PDF, vamos a extraer todo el texto usando GLImageReader, y luego vamos a seleccionar todo y apretar el botón de strip lines in selected text. 

# Segundo paso: corregir formato de texto utilizando un script de python en notepad++


Primero, hay que instalar Python asegurándose de tener activado el recuadro PATH FILE, luego instalar Notepad e instalar su complemento NPPExec.

Segundo, hay que crear un archivo en Notepad, este contendrá la siguiente línea de código: <mark style='background:var(--mk-color-teal)'>OJO, AGREGAR OTRA TAREA MÁS QUE SEPARE LOS INCISOS, LE DAS EL EJEMPLO DE TEXTO ERRÓNEO Y SOLUCIÓN DESEADA</mark>.

```

import re

# Leer el archivo de texto
with open("C:\\Users\\Diegote\\Desktop\\nuevo1.txt", "r", encoding="utf-8") as file:
    texto = file.read()

# 1. Eliminar espacios en blanco al principio de cada párrafo
texto = re.sub(r'(?m)^\s+', '', texto)

# 2. Eliminar símbolos º
texto = re.sub(r'º', r'', texto)

# 3. Reemplazar encabezados "ARTÍCULO", "Artículo", "Art." por "ART"
texto = re.sub(r'(?m)^(ARTÍCULO|Artículo|Art\.)\s', r'ART ', texto)

# 4. Reemplazar "ART número símbolo punto" por "ART número punto"
texto = re.sub(r'(?m)^(ART)\s(\d+)[^\w\s\.]*(\s*\w*\.?)', r'\1 \2\3', texto)

# 5. Corregir expresiones "Art. número punto" o "Artículo número punto" a "ART número punto"
texto = re.sub(r'(?m)^(Art\.\s*\d+\.|Artículo\s*\d+\.)(\s*)', r'ART \2', texto)

# 6. Eliminar símbolos "º" dentro de texto
texto = re.sub(r'(?m)(\d+)[º]\s', r'\1. ', texto)

# 7. Corregir listas numeradas dentro de párrafos (como 1.º, 2.º, etc.)
texto = re.sub(r'(?m)^\s*(\d+)[\.\-\)]\s*([^\n]+)', lambda match: f"{match.group(1)}. {match.group(2).capitalize()}", texto)

# 8. Agregar "###### " solo al inicio de los párrafos que comienzan con "ART número punto"
texto = re.sub(r'(?m)^(ART\s\d+(\s\w+)?\.)', r'###### \1', texto)

# 9. Asegurar un salto de línea después de "###### ART..."
texto = re.sub(r'(?m)(###### ART\s\d+(\s\w+)?\.)\s', r'\1\n', texto)

# 10. Asegurar que cada párrafo que comienza con "###### ART..." esté separado entre sí
texto = re.sub(r'(?m)(###### ART\s\d+(\s\w+)?\.\s)(?=######)', r'\1\n\n', texto)

# 11. Asegurar que el primer párrafo también esté completamente separado (al principio del archivo)
texto = re.sub(r'(?m)^(###### ART \d+\.\s)', r'\n\1', texto)

# Guardar el resultado en un nuevo archivo
with open("C:\\Users\\Diegote\\Desktop\\resultado_actualizado.txt", "w", encoding="utf-8") as file:
    file.write(texto)

# Imprimir el resultado en consola
print(texto)


```

Como se ve, ejecutará distintas tareas, desde limpiar elementos indeseables hasta separar párrafos y agregar símbolos.
Luego, debemos guardar este script, en nuestra carpeta de scripts, utilizando la extensión ".py". 
También debemos guardar el script en Notepad, para que NPPExec lo reconozca. Para ello, debemos ir a la opción "Execute NPP Script" y pegar en el recuadro la siguiente expresión:

```
python "$(FULL_CURRENT_PATH)"
```

Lo guardamos y le damos un nombre. Cambiar nombre -> Save -> Ok. 

Lo siguiente será ejecutar nuestro script. Para ello, con Python y Notepad abiertos (este último, con el script ya guardado abierto en una pestaña) copiaremos y pegaremos el texto a trabajar, en una pestaña de Notepad. Luego, iremos a Complementos -> NPPExec y ejecutaremos el script apretando Ok.

¡Listo! Tenemos nuestro texto corregido en Notepad. Este se habrá guardado como un archivo .txt en nuestro escritorio.

> [!info]
> Esta solución aplica para cualquier procesamiento de texto que requiramos hacer en Notepad usando NPPExec y un script de Python. Tan sólo dar las indicaciones necesarias a Chat GPT para crear el script, copiar y pegar en un nuevo archivo de Notepad y guardar con la extensión .py. 