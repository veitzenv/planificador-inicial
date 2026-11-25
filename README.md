# Planificador Inicial

Herramienta impulsada por IA con el propósito de facilitar la planificación para docentes de Inicial, utilizando como fuente el programa de ANEP. Spring Boot, PostgreSQL y React.

## Requisitos

- Git
- JDK 21
- Docker y Docker Compose

## Cómo levantarlo

1. Clonar el repositorio con el comando `git clone https://github.com/veitzenv/planificador-inicial.git` y la dirección del repositorio. Luego, cd planificador-inicial.
2. Crear el .env copiando el de ejemplo con el comando `cp .env.example .env` y completar la contraseña en el archivo nuevo.
3. Levantar la base con el comando `docker compose up -d`
4. Desde la carpeta del backend, ejecutar el comando `./mvnw spring-boot:run`. Si se hace desde otra, no va a encontrar el .env
5. Comprobar que levantó ejecutando el comando `curl http://127.0.0.1:8080/actuator/health`. La respuesta debe incluir: `"status":"UP"`

## Diferencias Linux/Windows

- Correr el backend: en Linux `./mvnw spring-boot:run`; en Windows (PowerShell) `.\mvnw.cmd spring-boot:run`.
- Comprobar que levantó: en PowerShell usar `curl.exe` en vez de `curl`, o abrir `http://127.0.0.1:8080/actuator/health` en el navegador.
- Fin de línea: el archivo `.gitattributes` normaliza los fines de línea para que el repo funcione igual en los dos sistemas.


