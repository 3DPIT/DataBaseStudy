# SQL



SELECT : 선택한 '컬럼'을 보여줘

FROM  :  특정 '테이블'에서

WHERE :  '조건'에 해당하는



#### SELECT 문과 FROM 사용

영화(film) 테이블에는 어떤 데이터(컬럼)들이 있는지 확인하기

```mysql
/* 영화 테이블에 있는 컬럼을 모두 보고 싶은경우*/
SELECT * FROM film;
```

![image-20200605170940175](SQL.assets/image-20200605170940175.png)



#### 특정 컬럼만 보고 싶을때

```mysql
/* 특정 컬럼만 보고 싶을 떄 */

SELECT film_id, title, rating, special_features
FROM film;
```

![image-20200605171611507](SQL.assets/image-20200605171611507.png)



#### 등급이 R인 영화만 따로 보고 싶은경우

``` mysql
/* 등급이 R인 영화만 따로 보고 싶다면? */

SELECT film_id, title, rating, special_features
FROM film
WHERE rating = 'R';
```

![image-20200605171756713](SQL.assets/image-20200605171756713.png)



#### 전체 영화 목록 중에서 대여 기간이 3일인 영화의 번호, 제목, 대여료, 대여기간  출력



```mysql
/* 전체 영화 목록 중에서 대여 기간이 3일인 
영화의 번호, 제목, 대여료, 대여기간  출력
 */

SELECT film_id, title, rental_rate, rental_duration
FROM film
WHERE rental_duration = 3;
```

![image-20200605172158631](SQL.assets/image-20200605172158631.png)