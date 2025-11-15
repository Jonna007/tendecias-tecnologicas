
# Práctica No 3 - Gestión de Bases de Datos con y sin Volúmenes usando Docker y TablePlus

## 1. Título

**Práctica No 3**: Gestión de bases de datos mediante Docker y TablePlus

## 2. Tiempo de duración

Aproximadamente 2 horas.

## 3. Fundamentos

En esta práctica, trabajé con bases de datos PostgreSQL utilizando **Docker** para crear contenedores y **TablePlus** como herramienta gráfica. Aprendí a crear y administrar bases de datos, crear tablas, insertar registros y comprobar la persistencia de los datos con y sin el uso de volúmenes de Docker.

Se utilizó `docker run` para levantar contenedores PostgreSQL, y se realizaron conexiones desde TablePlus. Se verificó la persistencia de datos después de eliminar contenedores, y se aprendió a crear volúmenes con `docker volume create`.

Entre los comandos utilizados:

- `docker run --name ...`
- `docker stop`, `docker start`, `docker rm -f`
- `docker volume create` y montaje de volúmenes (`-v`)

## 4. Conocimientos previos

Para desarrollar esta práctica fue importante tener conocimientos sobre:
- PostgreSQL y su sintaxis SQL.
- Uso básico de Docker, contenedores y volúmenes.
- Manejo de TablePlus como herramienta gráfica para conectarse a bases de datos.
- Comandos de terminal.

## 5. Objetivos a alcanzar

- Conectarse a una base de datos PostgreSQL desde TablePlus y Terminal.
- Validar operaciones realizadas desde una herramienta en la otra.
- Entender cómo se comporta una base de datos con y sin persistencia usando volúmenes de Docker.

## 6. Equipo necesario

- **Computador:** DESKTOP-OM5U658
- **Sistema Operativo:** Windows 11 Pro (Versión 25H2)
- **Procesador:** Intel(R) Core(TM) 7 240H (2.50 GHz)
- **Memoria RAM:** 32,0 GB
- **Software:** Docker Desktop, TablePlus, Terminal (Warp)
- **Conexión a Internet** para documentación y plataforma

## 7. Material de apoyo

- Documentación oficial de Docker
- Manual oficial de PostgreSQL
- Manual de TablePlus
- Videos y guías proporcionados por el docente en la plataforma EVA

## 8. Procedimiento

### Parte 1: Base de datos sin volumen

1. Crear contenedor PostgreSQL `server_db` sin volumen.
![image](https://github.com/user-attachments/assets/f25104a9-d38a-4216-9316-0aa17111cade)
2. Conectarse desde TablePlus.
![image](https://github.com/user-attachments/assets/4de119e9-be96-40c1-94e2-a7990efebe4a)
3. Crear base de datos `test` y tabla `customer`.
![image](https://github.com/user-attachments/assets/04933e77-cf75-4f4e-992d-b4b600d50fee)

4. Insertar registros.
![image](https://github.com/user-attachments/assets/6d9f97f7-73de-444e-a8f9-e587d9fab4b8)
![image](https://github.com/user-attachments/assets/623d076b-54ce-4d1d-9062-487a93d94d23)

5. Detener y eliminar el contenedor.
![image](https://github.com/user-attachments/assets/d859cb18-149a-49e3-a8af-43c172fed463)

6. Comprobar que los datos no se conservaron (porque no usamos volumen).
![image](https://github.com/user-attachments/assets/975eb8a3-60c7-4de1-bd47-6ef2545d4f78)


### Parte 2: Base de datos con volumen

1. Crear volumen `pg_data` con `docker volume create`.
![image](https://github.com/user-attachments/assets/c50901dd-9471-4de1-83b3-aeee7b1d7962)

2. Crear contenedor `server_db2` y montar volumen.
3. Conectarse desde TablePlus.
![image](https://github.com/user-attachments/assets/e43ccee3-2f3b-4e86-85c1-a395af2411e6)

4. Crear base de datos `test`, tabla `customer`, e insertar datos.
![image](https://github.com/user-attachments/assets/13ac4d90-96e4-449f-a016-8a10e2c766dd)

![image](https://github.com/user-attachments/assets/6eae1f1b-1ed0-4ffa-a47a-31539e726d6d)

5. Detener y eliminar el contenedor.
![image](https://github.com/user-attachments/assets/589e2625-fded-4afc-ac86-0423fb816be1)
![image](https://github.com/user-attachments/assets/63d16d80-642a-4af9-820a-424a3b5b5c8c)

6. Volver a crear `server_db2` con el volumen `pg_data`.
![image](https://github.com/user-attachments/assets/e9e24ca2-1498-44e4-b3cd-5bcc2f6a74e8)

7. Comprobar que la base de datos y sus registros **sí persistieron**.
![image](https://github.com/user-attachments/assets/22527aa9-6f64-45a8-a381-2b13031e91ac)


## 9. Resultados esperados

Gracias a esta práctica, comprendí cómo se puede trabajar con PostgreSQL en Docker, y cómo la información se pierde o se conserva según se usen o no volúmenes. TablePlus facilitó la administración de datos y la conexión fue sencilla con las credenciales configuradas.

Con esto, reforcé conocimientos sobre contenedores, persistencia de datos y administración de bases de datos.

## 10. Bibliografía

- Docker Inc. (2024). _Manage data in Docker_ (Volumes). https://docs.docker.com/storage/volumes/
- TablePlus. (2024). _Modern, native tool for relational databases_. https://tableplus.com/
- PostgreSQL Global Development Group. (2023). _PostgreSQL 16 documentation_. https://www.postgresql.org/docs/
