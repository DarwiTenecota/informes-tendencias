# informes-tendencias
informes de cada practica, paso a paso. 
Crear una cuenta en docker 

![image](https://user-images.githubusercontent.com/91229151/197310415-2ab98a07-b247-4c9b-8780-e4b8534749ee.png)

ingresar a Play with Docker

![image](https://user-images.githubusercontent.com/91229151/197310460-83d27819-c5a2-4b4d-8614-531e2bf67b34.png)

ingresar el comando : docker run --name serverweb -p 80:80 -d nginx

para cargar las librerias 

![image](https://user-images.githubusercontent.com/91229151/197310606-a8f9d055-3591-4fc2-8299-a6cf1a8ef53d.png)

para verificar si esta corriendo o esta correctamente instalado utilizar el comando : docker ps

![image](https://user-images.githubusercontent.com/91229151/197310636-16733ae2-fcb2-43ab-b8a6-e3a97ca40136.png)

poner en OPEN PORT QUE ESTA A LADO DEL IP poner el puerto 80

![image](https://user-images.githubusercontent.com/91229151/197310755-71b9cdbe-30ec-4f44-aff0-c5072f19305b.png)

COMANDO BASICO DE DOCKER 

DOCKER RUN ---> CORRER UN CONTENEDOR

DOCKER PS ---->> LISTAN LOS CONTENEDORES QUE ESTAN CORRIENDO 

(-- NAME SERVERWEB) -----> ES PARA COLOCAR UN NOMBRE Y SIRVE PARA IDENTIFICAR EL DOCKER Y DONDE ESTA CORRIENDO

80:80 ---> MAQUINA ANFITRIONA 


-d ===> nos sirve o permite seguir ocupando la linea de comandos caso contrario no se va a poder ,ademas si usamos el proceso pasa a segundo plano 

nginx ==> imagen que se descargan ,en base a esa imagen se crea el contenedor

CREAR UN ARCHIVO HTML EN EL REPOSITORIO.

![image](https://user-images.githubusercontent.com/91229151/197312315-546f42d9-d79f-4d91-a465-ee3763f4d008.png)

INSERTAR CODIGO HTML DONDE APAREZCA EL NOMBRE:

![image](https://user-images.githubusercontent.com/91229151/197314401-669e3fdd-be47-4c91-b25d-db9d760c9669.png)

REGRESAR A PLAY WITH DOCKER

INGRESAR EL COMANDO : wget /////seguido de el enlace o link del repositorio html//// https://github.com/DarwiTenecota/informes-tendencias/blob/main/index2.html

![image](https://user-images.githubusercontent.com/91229151/197314650-0ab0e490-1db7-4918-8c93-af29c0cb5a0a.png)

ingresar el comando ls para verificar si se descargo 

![image](https://user-images.githubusercontent.com/91229151/197315433-b3dad339-320e-46d7-99f5-4291ed229e48.png)

ingresar el comando docker cp index2.html serverweb:/usr/share/nginx/html/index2.html

Es para extraer o añadir la informacion del html 

PRESIONAR EL OPEN PORT  Y ESCRBIR 80 

![image](https://user-images.githubusercontent.com/91229151/197315629-a4d369b1-e2d1-4d87-93e4-2f25940206b9.png)

EN CASO DE QUE NO SE EJECUTE O PRESENTE ERROR ,DEBERIAMOS CLONAR EL REPOSITORIO 

INGRESAR EL COMANDO: vi index2.html

ingresar el comando : git clone https://github.com/DarwiTenecota/informes-tendencias 

ingresar el comando ls ,para verificar si se cargo.

Ejecutar el comando docker cp index2.html serverweb:/usr/share/nginx/html/index.html

![image](https://user-images.githubusercontent.com/91229151/197315725-2a876ad2-3be3-4d8a-bab9-2c62b2110459.png)

presionar en el open port y ingresar 80 y esta vez si nos debe salir 


![image](https://user-images.githubusercontent.com/91229151/197315745-9b5429bd-b014-44e7-a584-34c7ac7ec453.png)

cabe mencionar que en el enlace que se abre se debe poner /index2.html


![image](https://user-images.githubusercontent.com/91229151/197315772-b2e7df23-6228-4cd8-b16a-cf6e540cb1d0.png)









