# Práctica No 6 - Creación de Imágenes Personalizadas (Dockerfile) para React

## 1. Título
**Práctica No 6**: Contenerización de una aplicación Frontend (React) mediante Dockerfile y Multi-stage Builds.

## 2. Tiempo de duración
Aproximadamente 2 horas.

## 3. Fundamentos
En esta práctica se profundiza en el concepto de **Infraestructura como Código**, dejando de lado la ejecución manual de contenedores para automatizar la creación de imágenes mediante un **Dockerfile**.
[cite_start]El Dockerfile actúa como una "receta" que contiene las instrucciones precisas para construir una imagen de Docker, asegurando que el entorno sea reproducible y estandarizado[cite: 2328, 2329].
Se aplicaron conceptos avanzados como:
* [cite_start]**Multi-stage builds**: Una técnica que permite usar una imagen intermedia (Node.js) para compilar la aplicación y una imagen final ligera (Nginx) para servirla, optimizando drásticamente el peso del contenedor final[cite: 2392, 2394].
* [cite_start]**.dockerignore**: Archivo fundamental para excluir carpetas locales pesadas como `node_modules` del contexto de construcción, mejorando la velocidad del `build`[cite: 2377].

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
*Figura 1. Backend ejecutándose en el puerto 8000.*
![alt text](<Captura de pantalla 2025-11-22 215110.png>)

**Paso 2: Verificación local del Frontend.**
Antes de crear el contenedor, se verificó que la aplicación React funcionara correctamente en el entorno local mediante `npm run dev`.
*Figura 2. Aplicación React funcionando localmente.*
> [¡PEGA AQUÍ TU CAPTURA DEL NAVEGADOR CON LA APP EN MODO DEV!]

**Paso 3: Creación de archivos de configuración.**
Se creó el archivo `.dockerignore` para excluir `node_modules` y el `Dockerfile` configurado en dos etapas: compilación con Node.js y servicio con Nginx Alpine.
*Figura 3. Estructura del Dockerfile en VS Code.*
> [¡PEGA AQUÍ TU CAPTURA DEL CÓDIGO DOCKERFILE!] (Si no la tomaste, puedes tomarla ahora de tu VS Code).

**Paso 4: Construcción de la imagen (Build).**
Se ejecutó el comando `docker build -t mi-frontend-react .` para generar la imagen binaria a partir del Dockerfile.
*Figura 4. Proceso de construcción exitoso en la terminal.*
> [¡PEGA AQUÍ LA CAPTURA DONDE SE VE "WRITING IMAGE... DONE" O DOCKER BUILD TERMINADO!] (La imagen 'image_2d1bdf.jpg' que enviaste).

**Paso 5: Despliegue y Validación.**
Se inició el contenedor con `docker run -d -p 8080:80...` y se accedió al navegador para confirmar que Nginx está sirviendo la aplicación correctamente conectada a la API.
*Figura 5. Aplicación ejecutándose desde el contenedor Docker (localhost:8080).*
> [¡PEGA AQUÍ LA ÚLTIMA CAPTURA QUE ENVIASTE: 'image_2d273d.jpg'!]

## 9. Resultados esperados
La práctica concluyó exitosamente con la creación de una imagen Docker optimizada para producción. Se logró automatizar el proceso de despliegue, pasando de una ejecución manual dependiente de Node.js local a un contenedor autosuficiente servido por Nginx. La aplicación visualiza correctamente los datos del backend, confirmando la correcta configuración de red y puertos.

## 10. Bibliografía
* Docker Inc. (2024). *Dockerfile reference*. https://docs.docker.com/engine/reference/builder/
* Docker Inc. (2024). *Multi-stage builds*. https://docs.docker.com/build/building/multi-stage/
* React Documentation. (2024). *Deployment*. https://react.dev/