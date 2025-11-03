# Práctica: Comandos de Linux

## 1. Título
**Práctica No 1**: Comandos Linux en la Terminal

## 2. Tiempo de duración
La práctica se realizó aproximadamente en unas 2 horas.

## 3. Fundamentos

Esta práctica se centra en los comandos básicos de Linux orientados a la gestión de archivos y directorios. Dominar estos comandos permite al usuario realizar operaciones fundamentales como crear, mover, copiar, eliminar archivos, y estructurar carpetas de manera eficiente desde la terminal.

Entre los comandos utilizados destacan:

* `mkdir`: crea directorios.
* `echo`: escribe texto y permite redirecciones.
* `cat`: muestra el contenido de archivos.
* `cp`: copia archivos.
* `mv`: mueve o renombra archivos.
* `rm`, `rmdir`: eliminan archivos y carpetas.
* `history`: muestra los comandos ejecutados.

Además, se emplea la redirección de contenido con:
* `>` (sobrescribir) 
* `>>` (añadir), permitiendo generar nuevos archivos a partir de otros.

## 4. Conocimientos previos

Para realizar esta práctica es necesario conocer sobre Linux, un sistema operativo open source. Un comando Linux es un programa que se ejecuta en la CLI (Interfaz de Línea de Comandos). Usamos la terminal Warp, que es un terminal moderno, para ejecutar comandos básicos como `cd`, `ls`, `cp`, y `mv`.

## 5. Objetivos a alcanzar
   
- Crear una estructura de carpetas en un directorio.
- Manipular los archivos: crear, copiar, mover, eliminar.
- Aplicar redirección y concatenación de archivos.
- Eliminar archivos y directorios de manera controlada.
- Volcar el historial de comandos a un archivo y presentarlo como parte de la entrega.
  
## 6. Equipo necesario
  
- **Computador:** DESKTOP-OM5U658
- **Sistema Operativo:** Windows 11 Pro (Versión 25H2)
- **Procesador:** Intel(R) Core(TM) 7 240H (2.50 GHz)
- **Memoria RAM:** 32,0 GB
- Conexión a Internet para el material de apoyo
- Terminal en Warp

## 7. Material de apoyo
   
- Guía oficial de comandos Linux
- Documentación de Warp
- Guía de asignatura proporcionada por el docente.

## 8. Procedimiento

**Paso 1:** Se creó una carpeta denominada `proyecto_comandos` y dentro de ella, tres subcarpetas denominadas `documentos`, `imagenes` y `scripts` con `mkdir`.


**Paso 2:** Dentro de la carpeta `documentos`, se creó un archivo llamado `notas.txt` y se añadieron tres líneas de texto usando `echo`.


**Paso 3:** Se copió `notas.txt` a la carpeta `scripts` y se modificó su nombre a `backup_notas.txt`.

*Figura 3. Comando "cp".*
> (Aquí pegas tu captura del comando 'cp ...')

**Paso 4:** Se movió el archivo `backup_notas.txt` a la carpeta `imagenes`.

*Figura 4. Comando "mv".*
> (Aquí pegas tu captura del comando 'mv ...')

**Paso 5:** Se creó un nuevo archivo `resumen.txt` y se redirecionó el contenido de `notas.txt`.

*Figura 5. Comando "cat" y redirección (>).*
> (Aquí pegas tu captura de 'cat ... > ...')

**Paso 6:** Se añadió una nueva línea de texto sin sobrescribir lo que ya estaba en `resumen.txt`.

*Figura 6. Comando "echo" y concatenación (>>).*
> (Aquí pegas tu captura de 'echo ... >> ...')

**Paso 7:** Se eliminó el archivo `backup_notas.txt` y la carpeta `imagenes` (ya vacía).

*Figura 7. Comandos "rm" y "rmdir".*
> (Aquí pegas tu captura de 'rm' y 'rmdir')

**Paso 8:** Se extrajo el historial de comandos a un archivo con mi nombre.

*Figura 8. Comando "history".*
> (Aquí pegas tu captura de 'history > ...')

## 9. Resultados esperados

En esta práctica, aprendí a usar los comandos básicos de Linux para organizar archivos. Pude crear carpetas con `mkdir`, moverme entre ellas y crear archivos de texto.

Lo más útil fue entender cómo copiar (`cp`) y mover (`mv`) archivos entre diferentes carpetas. También practiqué cómo eliminar archivos (`rm`) y carpetas vacías (`rmdir`) de forma segura.

Finalmente, entendí la diferencia entre `>` (que sobrescribe todo) y `>>` (que solo añade al final), lo cual me sirvió para crear y modificar el archivo `resumen.txt`. Guardar el historial con `history` fue un buen truco para registrar todo lo que hice.

## 10. Bibliografía

- Khattab, A., et al. (2008). WARP: A flexible platform for clean-slate wireless medium access protocol design.
- Richardson, D. (2019). _Introducción a la Terminal de Linux_.
- Sánchez Anguix, V. (2021). Comandos básicos de Linux.