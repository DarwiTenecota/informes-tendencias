Crear Docker-compose 
Dentro de una instancia, debe crear una carpeta (darwint) e ingresar, luego, nuevamente crear otra carpeta (db) donde estará el back-end e ingresar. Dentro de "bd" debe crear el archivo "docker-compose.yml".

![image](https://user-images.githubusercontent.com/91229151/209409969-cb20bdf7-298c-4bea-853a-7d7d9d5caee3.png)

![image](https://user-images.githubusercontent.com/91229151/209410033-40bc5a98-dd26-4c83-a0f4-ae02b85ce23e.png)

Docker-compose.yml

Al crear el archivo docker-compose, en su contenido debe especificarse la version de los contenedores, nombres, puertos, usuarios, contraseñas, entre otros, para generar el contenedor del pgAdmin y postgres.

![image](https://user-images.githubusercontent.com/91229151/209410225-26ba6e40-6bd6-4c58-a288-a7c9851aba4e.png)

Al guardar y salir del archivo, debe ejecutarlo para generar los contenedores.

![image](https://user-images.githubusercontent.com/91229151/209411303-ae82d92d-f9cd-48dc-af25-12a63c1882a3.png)

Crear servidor Postgres
Para continuar con el tutorial, antes debe abrir el puerto 8090 e ingresar al pgAdmin

![image](https://user-images.githubusercontent.com/91229151/209411622-48758409-5365-49bc-9130-5f644e597305.png)

![image](https://user-images.githubusercontent.com/91229151/209411648-855774e3-a334-4947-99e1-3932a1fe9efb.png)

Seguidamente, crear un nuevo servidor con los datos detallados para el contenedor postgres

![image](https://user-images.githubusercontent.com/91229151/209411718-abef8b4a-7901-4ded-a6c4-aa1f36957976.png)

Al crearlo, obtendrá el servidor creado correctamente

En la carpeta "db", se debe clonar el git donde está la app para el back-end para luego editar varios archivos que servirán para la conexión con la base de datos y front-end.

![image](https://user-images.githubusercontent.com/91229151/209411966-9d523757-f039-410e-8edc-9e37221e3613.png)

Se debe buscar el archivo "application.yml" o "application.properties" para editar los campos de datasource y enableCors.

![image](https://user-images.githubusercontent.com/91229151/209412106-80fa23e8-b41d-414f-a13b-515e1f50fa3f.png)

Al ingresar al editor, se debe editar el datasource con los datos del contenedor Postgres (url, usuario y contraseña), y en el enableCors poner la dirección URL del puerto 3000.

procedemos a abrir el puerto 3000 y se nos abrira una nueva ventana donde esta creado el front-end.

![Captura de pantalla (26)](https://user-images.githubusercontent.com/91167276/204882519-923e3a4e-3e43-41d9-8e3b-4db72edf2595.png)

Le damos en usuario y nos permite ver la informacion que se encuentra en la base de datos.

![Captura de pantalla (27)](https://user-images.githubusercontent.com/91167276/204882781-971e1d79-ce26-44e7-ac20-6df92bf6a15f.png)



