Postgresql y pgadmin con docker compose

 1.Creamos una caperta en donde se encontrara nuestro archivo YML
![image](https://user-images.githubusercontent.com/91229151/209200175-b1fbfc04-a769-49b4-a4ff-d087d6c10a59.png)

### 2.Accedemos a nuestra carpeta que acabamos de crear utilizamos el comando cd.
![image](https://user-images.githubusercontent.com/91229151/209200296-756c0564-d722-4998-a663-fe36f3092b46.png)

### 3.Una vez dentro de la carpeta, vamos a crear el archivo en el cual encontraremso nuestros contenedores, para ello ocupamos el comando vi.
![image](https://user-images.githubusercontent.com/91229151/209218188-eebf0065-f6a2-4ed3-9346-9e1c37e81ec1.png)

### 4.Una vez creado nuestro archivo vamos a editarlo para crear el contenedor de postgres y pgadmin nos quedaria asi.
### -Contenedor de Postgres
![a3](https://user-images.githubusercontent.com/91167276/201827028-9b5afdf3-b463-4b57-be28-b0d82179155a.JPG)
### -Contenedor de pgadmin.
![a4](https://user-images.githubusercontent.com/91167276/201827493-af0a08bf-bd26-4615-9f65-b9ddc2196aeb.JPG)
### 5.Una vez configurado guardamos con el comando :w y salimos con el comando :q!. Con el comando cat verificamos que el archivo se haya guardado bien.
![a5](https://user-images.githubusercontent.com/91167276/201828173-1e2c6828-51a2-4dda-9ec9-42cde20ce9c8.JPG)
### 6.Ahora colocamos el comando docker-compose up -d para que se creen los contenedores.
![a6](https://user-images.githubusercontent.com/91167276/201828537-82207b06-f73d-4563-8181-1431fe3b04b5.JPG)
### 7.Comprobamos que se haya creado, abrimos el puerto 8090 y colocamos el usuario y contraseña que asignamos.
![a7](https://user-images.githubusercontent.com/91167276/201829305-21478872-521e-4626-9bc9-9ec20d4d29a0.JPG)
### 8.Procedemos a crear un nuevo servidor.
![a8](https://user-images.githubusercontent.com/91167276/201829479-f140a720-ca75-46bf-a141-5097a6aadde5.JPG)
### 9.configurasmos las conexion.
![a9](https://user-images.githubusercontent.com/91167276/201829702-e52ba8b4-f2ea-4027-a541-5bf5154020e7.JPG)
### 10.Una vez configurado eso nos queda algo asi.
![a10](https://user-images.githubusercontent.com/91167276/201829784-a26b3a21-03ea-4c3b-ae15-05cbe17f1146.JPG)
### 11.Procedemos a crear la base de datos
![a11](https://user-images.githubusercontent.com/91167276/201829888-ba69c62f-ea5a-4f7a-b4e6-6568e1176495.JPG)
### 12.Le ponemos un nombre y damos en guardar.
![a12](https://user-images.githubusercontent.com/91167276/201830041-6280a24d-f8ee-4e2a-9255-4b1d8806c6e4.JPG)
## Listo tenemos creado nuestros contenedores junto a la base de datos.
![a13](https://user-images.githubusercontent.com/91167276/201830261-db41c9cc-0873-4a67-8247-44bd7dabe4b3.JPG)
