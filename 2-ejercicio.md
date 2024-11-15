# Ejercicio
Configurar SonarQube utilizando Docker Compose, para esto necesitas dos servicios:
- Servicio: SonarQube
- Desde el host es necesario acceder a SonarQube por lo que necesitas mapear el puerto correspondiente.
- Servicio: PostgreSQL (existen otras opciones: Microsoft SQL Server, Oracle)
- Coloca un healtcheck para cada uno de los servicios.
- Los dos servicios deben pertenecer a una red de tipo bridge
- Investiga cuáles son los volúmenes necesarios para cada servicio
- Investiga cuáles son las variables de entorno para que los servicios funcionen de manera adecuada.
## Crear el archivo docker-compose.yaml
## Ejecutar el archivo docker-compose.yaml
```
docker compose -f docker-compose.yaml up -d
```
![image](https://github.com/user-attachments/assets/bc79fdef-662e-4d0f-abb7-5e7d30936632)
![image](https://github.com/user-attachments/assets/60d31f86-c778-4b5d-981e-79690dff97b1)
## Verificar los contenedores en ejecución
```
docker compose -f docker-compose.yaml ps
```
![image](https://github.com/user-attachments/assets/c8d04a40-d6d1-4a20-a34a-836782b8afae)
# Acceder a SonarQube
```
http://localhost:9000
```
![image](https://github.com/user-attachments/assets/4c9920f2-534b-40ba-8648-5fd33ba95dbe)
![image](https://github.com/user-attachments/assets/690cda2d-0e4f-42e9-aa3e-0a05cd05c2c2)

# Detener y eliminar los contenedores
```
docker compose -f docker-compose.yaml down
```
![image](https://github.com/user-attachments/assets/712dc566-2f6a-468a-b7f3-34de4b072d85)
![image](https://github.com/user-attachments/assets/e10e8a89-fe15-4d32-8c9d-3326d2f162ee)
