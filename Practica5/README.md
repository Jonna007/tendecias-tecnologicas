# 📄 Práctica No 5 - Despliegue de WordPress, MySQL y phpMyAdmin con Docker Compose

## 1. Título

**Práctica No 5**: Orquestación de contenedores (WordPress, MySQL, phpMyAdmin) utilizando Docker Compose y formato YAML.

## 2. Tiempo de duración

Aproximadamente 2 horas.

## 3. Fundamentos

En esta práctica se deja de lado la ejecución imperativa de contenedores individuales para adoptar un enfoque declarativo mediante **Docker Compose**. Esta herramienta permite definir y ejecutar aplicaciones multi-contenedor (Docker, 2024).

Se utiliza el formato **YAML** ("YAML Ain't Markup Language"), un lenguaje de serialización de datos diseñado para ser legible por humanos, basado en la indentación estricta para definir jerarquías (YAML.org, 2024).

Los conceptos clave aplicados son:
- **Services**: Definición de los contenedores (WordPress, MySQL, phpMyAdmin) y sus configuraciones.
- **Volumes**: Persistencia de datos para asegurar que la información de la base de datos y los archivos de WordPress no se pierdan al reiniciar los contenedores.
- **Networks**: Creación de una red tipo `bridge` para la comunicación interna y resolución de nombres de host entre servicios.
- **Depends_on**: Control del orden de inicio de los servicios.

## 4. Conocimientos previos

- Dominio de comandos básicos de Docker (`run`, `ps`, `exec`).
- Entendimiento de la estructura Cliente-Servidor.
- Conceptos básicos de bases de datos relacionales (MySQL).
- Conocimiento sobre direccionamiento de puertos e IPs.

## 5. Objetivos a alcanzar

- Crear un archivo `docker-compose.yml` con la estructura correcta en formato YAML.
- Orquestar 3 servicios interconectados: Base de datos (MySQL), Aplicación (WordPress) y Gestión (phpMyAdmin).
- Definir volúmenes para la persistencia de datos y redes para la comunicación.
- Desplegar la pila completa con un solo comando y verificar su funcionamiento.

## 6. Equipo necesario

- **Computador:** DESKTOP-OM5U658
- **Sistema Operativo:** Windows 11 Pro (Versión 25H2)
- **Procesador:** Intel(R) Core(TM) 7 240H (2.50 GHz)
- **Memoria RAM:** 32,0 GB
- **Software:** Docker Desktop, Visual Studio Code, Terminal (Warp).

## 7. Material de apoyo

- Documentación oficial de Docker Compose.
- Guía de sintaxis YAML.
- Repositorio oficial de imágenes de Docker Hub (mysql, wordpress, phpmyadmin).
- Material audiovisual proporcionado en el entorno virtual de aprendizaje (EVA).

## 8. Procedimiento

**Paso 1:** Creación del archivo de configuración `docker-compose.yml`.
Se estructuró el archivo definiendo la versión, los servicios (`db`, `wordpress`, `phpmyadmin`), los volúmenes persistentes y la red `red_wp`.

*Figura 1. Código fuente en Visual Studio Code.*
<img width="859" height="1132" alt="1" src="https://github.com/user-attachments/assets/01d23ce7-4514-4c88-9f1f-9ac60710f257" />


**Paso 2:** Despliegue de los servicios.
Se utilizó el comando `docker-compose up -d` para descargar las imágenes y levantar los contenedores en segundo plano. Posteriormente, se verificó el estado con `docker-compose ps`.

*Figura 2. Ejecución de comandos en terminal Warp.*
<img width="949" height="1069" alt="2" src="https://github.com/user-attachments/assets/5b550f0f-0c2b-44ef-b0d5-0ee6e77b7df5" />


**Paso 3:** Configuración inicial de WordPress.
Se accedió a `localhost:8081` para realizar la instalación del CMS, definiendo el título del sitio y las credenciales de administrador.

*Figura 3. Instalación de WordPress.*
<img width="736" height="848" alt="3" src="https://github.com/user-attachments/assets/df1d13c8-29d6-462f-aa47-fda502a7cc02" />


**Paso 4:** Verificación del funcionamiento de WordPress.
Acceso exitoso al "Escritorio" (Dashboard) de WordPress, confirmando la conexión correcta con la base de datos.

*Figura 4. Escritorio de WordPress.*
<img width="958" height="1144" alt="4" src="https://github.com/user-attachments/assets/93819b69-b372-488b-abd1-c62eb3ccaa8c" />


**Paso 5:** Verificación de la Base de Datos con phpMyAdmin.
Acceso a `localhost:8082` para inspeccionar visualmente la base de datos `wordpress` y confirmar la creación automática de las tablas.

*Figura 5. Tablas de la base de datos en phpMyAdmin.*
<img width="960" height="1199" alt="5" src="https://github.com/user-attachments/assets/36fff80b-7419-4374-9870-c8d443ff2f1d" />


## 9. Resultados esperados

La práctica concluyó exitosamente logrando automatizar el despliegue de un entorno LAMP (Linux, Apache, MySQL, PHP) moderno utilizando contenedores.
Se verificó que:
1.  Los tres contenedores se comunican entre sí mediante la red `red_wp` utilizando los nombres de servicio como hostnames.
2.  La información de la base de datos persiste gracias al volumen `db_data`.
3.  El archivo `docker-compose.yml` permite replicar todo el entorno con un solo comando, eliminando la complejidad de la configuración manual.

## 10. Bibliografía

- Docker Inc. (2024). *Overview of Docker Compose*. https://docs.docker.com/compose/
- The YAML Project. (2024). *YAML Ain’t Markup Language (YAML™) Version 1.2*. https://yaml.org/
- WordPress Foundation. (2024). *WordPress: Blog Tool, Publishing Platform, and CMS*. https://wordpress.org/
