INFORME DE LA PRACTICA 

PASO 1: INCIAR SESION O CREAR  EN EL CASO DE NO TENER UNA CUENTA EN DOCKER.HUB.

![image](https://user-images.githubusercontent.com/91229151/201003067-605fa2ce-b494-46c5-a509-75da95370fed.png)

PASO 2: UNA VEZ REALIZADO EL PASO 1 NOS DIRIGIMOS A PLAY WITH DOCKER 

![image](https://user-images.githubusercontent.com/91229151/201003284-9e2fd2a1-1deb-4638-aca5-271cd9ea3b0f.png)

PASO 3: INICIAMOS PRECIONANDO START ,NOS MUESTRA UNA VENTANA DE ESTA FORMA: 

![image](https://user-images.githubusercontent.com/91229151/201003513-b72cf6c2-6814-4e87-9783-d552203726e1.png)

PASO 4: CREAMOS EL CONTENEDOR DE PGADMIN CON EL SIGUIENTE COMANDO 
docker run -d --name pgadmin -p 8090:80 -e PGADMIN_DEFAULT_EMAIL=dftenecota@sudamericano.edu.ec -e PGADMIN_DEFAULT_PASSWORD=admin dpage/pgadmin4

![image](https://user-images.githubusercontent.com/91229151/201012682-1ad0c2e6-89d2-475c-a74f-c8e4d135b77e.png)


PASO 5:  PRESIONAMOS ENTER PARA QUE SE INICIE LA DESCARGA 

![image](https://user-images.githubusercontent.com/91229151/201012892-a8fa217f-ac05-4880-bf9d-f4c2e150188c.png)


PASO 6: CREAMOS EN CONTENEDOR DE POSTGRESQL CON EL SIGUIENTE COMANDO :
docker run -d --name dbpsql -e POSTGRES_PASSWORD=medallas  -p 5432:5432 postgres

![image](https://user-images.githubusercontent.com/91229151/201013020-9671bed1-d2fe-48de-82af-e0604773b1cf.png)

PASO 7: PRESIONAMOS ENTER PARA QUE SE INICE LA INSTALACION 

![image](https://user-images.githubusercontent.com/91229151/201013480-8be0091d-fca2-4807-be44-6b90cb5012f6.png)


PASO 8: INGRESAMOS LAS CREDECIALES CREADAS ANTERIORMENTE EN LOS CONTENEDORES  PARA SU RESPECTIVA COMRPOBACION EN EL PUERTO PDADMIN  .

Email : dftenecota@sudamericano.edu.ec
password : admin 

![image](https://user-images.githubusercontent.com/91229151/201006079-fbd971eb-a43d-4161-b6e7-833eefe445d5.png)


PASO 9: INICIAMOS SESION Y PODREMOS OBSERVAR ESTA VENTANA: 

![image](https://user-images.githubusercontent.com/91229151/201006216-dae09966-a2cd-466f-8780-66a7b97ea953.png)

PASO 10: CREAMOS LA RED EN EL CONTENEDO CON EL SIGUIENTE COMANDO : 
docker network create --attachable redarwintenecota

![image](https://user-images.githubusercontent.com/91229151/201013647-434d332c-e5bf-482f-b074-0ba90386715b.png)


PASO 11: AGREGAMOS  EL CONTENEDOR DE POSTGRESQL CON EL SIGUIENTE COMANDO :

docker network connect redarwintenecota dbpsql

![image](https://user-images.githubusercontent.com/91229151/201013780-c34b117d-b207-49f9-8111-aee9d055a29b.png)


PASO 12: AGREGAMOS  EL CONTENEDOR DE PGADMIN CON EL SIGUIENTE COMANDO :

docker network connect redarwintenecota pgadmin
![image](https://user-images.githubusercontent.com/91229151/201013901-74e385b9-677a-4024-949a-43a86cb1b177.png)



PASO 13 : VERIFICAMOS LOS CONTENEDORES CREADOS EN LA RED CON EL SIGUIENTE COMANDO : 
docker inspect redarwintenecota 

![image](https://user-images.githubusercontent.com/91229151/201014012-fcc9cc8d-e521-4717-ac9a-f846ef024db2.png)


PASO 14: EL COMANDO UTILIZADO EN EL PASO 13 NOS MUESTRA LAS IPS ASIGNADAS A CADA CONTENEDOR 
![image](https://user-images.githubusercontent.com/91229151/201014458-6499d935-ae1a-4700-9730-6fd2c481d2b1.png)


![image](https://user-images.githubusercontent.com/91229151/201014544-cafa16fc-2bd4-4ba6-9ce6-f7f7b8d3341e.png)






 
