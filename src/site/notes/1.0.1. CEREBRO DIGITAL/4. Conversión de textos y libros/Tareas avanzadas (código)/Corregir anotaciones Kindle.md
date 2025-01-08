---
{"dg-publish":true,"dg-path":" 1.2. Cerebro Digital/4. Conversión de textos y libros/Tareas avanzadas (código)/Corregir anotaciones Kindle.md","permalink":"/1-2-cerebro-digital/4-conversion-de-textos-y-libros/tareas-avanzadas-codigo/corregir-anotaciones-kindle/"}
---

# Introducción

Me gusta leer en mi Kindle, y hacer anotaciones y comentarios al vuelo. Esta lectura tiene el carácter de ser activa y obedecer a un propósito: capturar la información en mi cerebro digital y luego procesarla y memorizarla.
Esto sería tremendamente fácil si leemos libros comprados directamente en la tienda de Amazon, pues podremos exportar las anotaciones con facilidad a nuestro cerebro digital.
Sin embargo, si eres de los que leen libros PDF reconvertidos al Kindle, por distintos motivos, como es mi caso, deberás dar una pequeña vuelta.

# Detección de anotaciones en My Clippings

Al conectar tu Kindle a tu PC, podrás encontrar un archivo llamado MyClippings.txt. En este archivo, estarán tus anotaciones hechas en los distintos libros que has encontrado. 
Entonces, deberás detectar las anotaciones del libro que deseas transferir a Obsidian, y copiarlas completamente. 

# Procesamiento con Notepad++

Una vez hayas copiado tus anotaciones, puedes pegarlas tranquilamente en Notepad. Ha llegado el momento de procesar el texto. 
Puede haber expresiones que no te interese mantener, o espacios que te interese eliminar. En mi caso, resolví hacerlo mediante el siguiente Python script. 

```
import os
import re
import chardet

def procesar_texto():
    # Obtener la ruta del escritorio
    escritorio = os.path.join(os.path.expanduser("~"), "Desktop")

    # Definir las rutas de los archivos
    ruta_entrada = os.path.join(escritorio, "nuevo1.txt")
    ruta_salida = os.path.join(escritorio, "anotaciones procesadas.txt")

    # Verificar si el archivo de entrada existe
    if not os.path.exists(ruta_entrada):
        print(f"Error: El archivo '{ruta_entrada}' no existe en el escritorio.")
        return

    # Detectar la codificación del archivo de entrada
    with open(ruta_entrada, 'rb') as archivo:
        raw_data = archivo.read()
        result = chardet.detect(raw_data)
        encoding_detected = result['encoding']
        print(f"Codificación detectada: {encoding_detected}")

    # Leer el archivo original con la codificación detectada
    with open(ruta_entrada, 'r', encoding=encoding_detected) as archivo:
        lineas = archivo.readlines()

    # Tareas 1 a 4: Filtrar líneas no deseadas con expresiones regulares
    patrones_a_eliminar = [
        r"^\s*Aprende a tomar notas con tu Cerebro Digital: Leer es perder el tiempo si luego no puedes recuperar esa información \(Spanish Edition\) \(Emowe, Marcos\)",  # Línea completa con espacios ignorados
        r"^\s*- La subrayado en la posición",                                                                                     # Líneas que comienzan con esta frase
        r"^\s*- El marcador en la posición",                                                                                     # Líneas que comienzan con esta frase
        r".*===.*"                                                                                                               # Líneas que contienen ===
    ]
    lineas_filtradas = [
        linea for linea in lineas
        if not any(re.match(patron, linea) for patron in patrones_a_eliminar)
    ]

    # Tarea 5: Reducir saltos de línea a solo uno entre párrafos
    texto_unido = ''.join(lineas_filtradas)
    texto_limpiado = re.sub(r'\n\s*\n+', '\n\n', texto_unido.strip())

    # Guardar el texto procesado
    with open(ruta_salida, 'w', encoding='utf-8') as archivo_salida:
        archivo_salida.write(texto_limpiado)

    print(f"Procesamiento completado. Archivo guardado en: {ruta_salida}")

# Ejecutar el procesamiento
procesar_texto()

```

**Importante**: cada vez que se utilice el script, debe cambiarse la expresión recurrente que tiene origen en el nombre del libro. En el caso del script de ejemplo: Aprende a tomar notas con tu Cerebro Digital: Leer es perder el tiempo si luego no puedes recuperar esa información \(Spanish Edition\) \(Emowe, Marcos\).  **Intentar mantener los símbolos**.