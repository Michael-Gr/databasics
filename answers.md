## Example:
1.
 - `SQL:`
    SELECT count(\*) from items

 - `ANSWER:`
   100

---

1.
 - `SQL:` select count(users.id) from users

 - `ANSWER:` 50


2.
 - `SQL:` select title from items order by price DESC limit 5

 - `ANSWER:` Small Cotton Gloves
             Small Wooden Computer
             Awesome Granite Pants
             Sleek Wooden Hat
             Ergonomic Steel Car

3.
 - `SQL:` select title from items where category = 'Books' order by price limit 1

 - `ANSWER:` Ergonomic Granite Chair

4.
 - `SQL:` select users.first_name, users.last_name from users, addresses where users.id = addresses.user_id and addresses.street = '6439 Zetta Hills'

 - `ANSWER:` first_name   | last_name
             -------------+----------
             Corrine      | Little   

5.
 - `SQL:` update addresses set city = 'New York', zip = '10108' from users where users.id = addresses.user_id and users.first_name = 'Virginie' and users.last_name = 'Mitchell'

 - `ANSWER:` UPDATE 1

6.
 - `SQL:` select sum(items.price) from items where items.category = 'Tools'

 - `ANSWER:` 7383

7.
 - `SQL:` select sum(orders.quantity) from orders

 - `ANSWER:` 2125

8.
 - `SQL:` select sum(orders.quantity * items.price) from orders, items where orders.item_id = items.id and items.category = 'Books';

 - `ANSWER:` 420566

9.
 - `SQL:` insert into users values(51, 'Michael', 'Gr', 'me@email.com');
          insert into orders values(378, 51, 13, 1, '2015-02-09 00:40:31.307668');

 - `ANSWER:` INSERT 0 1
             INSERT 0 1
