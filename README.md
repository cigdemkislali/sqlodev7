# sqlodev7
sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

1-)film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.
select rating from film GROUP BY rating;
2-)film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.
select replacement_cost , COUNT() from film GROUP BY replacement_cost HAVİNG COUNT() > 50;
3-)customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir? 
select store_id ,COUNT (*) from customer GROUP BY store_id;
4-) city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.
select country_id, COUNT(*) from city GROUP BY country_id ORDER BY COUNT(country_id) DESC LIMIT 1;
