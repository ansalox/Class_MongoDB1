# Class_MongoDB

1 - Para ver todas las bases de datos que tenemos en MongoDB

```
show dbs
```
![image](https://user-images.githubusercontent.com/54609399/138028777-2c4971fe-679e-4cfb-8666-cba56611f2a7.png)

2 - Ver la DB actual en la que estamos posicionados

```
db
```

![image](https://user-images.githubusercontent.com/54609399/138027987-f4ca5f94-34de-409e-a709-d4ab6b87aaa8.png)

3 - Crear y/o usar una DB, y luego comprobamos si en verdad estamos ubicados en la DB con el comando db

```
use pruebadb
```

![image](https://user-images.githubusercontent.com/54609399/138027109-18967b6b-2b03-429b-9e1b-41c8c00b933d.png)

4 - La DB no se puede eliminar porque no existe aun, para que MongoDB la ponga existente se le debe crear una colección primero

```
db.dropDatabase()
```

![image](https://user-images.githubusercontent.com/54609399/138027141-7279b294-9cb6-4dad-aaf5-1ebac5e7fad7.png)

5 - Crear una colección en una DB, podemos ver las colecciones que tengamos con el comando show collections

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

6 - Eliminar coleccion

```
db.item.drop()
```

![image](https://user-images.githubusercontent.com/54609399/138027255-6fd7e6c0-9354-4d55-b68f-bccebd0f86a5.png)

7 - Eliminar correctamente una DB, ahora que la DB ya tiene colecciones podemos eliminarla

```
db.dropDatabase()
```

![image](https://user-images.githubusercontent.com/54609399/138030580-2eebbf1e-816a-467b-9e6d-174fcd6a1569.png)

8 - Cambiar nombre de una colección (Para este paso necesitamos crear otra vez pruebadb y sus colecciones user e item)

```
db.["user"].renameCollection("userapp")
```

![image](https://user-images.githubusercontent.com/54609399/138027304-7f7112b8-10a6-4be8-8b44-53329a03e1b4.png)

![image](https://user-images.githubusercontent.com/54609399/138027331-7f82b8f9-c8bb-4814-aeb4-76cc655e738e.png)

**** COMO HACER BACKUP DE BASES DE DATOS EN MONGODB ****

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
