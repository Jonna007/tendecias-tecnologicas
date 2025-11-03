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
<img width="946" height="577" alt="image" src="https://github.com/user-attachments/assets/3b3b0343-0d11-47b6-9417-542fce3d763b" />

**Paso 2:** Dentro de la carpeta `documentos`, se creó un archivo llamado `notas.txt` y se añadieron tres líneas de texto usando `echo`.
<img width="950" height="423" alt="image" src="https://github.com/user-attachments/assets/04730645-9467-4db8-8550-a02c27a943d4" />

**Paso 3:** Se copió `notas.txt` a la carpeta `scripts` y se modificó su nombre a `backup_notas.txt`.
<img width="943" height="190" alt="image" src="https://github.com/user-attachments/assets/36ab226f-0fd4-4308-8a7c-23edff698e96" />

**Paso 4:** Se movió el archivo `backup_notas.txt` a la carpeta `imagenes`.
<img width="953" height="289" alt="image" src="https://github.com/user-attachments/assets/dce76f9a-478d-4257-af86-c7f53ecf7dba" />

**Paso 5:** Se creó un nuevo archivo `resumen.txt` y se redirecionó el contenido de `notas.txt`.
<img width="957" height="248" alt="image" src="https://github.com/user-attachments/assets/34079314-17e4-4109-990d-8caba329b726" />

**Paso 6:** Se añadió una nueva línea de texto sin sobrescribir lo que ya estaba en `resumen.txt`.
<img width="946" height="266" alt="image" src="https://github.com/user-attachments/assets/26226d70-87ad-477b-8675-bf5084848b7d" />

**Paso 7:** Se eliminó el archivo `backup_notas.txt` y la carpeta `imagenes` (ya vacía).
<img width="942" height="368" alt="image" src="https://github.com/user-attachments/assets/f2651af3-a17b-4a06-a68c-b18739397b24" />

**Paso 8:** Se extrajo el historial de comandos a un archivo con mi nombre.
<img width="952" height="199" alt="image" src="https://github.com/user-attachments/assets/6a3fecac-f096-44d0-b11c-b5d4be209f6c" />

## 9. Resultados esperados

En esta práctica, aprendí a usar los comandos básicos de Linux para organizar archivos. Pude crear carpetas con `mkdir`, moverme entre ellas y crear archivos de texto.

Lo más útil fue entender cómo copiar (`cp`) y mover (`mv`) archivos entre diferentes carpetas. También practiqué cómo eliminar archivos (`rm`) y carpetas vacías (`rmdir`) de forma segura.

Finalmente, entendí la diferencia entre `>` (que sobrescribe todo) y `>>` (que solo añade al final), lo cual me sirvió para crear y modificar el archivo `resumen.txt`. Guardar el historial con `history` para registrar todo lo que hice.

## 10. Bibliografía

- Khattab, A., et al. (2008). WARP: A flexible platform for clean-slate wireless medium access protocol design.
- Richardson, D. (2019). _Introducción a la Terminal de Linux_.
- Sánchez Anguix, V. (2021). Comandos básicos de Linux.
