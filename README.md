# SQL_HW_1

![](https://www.datocms-assets.com/14946/1627286560-sql-databases.png?auto=format&fit=max&w=1200)

Исходная таблица в приложении. 

---------
 1. Вывести все поля и все строки.
 ```SQL
select * from students s;
```
 2. Вывести всех студентов в таблице (аналогично предыдущему запросу).
```SQL
select * from students s;
```
 3. Вывести только Id пользователей.
 ```SQL
select id from students s ;
```
 4. Вывести только имя пользователей.
 ```SQL
select name from students s;
```
 5. Вывести только email пользователей.
 ```SQL
select email from students s;
```
 6. Вывести имя и email пользователей.
 ```SQL
select name, email from students s;
```
 7. Вывести id, имя, email и дату создания пользователей.
 ```SQL
select id, name, email, created_on  from students s;
```
 8. Вывести пользователей где password 12333.
 ```SQL
select * from students s where password = '12333'; 
select * from students s where password like '12333'; 
```
 9. Вывести пользователей которые были созданы 2021-03-26 00:00:00.
 ```SQL
select * from students s where created_on = '2021-03-26 00:00:00';
select * from students s where created_on in ('2021-03-26 00:00:00');
```
 10. Вывести пользователей где в имени есть слово Анна.
 ```SQL
select * from students s where name like '%Anna%'; 
```
 11. Вывести пользователей где в имени в конце есть 8.
 ```SQL
select * from students s where name like '%8'; 
```
 12. Вывести пользователей где в имени в есть буква а.
 ```SQL
select * from students s where name like '%a%'; 
```
 13. Вывести пользователей которые были созданы 2021-07-12 00:00:00
 ```SQL
select * from students s where created_on = '2021-07-12 00:00:00'; 
select * from students s where created_on in ('2021-07-12 00:00:00'); 
```
 14. Вывести пользователей которые были созданы 2021-07-12 00:00:00 и имеют пароль 1m313.
 ```SQL
 select * from students s where created_on = '2021-07-12 00:00:00' and password  = '1m313';
 ```
 15. Вывести пользователей которые были созданы 2021-07-12 00:00:00 и у которых в имени есть слово Andrey.
 ```SQL
select * from students s where created_on = '2021-07-12 00:00:00' and name  like '%Andrey%';
```
 16. Вывести пользователей которые были созданы 2021-07-12 00:00:00 и у которых в имени есть цифра 8.
 ```SQL
select * from students s where created_on = '2021-07-12 00:00:00' and name  like '%8%';
```
 17. Вывести пользователя у которых id равен 110.
 ```SQL
select * from students s where id = 110;
```
 18. Вывести пользователя у которых id равен 153.
  ```SQL
select * from students s where id = 153;
```
 19. Вывести пользователя у которых id больше 140.
 ```SQL
select * from students s where id > 140;
```
 20. Вывести пользователя у которых id меньше 130.
  ```SQL
select * from students s where id < 130;
```
 21. Вывести пользователя у которых id меньше 127 или больше 188.
  ```SQL
select * from students s where id < 127 or id > 188;
select * from students s where id not between 127 and 188;
```
 22. Вывести пользователя у которых id меньше либо равно 137.
  ```SQL
select * from students s where id <= 137;
```
 23. Вывести пользователя у которых id больше либо равно 137.
  ```SQL
select * from students s where id >= 137;
```
 24. Вывести пользователя у которых id больше 180 но меньше 190.
  ```SQL
select * from students s where id > 180 and id < 190;
```
 25. Вывести пользователя у которых id между 180 и 190.
  ```SQL
select * from students s where id between  180 and 190;
```
 26. Вывести пользователей где password равен 12333, 1m313, 123313.
  ```SQL
select * from students s where password in ('12333', '1m313', '123313'); 
```
 27. Вывести пользователей где created_on равен 2020-10-03 00:00:00, 2021-05-19 00:00:00, 2021-03-26 00:00:00.
  ```SQL
select * from students s where created_on in ('2020-10-03 00:00:00', '2021-05-19 00:00:00', '2021-03-26 00:00:00'); 
```
 28. Вывести минимальный id.
  ```SQL
select min(id) from students;
```
 29. Вывести максимальный.
  ```SQL
select max(id) from students;
```
 30. Вывести количество пользователей.
  ```SQL
select count(id) from students;
```
 31. Вывести id пользователя, имя, дату создания пользователя. Отсортировать по порядку возрастания даты добавления пользователя.
  ```SQL
select id, name, created_on from students s order by created_on asc; 
```
 32. Вывести id пользователя, имя, дату создания пользователя. Отсортировать по порядку убывания даты добавления пользователя.
  ```SQL
select id, name, created_on from students s order by created_on desc;
``` 
-------

Таблица 


|id|name|email|password|created_on|
|--|----|-----|--------|----------|
|116|Thomas|Thomas@gmail.com|1fef4|2021-03-26 00:00:00.000|
|118|Michael|Michael@gmail.com|12333|2021-01-26 00:00:00.000|
|119|Elliott|Elliott@gmail.com|12333|2021-02-26 00:00:00.000|
|120|James|James@gmail.com|12333|2021-03-26 00:00:00.000|
|121|Steven|Steven@gmail.com|12333|2021-04-26 00:00:00.000|
|122|Anna_5|Anna_5@gmail.com|332f2|2021-05-26 00:00:00.000|
|123|Anna_6|Anna_6@gmail.com|332f2|2021-06-26 00:00:00.000|
|124|Anna_7|Anna_7@gmail.com|332f2|2021-07-26 00:00:00.000|
|125|Anna_8|Anna_8@gmail.com|332f2|2021-08-26 00:00:00.000|
|126|Anna_9|Anna_9@gmail.com|332f2|2021-09-26 00:00:00.000|
|127|8_Jermaine|8_Jermaine@gmail.com|332f2|2021-09-26 00:00:00.000|
|129|8_Mabel|8_Mabel@gmail.com|332f2|2021-09-26 00:00:00.000|
|131|8_Mary|8_Mary@gmail.com|ev42f2|2021-11-12 00:00:00.000|
|132|8_Yoshie|8_Yoshie@gmail.com|ev42f2|2021-12-12 00:00:00.000|
|133|8_Alice|8_Alice@gmail.com|ev44ff|2021-03-15 00:00:00.000|
|134|8_David|8_David@gmail.com|ev44ff|2021-04-15 00:00:00.000|
|135|8_Robert|8_Robert@gmail.com|ev44ff|2021-05-15 00:00:00.000|
|136|8_Stanley|8_Stanley@gmail.com|3ev44ff|2021-07-12 00:00:00.000|
|137|8_James|8_James@gmail.com|4ev44ff|2021-07-12 00:00:00.000|
|138|8_Patty|8_Patty@gmail.com|5ev44ff|2021-07-12 00:00:00.000|
|139|8_Jackson|8_Jackson@gmail.com|1ev44ff|2021-07-12 00:00:00.000|
|140|8_Frank|8_Frank@gmail.com|2ev44ff|2021-07-12 00:00:00.000|
|141|8_William|8_William@gmail.com|3ev44ff|2021-07-12 00:00:00.000|
|142|8_Norris|8_Norris@gmail.com|4ev44ff|2021-07-12 00:00:00.000|
|143|8_Earl|8_Earl@gmail.com|1m313|2021-07-12 00:00:00.000|
|146|8_Sylvia|8_Sylvia@gmail.com|1m313|2021-07-12 00:00:00.000|
|147|8_Kathleen|8_Kathleen@gmail.com|1m313|2021-07-12 00:00:00.000|
|148|8_Dallas|8_Dallas@gmail.com|1m313|2021-07-12 00:00:00.000|
|149|8_Tamera|8_Tamera@gmail.com|1m313|2021-07-12 00:00:00.000|
|150|Andrey_1|Andrey_1@gmail.com|1m313|2021-07-12 00:00:00.000|
|151|Andrey_2|Andrey_2@gmail.com|1m313|2021-07-12 00:00:00.000|
|152|Andrey_3|Andrey_3@gmail.com|1m313|2021-07-12 00:00:00.000|
|153|Andrey_4|Andrey_4@gmail.com|1m313|2021-07-12 00:00:00.000|
|154|Andrey_5|Andrey_5@gmail.com|1m313|2021-07-12 00:00:00.000|
|155|Andrey_6|Andrey_6@gmail.com|1m313|2021-07-12 00:00:00.000|
|156|Leticia_Long|Leticia_Long@gmail.com|123313|2021-07-12 00:00:00.000|
|157|Christopher_Kumro|Christopher_Kumro@gmail.com|123313|2021-07-12 00:00:00.000|
|158|Olive_Warne|Olive_Warne@gmail.com|123313|2021-07-12 00:00:00.000|
|159|Kenneth_Coleman|Kenneth_Coleman@gmail.com|123313|2021-07-12 00:00:00.000|
|160|William_Owen|William_Owen@gmail.com|123313|2021-07-12 00:00:00.000|
|161|Richard_Laflam|Richard_Laflam@gmail.com|4f4v3ff|2020-10-03 00:00:00.000|
|162|Bettye_Bevington|Bettye_Bevington@gmail.com|4f4v3ff|2020-10-03 00:00:00.000|
|163|Frida_Krieger|Frida_Krieger@gmail.com|4f4v3ff|2020-10-03 00:00:00.000|
|164|Rocky_Siddon|Rocky_Siddon@gmail.com|9vjj94v|2021-05-19 00:00:00.000|
|165|Veronica_Jones|Veronica_Jones@gmail.com|9vjj94v|2021-05-19 00:00:00.000|
|166|Michael_Carrano|Michael_Carrano@gmail.com|9vjj94v|2021-05-19 00:00:00.000|
|167|Joanne_Hubler|Joanne_Hubler@gmail.com|9vjj94v|2021-03-26 00:00:00.000|
|168|Thomas_Patel|Thomas_Patel@gmail.com|9vjj94v|2021-03-26 00:00:00.000|
|169|Angelina_Venezia|Angelina_Venezia@gmail.com|9vjj94v|2021-03-26 00:00:00.000|
|170|Albert_Madrigal|Albert_Madrigal@gmail.com|8vj1j91|2021-01-11 00:00:00.000|
|171|Alice_Garner|Alice_Garner@gmail.com|8vj2j92|2021-02-12 00:00:00.000|
|172|Shirley_Hartung|Shirley_Hartung@gmail.com|8vj3j93|2021-03-13 00:00:00.000|
|173|Derrick_Gary|Derrick_Gary@gmail.com|8vj4j94|2021-04-14 00:00:00.000|
|174|Pauline_Moody|Pauline_Moody@gmail.com|8vj5j95|2021-05-15 00:00:00.000|
|175|John_Perez|John_Perez@gmail.com|8vj6j96|2021-06-16 00:00:00.000|
|176|Philip_Wilde|Philip_Wilde@gmail.com|8vj7j97|2021-07-17 00:00:00.000|
|177|Debra_Holland|Debra_Holland@gmail.com|8vj8j98|2021-08-18 00:00:00.000|
|178|Amy_Mcmanus|Amy_Mcmanus_1@gmail.com|8vj1j91|2021-01-11 00:00:00.000|
|179|Karl_Storie|Karl_Storie_2@gmail.com|8vj2j92|2021-02-12 00:00:00.000|
|180|Christine_Ackland|Christine_Ackland_3@gmail.com|8vj3j93|2021-03-13 00:00:00.000|
|181|Joseph_Spradlin|Joseph_Spradlin_4@gmail.com|8vj4j94|2021-04-14 00:00:00.000|
|182|James_Bradford|James_Bradford_5@gmail.com|8vj5j95|2021-05-15 00:00:00.000|
|183|Sadie_Mcdougall|Sadie_Mcdougall_6@gmail.com|8vj6j96|2021-06-16 00:00:00.000|
|184|Gerald_Gross|Gerald_Gross_7@gmail.com|8vj7j97|2021-07-17 00:00:00.000|
|185|Frederick_Bumbrey|Frederick_Bumbrey_8@gmail.com|8vj8j98|2021-08-18 00:00:00.000|
|186|Abbey_Tracy|Abbey_Tracy_1@gmail.com|8vj1j91|2021-01-11 00:00:00.000|
|187|Bryan_Miller|Bryan_Miller_2@gmail.com|8vj2j92|2021-02-12 00:00:00.000|
|188|Anita_Frederick|Anita_Frederick_3@gmail.com|8vj3j93|2021-03-13 00:00:00.000|
|189|Ernest_Wood|Ernest_Wood_4@gmail.com|8vj4j94|2021-04-14 00:00:00.000|
|190|Mary_Tornow|Mary_Tornow_5@gmail.com|8vj5j95|2021-05-15 00:00:00.000|
|191|Marion_Daniel|Marion_Daniel_6@gmail.com|8vj6j96|2021-06-16 00:00:00.000|
|192|Carey_Biro|Carey_Biro_7@gmail.com|8vj7j97|2021-07-17 00:00:00.000|
|193|Brenda_Walstrum|Brenda_Walstrum_8@gmail.com|8vj8j98|2021-08-18 00:00:00.000|
|194|Jack_Stensrud|Jack_Stensrud_1@gmail.com|8vj1j91|2021-01-11 00:00:00.000|
|195|Dennis_Carr|Dennis_Carr_2@gmail.com|8vj2j92|2021-02-12 00:00:00.000|
|196|Jimmy_Robinson|Jimmy_Robinson_3@gmail.com|8vj3j93|2021-03-13 00:00:00.000|
|197|Randall_Strop|Randall_Strop_4@gmail.com|8vj4j94|2021-04-14 00:00:00.000|
|198|Steven_Melancon|Steven_Melancon_5@gmail.com|8vj5j95|2021-05-15 00:00:00.000|
|199|Donna_Mellish|Donna_Mellish_6@gmail.com|8vj6j96|2021-06-16 00:00:00.000|
|200|Scott_Beaty|Scott_Beaty_7@gmail.com|8vj7j97|2021-07-17 00:00:00.000|
|201|Enrique_Gibson|Enrique_Gibson_8@gmail.com|8vj8j98|2021-08-18 00:00:00.000|
|202|Stanley_Hickman|Stanley_Hickman_1@gmail.com|8vj1j91|2021-01-11 00:00:00.000|
|203|Gloria_Mercado|Gloria_Mercado_2@gmail.com|8vj2j92|2021-02-12 00:00:00.000|
|204|Michael_White|Michael_White_3@gmail.com|8vj3j93|2021-03-13 00:00:00.000|
|205|Milton_Russell|Milton_Russell_4@gmail.com|8vj4j94|2021-04-14 00:00:00.000|
|206|Tanya_Aki|Tanya_Aki_5@gmail.com|8vj5j95|2021-05-15 00:00:00.000|
|207|Dawn_Dwelle|Dawn_Dwelle_6@gmail.com|8vj6j96|2021-06-16 00:00:00.000|
|208|Rex_Wilson|Rex_Wilson_7@gmail.com|8vj7j97|2021-07-17 00:00:00.000|
|112|Vadim|Vadim@gmail.com|1fef4|2021-03-26 00:00:00.000|
|113|Pam|Pam@gmail.com|1fef4|2021-03-26 00:00:00.000|
|130|8_Jarred_9|8_Jarred@gmail.com|ev42f2|2021-10-12 00:00:00.000|
|115|Marlin|Marlin@gmail.com|1fef4|2021-03-26 00:00:00.000|
|128|8_Terence|8_Terence@gmail.com|332f2|2021-08-26 00:00:00.000|
|209|Donald_Hayner|Donald_Hayner_8@gmail.com|8vj8j98|2021-08-18 00:00:00.000|
|210|Elmer_Dixon|Elmer_Dixon_1@gmail.com|8vj1j91|2021-01-11 00:00:00.000|
|211|Steven_Horton|Steven_Horton_2@gmail.com|8vj2j92|2021-02-12 00:00:00.000|
|212|Fay_Akins|Fay_Akins_3@gmail.com|8vj3j93|2021-03-13 00:00:00.000|
|213|Jay_Biggs|Jay_Biggs_4@gmail.com|8vj4j94|2021-04-14 00:00:00.000|
|214|Marie_Casto|Marie_Casto_5@gmail.com|8vj5j95|2021-05-15 00:00:00.000|
|215|Kenneth_Jackson|Kenneth_Jackson_6@gmail.com|8vj6j96|2021-06-16 00:00:00.000|
|216|Sam_Williams|Sam_Williams_7@gmail.com|8vj7j97|2021-07-17 00:00:00.000|
|217|Virginia_Bruce|Virginia_Bruce_8@gmail.com|8vj8j98|2021-08-18 00:00:00.000|
|117|Josefina|Josefina@gmail.com|3332e|2021-03-26 00:00:00.000|
|218|Klim|klim@gmail.com|q23ref2|2022-02-18 20:06:50.045|
|219|vadim|vik@gmai.com|123456|2022-02-18 20:06:59.062|
|220|Vadim_32|Vadim_32@gmail.com|3ef23ef22|2022-02-18 20:07:10.485|
|222|vadim|vik123@gmai.com|123456|2022-02-18 20:09:56.783|
|224|viktor|vik12356@gmai.com|123456|2022-02-18 20:11:28.229|
|225|None|None|None|2022-02-18 20:13:18.663|
|226|Dima0|Dima@gmail.com0|Dima2e2efe2f0|2022-02-18 20:13:45.382|
|227|Dima1|Dima@gmail.com1|Dima2e2efe2f1|2022-02-18 20:13:45.540|
|228|Dima2|Dima@gmail.com2|Dima2e2efe2f2|2022-02-18 20:13:45.695|
|229|Dima3|Dima@gmail.com3|Dima2e2efe2f3|2022-02-18 20:13:45.849|
|230|viktor|vik12356@gmail.com|123456|2022-02-18 20:13:17.154|
|232|qw|wqw|qwqw|2022-02-18 20:42:47.742|
|233|Dima|Dima123@gmail.com|12jjsd4|2022-02-18 20:51:46.480|
|239|Artem|artem@mail.ru|321123|2022-02-18 22:47:20.308|
|241|Elena|efwwf@gwrg.wrg|12345678|2022-02-19 15:58:31.860|
|240|Artem1|artem1@mail.ru|321123|2022-02-18 23:41:39.930|
|242|Garret|aa@aaaaa.aa|1234445|2022-02-21 12:51:58.117|
|245|Garret|dasddnadbadada@gmail.com|1234445|2022-02-21 13:02:15.305|
|246|kek|kek@yahoo.com|qwqw|2022-02-22 18:38:40.822|
|247|Valentin|val@gmail.com|eee123|2022-02-22 19:50:28.516|
|253|Val|val123@gmail.com|qqq123|2022-02-22 20:04:57.527|
|254|Valik0|valik123@gmail.com|qqq|2022-02-22 20:17:27.099|
|257|PAvel|PAvel@test.com|123456|2022-03-01 16:07:13.840|
|259|PAvel|PAve1l@test.com|123456|2022-03-01 16:13:20.945|
|260|Dima_vaflya0|Dima_vaflya@test.com0|123456Dima_vaflya0|2022-03-01 16:32:59.984|
|261|Dima_vaflya1|Dima_vaflya@test.com1|123456Dima_vaflya1|2022-03-01 16:33:00.176|
|262|Dima_vaflya2|Dima_vaflya@test.com2|123456Dima_vaflya2|2022-03-01 16:33:00.359|
|263|Dima_vaflya3|Dima_vaflya@test.com3|123456Dima_vaflya3|2022-03-01 16:33:00.543|
|626|Sergey|gmail.com|2702|2022-10-18 00:00:00.000|
|627|Sergey H|gmail.comy|__|2022-10-18 00:00:00.000|
|628|Sergey|gmail.comt||2022-10-18 00:00:00.000|
