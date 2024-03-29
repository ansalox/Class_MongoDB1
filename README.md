# Class_MongoDB

una vez instalado podemos empezar a trabajar con mongo DB

para ello vamos a las consolas que teniamos abiertas mongo y mongod

nos ubicmaos en la de mongo que es el cliente

![image](https://user-images.githubusercontent.com/54609399/138191271-1236b65d-32f8-4921-948a-a92e23a39239.png)

tambien vamos abrir y tener listo compass, para esto ejecutamos la aplicacion en caso que la hayan cerrado y la dejamos lista

![image](https://user-images.githubusercontent.com/54609399/138191350-389e43d7-ab59-4286-b132-a9ddef37ee09.png)

tenemos que entrar a las BD en compass y lo hacemos de la siguiente manera
vamos a la consola mongo y copiamos la siguiente linea usando ctrl + shift + c, ya que si usamos ctrl + c no copia nada

![image](https://user-images.githubusercontent.com/54609399/138191465-cfc96b70-fe33-4e32-b610-144d64ea0581.png)

mongodb://127.0.0.1:27017/

pegamos esta lina en el compas en la siguiente parte y damos conectar (importante copiar toda la linea hasta el ultimo slash)

![image](https://user-images.githubusercontent.com/54609399/138191539-680a736f-3a7b-499f-87d0-16708676f09f.png)

una vez conecte nos saldra lo siguiente

![image](https://user-images.githubusercontent.com/54609399/138191609-22df5976-dbad-4d8d-881e-f322a8b97b74.png)

con esto estamos listos para continuar


1 - Para ver todas las bases de datos que tenemos en MongoDB en consola

```
show dbs
```
![image](https://user-images.githubusercontent.com/54609399/138028777-2c4971fe-679e-4cfb-8666-cba56611f2a7.png)

Para verlas en Mongo Compass

![image](https://user-images.githubusercontent.com/54609399/138150837-ebedf815-add3-4b42-ab84-45734f22277e.png)

2 - Ver la DB actual en la que estamos posicionados en consola, mongo nos pone una BD ficticia llamada test ya que no hemos seleccionado ninguna BD

```
db
```

![image](https://user-images.githubusercontent.com/54609399/138027987-f4ca5f94-34de-409e-a709-d4ab6b87aaa8.png)

En Compass solo los muestra la lista de BD que tenemos pero no estamos posicionado en ninguna

![image](https://user-images.githubusercontent.com/54609399/138151350-ac17962f-ce03-4e62-9164-405b1860a968.png)

3 - Crear y/o usar una DB, y luego comprobamos si en verdad estamos ubicados en la DB con el comando db

```
use pruebadb
```

![image](https://user-images.githubusercontent.com/54609399/138027109-18967b6b-2b03-429b-9e1b-41c8c00b933d.png)

En Compass hacemos el siguiente proceso:

![image](https://user-images.githubusercontent.com/54609399/138151568-b27df352-6e29-40b3-a74a-24921e26cffc.png)

Debemos poner el nombre de la DB y crearle una coleccion inicial obligatoriamente si las BD no tienen una coleccion esa BD no existe, no seleccionamos ninguno de los check ya que son plantillas con cosas creadas por defecto que no necesitamos.

![image](https://user-images.githubusercontent.com/54609399/138151803-4d83f266-0f5a-499a-9491-3fd24986e813.png)

YA podemos ver la BD creada en la lista de bases de datos (sinos fijamos no sale pruebadb que fue la que creamos en consola)

![image](https://user-images.githubusercontent.com/54609399/138151863-3f557884-2164-4b20-9865-1d4fbb21249d.png)

Dentro de exampleDB  si le damos click podemos ver que hay una coleccion user

![image](https://user-images.githubusercontent.com/54609399/138151908-ca2a7f0c-3f60-4336-ac0d-9b3d85e4fbe4.png)



4 - ya creamos DB en consola y en compas ahora vamos a ver como se eliminan pero resulta que en consola La DB no se puede eliminar porque no existe aun ya que no se le creo una coleccion como en compass, para que MongoDB la ponga existente se le debe crear una colección primero sino queda como fantasma intentemos eliminarla usando el siguiente comando y veremos que sigue quedando si usamos el comando db

```
db.dropDatabase()
```

![image](https://user-images.githubusercontent.com/54609399/138192774-4e957cd4-bcaf-48e5-8c14-04dbc843bb8a.png)

En compass esto no pasa porque nos obliga a crear una coleccion para poder crear una DB entonces en compass por eso si existe

5 - Ahora vamos a crear una colección en una DB en consola con esto ya existiria la DB y dejaria de ser fantasma, podemos ver las colecciones que tengamos con el comando show collections

```
db.createCollection("user")
```

```
db.createCollection("item")
```

```
show.collections
```

![image](https://user-images.githubusercontent.com/54609399/138027191-ff790bbc-8665-47a1-b33d-7976f0a9356b.png)

Para crear otra coleccion en Compass, realizamos el siguiente paso:

![image](https://user-images.githubusercontent.com/54609399/138152247-ca01f5e7-1791-44c8-82ca-cc6a70d2458b.png)

Ponemos el nombre de la coleccion pero no seleccionamos ningun check porque nos genera codigo que no nos sirve y nos puede afectar la DB

![image](https://user-images.githubusercontent.com/54609399/138152290-e5d5abcc-250e-4ec4-853a-22d89e73a757.png)

En compass podemos ya ver en la lista de colecciones de la DB exampledb que esta l anueva coleccion

![image](https://user-images.githubusercontent.com/54609399/138152354-cab4b5fe-0a9e-4a2a-ab4d-54685299f3b6.png)

Si refrescamos el compas podemos ver tambien la BD creada desde la consola

![image](https://user-images.githubusercontent.com/54609399/138193386-1b829b6f-e378-4ff4-9dc4-34eb3119ea3c.png)

y si usamos el comando show dbs en la consola vemos tambien las dos DB 

![image](https://user-images.githubusercontent.com/54609399/138193609-80da1840-c33a-4a21-9247-460ee965c6ec.png)

6 - Eliminar coleccion en consola (Ahora si podemos porque ya no es un fantasma), luego de eliminar podemos ver las colecciones y no deberia de aparecer

```
db.item.drop()
```

![image](https://user-images.githubusercontent.com/54609399/138027255-6fd7e6c0-9354-4d55-b68f-bccebd0f86a5.png)

Eliminar en compass

![image](https://user-images.githubusercontent.com/54609399/138152595-dc3eaed1-5f2b-40cd-8f0d-530726c17b59.png)

Nos pide por seguridad escribir el nombre de la coleccion para saber que no es un kacker o un scropt ejecutandose malisioso

![image](https://user-images.githubusercontent.com/54609399/138152642-3c2a52ce-364f-42cb-a738-bccdc2401a2b.png)

Podemos ver que ya se elimino la coleccion

![image](https://user-images.githubusercontent.com/54609399/138152693-144ed89d-0de3-4c9c-a765-d4023f04ef74.png)


7 - Eliminar correctamente una DB en consola, ahora que  ya tiene colecciones podemos eliminarla

```
db.dropDatabase()
```

![image](https://user-images.githubusercontent.com/54609399/138196099-ef89f1a8-e216-430d-ab17-082c2524604a.png)

si suamos el comando show dbs podeos ver que ya no esta la DB

![image](https://user-images.githubusercontent.com/54609399/138196239-0851ddc3-6974-4e24-b092-81a643592a4d.png)


Para eliminar una DB en compass

![image](https://user-images.githubusercontent.com/54609399/138152917-fe5f26b3-ee4c-4cef-8fe6-5c6c8fa8ecc5.png)

Por seguridad nos pide el nombre de la DB

![image](https://user-images.githubusercontent.com/54609399/138153036-24d44fbf-381a-4ee8-8443-6c1018cb4b3d.png)

verificamos que no este ya la DB en compass

![image](https://user-images.githubusercontent.com/54609399/138153081-52a13302-f86c-461d-a3dd-3e9438140f17.png)


8 - Cambiar nombre de una colección (Para este paso necesitamos crear otra vez pruebadb y sus colecciones user e item tambien la de compass exampleDB y sus colecciones user e item)

```
db.["user"].renameCollection("userapp")
```

![image](https://user-images.githubusercontent.com/54609399/138027304-7f7112b8-10a6-4be8-8b44-53329a03e1b4.png)


En compass no se puede editar el nombre de las colecciones 

NOTA: el nombre de las bases de datos no se pueden editar ni en compass ni en consola

9 - Crear documentos en Compass.

Nos ubicamos dentro de la colección

![image](https://user-images.githubusercontent.com/54609399/138153728-8e99b743-a218-478f-bca0-fec89fba383b.png)

seleccionamos add data

![image](https://user-images.githubusercontent.com/54609399/138153775-9a8960c5-d235-4375-b346-805038542027.png)

Damos click en insert document

![image](https://user-images.githubusercontent.com/54609399/138153852-aea13e09-b3f1-471d-b476-09cb755e8871.png)

Seleccionamos la siguiente opcion

![image](https://user-images.githubusercontent.com/54609399/138153977-5f9875d9-f93a-4063-97fd-c6d0e08910df.png)

siempre genera un ID por defecto no se debe eliminar esto es lo que identifica cada documento de mongo como unico para mongo se llaman ObjetID

![image](https://user-images.githubusercontent.com/54609399/138154055-696a9374-92b2-4c48-a7fe-b22c2f722b4a.png)

insertamos un nuevo campo con el +

![image](https://user-images.githubusercontent.com/54609399/138154107-4383c916-b98d-43f9-b6b9-4d05d6ea7eb4.png)

![image](https://user-images.githubusercontent.com/54609399/138154218-118597b9-543f-4f25-b711-e065827e89a2.png)

Escribirmos en la primer aparte el nombre de la propiedad como name y en la segunda parte el nombre del valor ejemplo Pepe, si nos fijamos a la derecha sale el tipo de dato

![image](https://user-images.githubusercontent.com/54609399/138154256-215896e2-3d2d-4574-9119-f531bad9a386.png)

Ahora vamos a crear otro campo desde el mas ojo si le dan a la X eliminan el commpo creamos el campo age de edad y le ponemos 25

![image](https://user-images.githubusercontent.com/54609399/138154296-4e0c8d01-6ae0-46b0-9232-41f1553f6b02.png)

a la derecha seleccionamos int64 sigifica que es tipo entero y de 64 bits osea mas optimo que el de 32 que es versiones viejas

![image](https://user-images.githubusercontent.com/54609399/138154364-495632f2-0fc8-42ef-bede-994230c9eb6e.png)

Para finalizar le damos inset y ya tendiramos un documento creado nuestro primer registro que es un JSON

![image](https://user-images.githubusercontent.com/54609399/138154419-f0fdb554-fb8e-4e51-8bcf-edd9d9e123a8.png)

![image](https://user-images.githubusercontent.com/54609399/138154478-7a7342e8-e1d3-4803-925a-aeb6392b6c34.png)

Podemos hacer lo que queramos con los documentos. editarlos o eliminarlos o copiarlos desde las siguientes opciones

![image](https://user-images.githubusercontent.com/54609399/138197536-7300fa22-80c9-4864-876a-8ef3e55fe116.png)


**** COMO HACER BACKUP DE BASES DE DATOS EN MONGODB POR CONSOLA ****

![image](https://user-images.githubusercontent.com/54609399/138027331-7f82b8f9-c8bb-4814-aeb4-76cc655e738e.png)

crear carpeta de backup y escribir comando mongodum

![image](https://user-images.githubusercontent.com/54609399/138027427-959ba81d-d158-478a-b878-d1eb5b036d17.png)

![image](https://user-images.githubusercontent.com/54609399/138027484-e2329083-a9e3-4357-b9cd-6931ef136e4c.png)

![image](https://user-images.githubusercontent.com/54609399/138027516-65879562-d6c2-476e-b219-41dd6a4ed83d.png)

8 - validamos que haya quedado

![image](https://user-images.githubusercontent.com/54609399/138027539-4d8d4f29-7ee4-4e8a-82fc-e762dc4fe6a4.png)

9 - ahora eliminamos de nuevo prueba db

![image](https://user-images.githubusercontent.com/54609399/138027600-9c1ce772-4882-41ae-8add-42740016cf60.png)

10 - y ahora restauramos solo esa bd

![image](https://user-images.githubusercontent.com/54609399/138027649-23d6861b-8a2d-496a-bbc1-932e55b21401.png)

11 - confirmamos

![image](https://user-images.githubusercontent.com/54609399/138027722-426d5531-2830-4eba-9906-2eb7081b0900.png)

12 - para una sola bd

![image](https://user-images.githubusercontent.com/54609399/138027745-556ee1cb-8ad8-4541-b29d-cd1f93443750.png)

![image](https://user-images.githubusercontent.com/54609399/138027755-14827f86-c7dd-4bef-acc6-7f6d495d2ccb.png)

13 - 13 - para colecciones

![image](https://user-images.githubusercontent.com/54609399/138027803-0ff3f832-8bd5-4daf-917d-99be3c8b2a71.png)

14 - restaurar

![image](https://user-images.githubusercontent.com/54609399/138027832-51b30a07-7285-4084-a3ea-0db6fb9053e1.png)

15 - 
