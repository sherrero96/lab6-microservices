# Lab6 - Microservices

First we started the Eureka service. 
Once the server is up, we start the web server and the account server. 
Once started, they register in Eureka.

![image 1](Img/1%20-%20TwoServices.png "Two micro up")

As you can see in the following image, both services are registered in Eureka:

![image 2](Img/2%20-%20Registro.png "Both services are registered")

Now we turn on a new account service on port 4444

![image 3](Img/3%20-%20AnotherMicro.png "New Account service")

Now let's kick the account service out of port 2222. 
As you can see in the image below, the account information service is still working.

![image 4](Img/4%20-%20StillWork.PNG "Still Working")

It continues to work because Eureka detects that the service on port 2222 is not working, 
but has a mirror on 4444 that can provide the same service. All this is made transparent to the user.


