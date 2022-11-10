INFORME DE LA PRACTICA 

PASO 1: CREAR UNA CUENTA EN DOCKER.HUB.

![image](https://user-images.githubusercontent.com/91229151/201003067-605fa2ce-b494-46c5-a509-75da95370fed.png)

PASO 2: UNA VEZ REALIZADO EL PASO 1 NOS DIRIGIMOS A PLAY WITH DOCKER 

![image](https://user-images.githubusercontent.com/91229151/201003284-9e2fd2a1-1deb-4638-aca5-271cd9ea3b0f.png)

PASO 3: INICIAMOS PRECIONANDO START ,NOS MUESTRA UNA VENTANA DE ESTA FORMA: 

![image](https://user-images.githubusercontent.com/91229151/201003513-b72cf6c2-6814-4e87-9783-d552203726e1.png)

PASO 4: CREAMOS EL CONTENEDOR DE PGADMIN CON EL SIGUIENTE COMANDO 
docker run -d --name pgadmin -p 8090:80 -e PGADMIN_DEFAULT_EMAIL=dftenecota@sudamericano.edu.ec -e PGADMIN_DEFAULT_PASSWORD=admin dpage/pgadmin4

![image](https://user-images.githubusercontent.com/91229151/201004406-7c942a7e-fa21-417d-8c1e-bbb7d30651f3.png)

PASO 5:  PRESIONAMOS ENTER PARA QUE SE INICIE LA DESCARGA 

![image](https://user-images.githubusercontent.com/91229151/201004852-a0d3f537-4f88-4a61-87c9-3b05fbf4f1c7.png)

PASO 6: CREAMOS EN CONTENEDOR DE POSTGRESQL CON EL SIGUIENTE COMANDO :
docker run -d --name dbpsql -e POSTGRES_PASSWORD=medallas  -p 5432:5432 postgres

![image](https://user-images.githubusercontent.com/91229151/201005239-fe798925-4b8f-4f61-afb1-c86573e6f149.png)

PASO 7: PRESIONAMOS ENTER PARA QUE SE INICE LA INSTALACION 

![image](https://user-images.githubusercontent.com/91229151/201005590-15840080-35d0-4830-a14c-c449a3cbb423.png)

PASO 8: INGRESAMOS LAS CREDECIALES CREADAS ANTERIORMENTE EN LOS CONTENEDORES  PARA SU RESPECTIVA COMRPOBACION EN EL PUERTO PDADMIN  .

Email : dftenecota@sudamericano.edu.ec
password : admin 

![image](https://user-images.githubusercontent.com/91229151/201006079-fbd971eb-a43d-4161-b6e7-833eefe445d5.png)


PASO 9: INICIAMOS SESION Y PODREMOS OBSERVAR ESTA VENTANA: 

![image](https://user-images.githubusercontent.com/91229151/201006216-dae09966-a2cd-466f-8780-66a7b97ea953.png)

PASO 10: CREAMOS LA RED EN EL CONTENEDO CON EL SIGUIENTE COMANDO : 
docker network create --attachable redarwintenecota

![image](https://user-images.githubusercontent.com/91229151/201006628-2592f251-5bad-4d61-b15e-ad8ab6a2e2c6.png)

PASO 11: AGREGAMOS  EL CONTENEDOR DE POSTGRESQL CON EL SIGUIENTE COMANDO :

docker network connect redarwintenecota dbpsql

![image](https://user-images.githubusercontent.com/91229151/201007750-d3c18ee8-5206-4d4b-bf4a-a3dcfe1ccf9a.png)

PASO 12: AGREGAMOS  EL CONTENEDOR DE PGADMIN CON EL SIGUIENTE COMANDO :

docker network connect redarwintenecota pgadmin
![image](https://user-images.githubusercontent.com/91229151/201007858-b862e0fa-6a21-4c34-9750-9a3e6a19cc83.png)


PASO 13 : VERIFICAMOS LOS CONTENEDORES CREADOS EN LA RED CON EL SIGUIENTE COMANDO : 
docker inspect redarwintenecota 

![image](https://user-images.githubusercontent.com/91229151/201008014-d9c9287a-e72c-4862-a041-21774594eff0.png)


PASO 14: EL COMANDO UTILIZADO EN EL PASO 13 NOS MUESTRA LAS IPS ASIGNADAS A CADA CONTENEDOR 

![image](https://user-images.githubusercontent.com/91229151/201008261-2d64d0c8-d058-45e4-9638-f2e9651730a2.png)

![image](https://user-images.githubusercontent.com/91229151/201008420-1a58266f-6383-48ae-8e8d-58723b54794e.png)





 
