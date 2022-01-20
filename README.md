# <span style="color: RED"> CI</span><span style="color: ORANGE">NE</span><span style="color: RED">MA</span> - <span style="color: orange">APP</span>
____
This is the quite helpful app that simulates a simple workflow of the cinema(movie) service. It allows you to register as user or admin and simply manage your account. 
With that app you can track what movie sessions are available, make and complete orders(buy tickets, adding to your shopping cats) and so on. 


![cinema pict](https://mmr.ua/wp-content/uploads/2021/05/mgm-studios-1200x580.jpg)
____

###  <span style="color: RED">How</span><span style="color: black"> to</span><span style="color: orange"> run: </span>
1. First you'll need to connect to your database(MySQL) using db.properties file in resources package.
2. Then configure [Tomcat](https://tomcat.apache.org/) local server. 
3. There is implemented DataInitializer class, so you already have login `admin@123` and password `admin123`, so you don't need to be registered through POSTMAN to have access to
the service. Some services(endpoints) are allowed only for those who has role ADMIN, and some for those who is User, in our case we'll have both.
4. To test all the links and services, you should use download [POSTMAN](https://www.postman.com/), using it, is much easier to test the service.

___
#### <span style="color:ORANGE">Endpoints</span>
1. POST: `/register` `/login` - allowed for everyone.
2. POST: `/orders/complete` - allowed for role `USER`.
3. POST: `/cinema-halls, /movies, /movie-sessions`- allowed for role `ADMIN`.
4. PUT: `/shopping-carts/movie-sessions` - allowed for role `USER`.
5. PUT: `/movie-sessions/**` - allowed for role `ADMIN`.
6. DELETE: `/movie-sessions/**` - allowed for role `ADMIN`.
7. GET: `/shopping-carts/by-user`, `/orders` - allowed for role `USER`.
8. GET:`/users/by-email` - allowed for role `ADMIN`.
9. GET: `/cinema-halls`, `/movies`, `/movie-sessions/available`, - allowed for roles `ADMIN` and `USER`.
___
#### <span style="color:ORANGE"> PROJECT</span><span style="color:RED"> STRUCTURE:</span>
In general, we used 3-tier architecture which include:
1. `Controllers (Presentation tier)`
2. `Services (Application logic tier)`
3. `DAO (Data tier)`
___
#### <span style="color:Red"> Technologies</span><span style="color:ORANGE"> used:</span> 
1. [Java](https://www.java.com/ru/)
2. [Spring framework](https://spring.io/)
3. [Hibernate framework](https://hibernate.org/)
4. [MySql](https://www.mysql.com/)
5. Rest principles
6. [Maven](https://maven.apache.org/)
7. [Tomcat](https://tomcat.apache.org/)

# <span style="color:Red">E</span><span style="color:purple">N</span><span style="color:orange">J</span><span style="color:green">O</span><span style="color:blue">Y</span><span style="color:black">:)</span>



