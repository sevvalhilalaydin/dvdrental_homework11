Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.


actor ve customer tablolarında bulunan first_name sütunları için tüm verileri sıralayalım.
actor ve customer tablolarında bulunan first_name sütunları için kesişen verileri sıralayalım.
actor ve customer tablolarında bulunan first_name sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım.
İlk 3 sorguyu tekrar eden veriler için de yapalım.



--1.SORU--
(SELECT first_name FROM actor
ORDER BY first_name)
UNION
(SELECT first_name FROM customer
ORDER BY first_name);

--2.SORU--
(SELECT first_name FROM actor
ORDER BY first_name)
INTERSECT
(SELECT first_name FROM customer
ORDER BY first_name);

--3.SORU--
(SELECT first_name FROM actor
ORDER BY first_name)
EXCEPT
(SELECT first_name FROM customer
ORDER BY first_name);
