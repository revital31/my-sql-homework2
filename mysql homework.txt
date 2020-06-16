//1.id של המשתמש  שהוא כמעט הכי זקן
//SELECT id FROM users WHERE id IN (SELECT MAX date_of_birth FROM users); 


//2.אנשים מתחום החינוך
//הפקודה

SELECT email FROM `my sql h.w`.users WHERE email LIKE '%edu';


//3.שמות האנשים שנולדו בשנת 2000
//הפקודה
SELECT first_name FROM  users WHERE date_of_birth='2000';

//4.ממוצע שנת הלידה של אנשים שמחזיקים טלפון המתחיל ב050
SELECT  AVG (date_of_birth) FROM  users WHERE phone LIKE '%050'; 

//5.

SELECT date_of_birth FROM  users
GROUP BY date_of_birth
ORDER BY count(id)
 DESC LIMIT 3 ; 