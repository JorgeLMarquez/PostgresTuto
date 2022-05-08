# Mini tutorial de SQL 

Hola, esta es una pequeña guía de como usar Postgresql. 

# Instalación de Postgresql

1. Descarga e instala el motor de base de datos relacional PostgreSQL en tu Sistema Operativo: [download](https://www.postgresql.org/download/)
2. Ten en cuenta que esto puede variar según tu SO. (En este caso uso ubuntu, comando para la instalación: `sudo apt install postgresql`)
![image](https://github.com/JorgeLMarquez/PostgresTuto/blob/main/PostgresTuto/1.png)

4. Entra a la línea de comando de tu postgresql (Busca poder usar el comando `psql` en tu terminal).
```
$ sudo -i -u postgres
# psql
```
![image](https://github.com/JorgeLMarquez/PostgresTuto/blob/main/PostgresTuto/3.png)

6. Tendrás que hacer login del usuario que creaste en tu instalación.
8. Una vez después del login, ejecuta el comando `\l` para ver todas las bases de datos locales.
![image](https://github.com/JorgeLMarquez/PostgresTuto/blob/main/PostgresTuto/4.png)

10. Crea tu primera base de datos: `create database launchx_nodejs;` (no olvides el punto y coma al final)
![image](https://github.com/JorgeLMarquez/PostgresTuto/blob/main/PostgresTuto/5.png)

12. Seleciona la base de datos creada: `\c launchx_nodejs;`
![image](https://github.com/JorgeLMarquez/PostgresTuto/blob/main/PostgresTuto/6.png)

14. Lista las tablas creadas: `\dt`
![image](https://github.com/JorgeLMarquez/PostgresTuto/blob/main/PostgresTuto/7.png)

16. Crea una nueva tabla: `CREATE TABLE explorers(id bigserial, username varchar(50));`
![image](https://github.com/JorgeLMarquez/PostgresTuto/blob/main/PostgresTuto/8.png)

18. Vuelve a listar las tablas creadas, deberías poder ver la tabla `explorers`.
![image](https://github.com/JorgeLMarquez/PostgresTuto/blob/main/PostgresTuto/9.png)

11. Agrega un nuevo registro a la tabla creada anteriormente:

```sql
insert into explorers(id, username) values (1, 'Explorer1');
```
![image](https://github.com/JorgeLMarquez/PostgresTuto/blob/main/PostgresTuto/10.png)

12. Agrega 5 registros más siguiendo el ejemplo anterior:
```sql
insert into explorers(id, username) values (1, 'Explorer1');
insert into explorers(id, username) values (2, 'Explorer2');
insert into explorers(id, username) values (3, 'Explorer3');
insert into explorers(id, username) values (4, 'Explorer4');
insert into explorers(id, username) values (5, 'Explorer5');
```
![image](https://github.com/JorgeLMarquez/PostgresTuto/blob/main/PostgresTuto/11.png)

13. Lee los registros de la tabla explorers: `select * from explorers;`
![image](https://github.com/JorgeLMarquez/PostgresTuto/blob/main/PostgresTuto/12.png)

15. Lee solo los nombres de todos los registros de la db: `select e.username from explorers e;`
![image](https://github.com/JorgeLMarquez/PostgresTuto/blob/main/PostgresTuto/13.png)

17. Actualiza el valor del primer nombre del explorer con ID 1: `update explorers e set username = 'Explorer 1 Upd' where e.id = 1;`
![image](https://github.com/JorgeLMarquez/PostgresTuto/blob/main/PostgresTuto/14.png)

19. Elimina el explorer con ID 1: `delete from explorers e where e.id = 1;`
![image](https://github.com/JorgeLMarquez/PostgresTuto/blob/main/PostgresTuto/15.png)

20. Vemos si se realizaron 
![image](https://github.com/JorgeLMarquez/PostgresTuto/blob/main/PostgresTuto/16.png)

21. Salimos
![image](https://github.com/JorgeLMarquez/PostgresTuto/blob/main/PostgresTuto/17.png)

Objetivos de esta práctica:
- Instalar Postgresql
- Usar la línea de comando de Postgresql
- Crear un db desde la terminal
- Crear un tabla desde la terminal
- Aprender a realizar las operaciones básicas: crear, actualizar, leer y eliminar.

El uso de SQL en el día a día es vital, por lo que cualquier curso completo que puedas tomar solo te dará mejores habilidades para complementar tu formación como developer. Te recomiendo mucho buscar cursos y tutoriales sobre este tema, puedes invertir en el siguiente gran libro: https://www.practicalsql.com/index.html


# Editor de SQL

Te recomiendo mucho utilizar algún editor de SQL que te ayudará a realizar SQL de una forma más práctica que en la terminal:
- https://www.practicalsql.com/index.html
- https://www.pgadmin.org/download/
- https://eggerapps.at/postico/
- https://popsql.com/

