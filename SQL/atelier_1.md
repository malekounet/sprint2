3.

use atelier_1;
select name from  products;
============================
4.

use atelier_1;
select name, price from  products;
============================
5.

use atelier_1;
select name from  products where price<=200;
============================
6.

use atelier_1;
select name from  products where price<=120 AND price>60;
============================
7.

use atelier_1;
select name, price*100 as 'price in cent' from  products;
============================
8.

use atelier_1;
select avg(price) from  products;
===========================
9.

use atelier_1;
select AVG(price) from  products WHERE Manufacturer=2;
===========================
10.

use atelier_1;
select COUNT(*) from  products WHERE price>=180;
===========================
11.

use atelier_1;
select name, price from  products WHERE price>=180 ORDER BY price DESC, name ASC;
==========================
12.

USE atelier_1;
SELECT * FROM manufacturers m INNER JOIN products p ON m.Code=p.Manufacturer;
==========================
13.

USE atelier_1;
SELECT manufacturers.name, price,products.Name FROM manufacturers INNER JOIN products  ON manufacturers.Code=products.Manufacturer;
==========================
14.

USE atelier_1;
SELECT manufacturers.Code, AVG(price) FROM manufacturers INNER JOIN products  ON manufacturers.Code=products.Manufacturer
GROUP BY manufacturers.Name;
==========================
15.

USE atelier_1;
SELECT manufacturers.Name, AVG(price) FROM manufacturers INNER JOIN products  ON manufacturers.Code=products.Manufacturer
GROUP BY manufacturers.Name;
==========================
16.

USE atelier_1;
SELECT manufacturers.Name FROM manufacturers INNER JOIN products  ON manufacturers.Code=products.Manufacturer
GROUP BY manufacturers.Name HAVING AVG(price)>=150;
==========================
17.

USE atelier_1;
SELECT Name, price FROM products ORDER BY price ASC LIMIT 1;
==========================
18.

USE atelier_1;
SELECT manufacturers.Name, products.Name,MAX(price) FROM products INNER JOIN manufacturers on manufacturers.Code=products.Manufacturer GROUP BY manufacturers.Name;
==========================
19.

USE atelier_1;
INSERT INTO products (Name,Price ,Manufacturer )VALUES('Loudspeakers', 70, 2);
==========================










































