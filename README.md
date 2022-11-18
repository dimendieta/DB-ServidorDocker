# DB-ServidorDocker


                                                      Postgresql

docker run -d --name dbpsql -e POSTGRES_PASSWORD=admin -p 5432:5432 postgres


![image](https://user-images.githubusercontent.com/91167870/200968606-0dff043d-a8f2-40b0-9198-c0b86722323b.png)
                                                       PGadmin

docker run -d --name pgadmin -p 8090:80 -e PGADMIN_DEFAULT_EMAIL=dimendieta.2@sudamericano.edu.ec -e PGADMIN_DEFAULT_PASSWORD=admin dpage/pgadmin4



![image](https://user-images.githubusercontent.com/91167870/200968462-30b74128-a43a-4e03-921b-ebcf13d1fb52.png)


Creamos una red (redsuda)

docker network create --attachable redsuda
![image](https://user-images.githubusercontent.com/91167870/200968818-ceb3b74d-f624-407f-8e53-0e13b4fba8fb.png)




Agregamos contenedores a la red

Contenedor de postgresql: docker network connect redsuda dbpsql
Contenedor de pagadmin: docker network connect redsuda pgadmin

![image](https://user-images.githubusercontent.com/91167870/200969012-b7110893-a769-4f79-935b-fb842d26bc7c.png)

                                                             Verificamos contenedores conectados a la red

docker inspect redsuda

![image](https://user-images.githubusercontent.com/91167870/200969163-65aa0687-f2e4-4207-9615-424b395dddd7.png)

                                                             Abrimos el puerto 8090 e iniciamos sesión 
                                                             
![image](https://user-images.githubusercontent.com/91167870/200969303-bee7a27e-10c7-46c6-8b8d-a1d0d6ec6854.png)

                                                             Creamos el Servidor
        
![image](https://user-images.githubusercontent.com/91167870/202759657-f2c67abc-3950-4b61-8b7e-11072d8ebe3e.png)

![image](https://user-images.githubusercontent.com/91167870/202759130-d82038b0-e299-441a-90ab-993787528cf8.png)


