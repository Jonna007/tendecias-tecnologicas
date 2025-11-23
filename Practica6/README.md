# Práctica No 6 - Creación de Imágenes Personalizadas (Dockerfile) para React

## 1. Título
**Práctica No 6**: Contenerización de una aplicación Frontend (React) mediante Dockerfile y Multi-stage Builds.

## 2. Tiempo de duración
Aproximadamente 2 horas.

## 3. Fundamentos
En esta práctica se profundiza en el concepto de **Infraestructura como Código**, dejando de lado la ejecución manual de contenedores para automatizar la creación de imágenes mediante un **Dockerfile**.
El Dockerfile actúa como una "receta" que contiene las instrucciones precisas para construir una imagen de Docker, asegurando que el entorno sea reproducible y estandarizado.
Se aplicaron conceptos avanzados como:
**Multi-stage builds**: Una técnica que permite usar una imagen intermedia (Node.js) para compilar la aplicación y una imagen final ligera (Nginx) para servirla, optimizando drásticamente el peso del contenedor final.
**.dockerignore**: Archivo fundamental para excluir carpetas locales pesadas como `node_modules` del contexto de construcción, mejorando la velocidad del `build`.

## 4. Conocimientos previos
* Manejo de la terminal y comandos básicos de Docker (`run`, `ps`).
* Nociones básicas de **Node.js** y **npm** para la gestión de dependencias.
* Entendimiento de la arquitectura Cliente (Frontend) - Servidor (Backend).
* Conceptos de servidores web (Nginx).

## 5. Objetivos a alcanzar
* Clonar y ejecutar localmente un entorno de desarrollo (Frontend + Backend).
* Crear un archivo `.dockerignore` para optimizar el contexto de construcción.
* Redactar un **Dockerfile** utilizando la estrategia de construcción en etapas (Multi-stage).
* Construir una imagen personalizada usando `docker build`.
* Desplegar el contenedor final con `docker run` y verificar su conectividad con el backend.

## 6. Equipo necesario
* **Computador:** DESKTOP-OM5U658
* **Sistema Operativo:** Windows 11 Pro (Versión 25H2)
* **Procesador:** Intel(R) Core(TM) 7 240H (2.50 GHz)
* **Memoria RAM:** 32,0 GB
* **Software:** Docker Desktop, Visual Studio Code, Terminal (Warp).

## 7. Material de apoyo
* Documentación oficial de Docker (Dockerfile reference).
* Repositorios de código fuente proporcionados (MockAPI y Suda-Frontend).
* Guía de despliegue de React en Nginx.
* [cite_start]Material audiovisual de la plataforma EVA[cite: 2340].

## 8. Procedimiento

**Paso 1: Preparación del entorno y Backend.**
Se clonaron los repositorios necesarios. Primero se inició el servicio de Backend (MockAPI) para asegurar la disponibilidad de datos.
*Figura 1. Backend ejecutándose en el puerto 3100.*
![alt text](<Captura de pantalla 2025-11-22 215110.png>)
<img width="939" height="825" alt="Captura de pantalla 2025-11-23 034942" src="https://github.com/user-attachments/assets/d8836230-5c04-4c85-adb9-befed79df60a" />

**Paso 2: Verificación local del Frontend.**
Antes de crear el contenedor, se verificó que la aplicación React funcionara correctamente en el entorno local mediante `npm run dev`.
*Figura 2. Aplicación React funcionando localmente.*
<img width="917" height="735" alt="Captura de pantalla 2025-11-23 035515" src="https://github.com/user-attachments/assets/736152fb-4dbd-4fb7-a727-5d334cbbd7ac" />
<img width="961" height="1063" alt="Captura de pantalla 2025-11-23 035653" src="https://github.com/user-attachments/assets/d800aa12-dde9-420a-aded-ae910ced2087" />


**Paso 3: Creación de archivos de configuración.**
Se creó el archivo `.dockerignore` para excluir `node_modules` y el `Dockerfile` configurado en dos etapas: compilación con Node.js y servicio con Nginx Alpine.
*Figura 3. Estructura del Dockerfile en VS Code.*
<img width="814" height="934" alt="Captura de pantalla 2025-11-23 105441" src="https://github.com/user-attachments/assets/6c75ef76-23e6-45bb-8880-58643510c4b4" />


**Paso 4: Construcción de la imagen (Build).**
Se ejecutó el comando `docker build -t mi-frontend-react .` para generar la imagen binaria a partir del Dockerfile.
*Figura 4. Proceso de construcción exitoso en la terminal.*
<img width="928" height="1000" alt="Captura de pantalla 2025-11-23 100732" src="https://github.com/user-attachments/assets/299afd1c-28f8-4745-a912-0931cb0eb8c3" />


**Paso 5: Despliegue y Validación.**
Se inició el contenedor con `docker run -d -p 8080:80...` y se accedió al navegador para confirmar que Nginx está sirviendo la aplicación correctamente conectada a la API.
*Figura 5. Aplicación ejecutándose desde el contenedor Docker (localhost:8080).*
<img width="1919" height="1128" alt="Captura de pantalla 2025-11-23 101224" src="https://github.com/user-attachments/assets/e8a4c5e4-24b8-4248-9876-c7a1e19d769f" />

## 9. Resultados esperados
La práctica concluyó exitosamente con la creación de una imagen Docker optimizada para producción. Se logró automatizar el proceso de despliegue, pasando de una ejecución manual dependiente de Node.js local a un contenedor autosuficiente servido por Nginx. La aplicación visualiza correctamente los datos del backend, confirmando la correcta configuración de red y puertos.

## 10. Bibliografía
* Docker Inc. (2024). *Dockerfile reference*. https://docs.docker.com/engine/reference/builder/
* Docker Inc. (2024). *Multi-stage builds*. https://docs.docker.com/build/building/multi-stage/
* React Documentation. (2024). *Deployment*. https://react.dev/
