##1.- The two microservices are running and registered
### Account Microservice
![Account Microservice running and registered](https://raw.github.com/Santi-7/Laboratory-6-microservices/master/First Account.png)
### WebService Microservice
![WebService Microservice running and registered](https://raw.github.com/Santi-7/Laboratory-6-microservices/master/Web.png)

##2.- The service registration service has the two microservices registered
![Dashboard showing registered services](https://raw.github.com/Santi-7/Laboratory-6-microservices/master/Dashboard.png)

##3.- A second account microservice is running in the port 4444 and it is registered
![Account Microservice running on port 4444](https://raw.github.com/Santi-7/Laboratory-6-microservices/master/Second Account.png)

##4.- A brief report describing what happens when you kill the microservice with port 2222
When the Account Microservice on port 2222 is killed and the WebService Microservice on port 3333 tries to communicate with it, it obviously fails with a "Refused connection" error, because it doesn't know that the microservice isn't working. Right after, it asks the Registration Service on port 1111 for another microservice that provides the Account microservice, which answers with the Account microservice on port 4444. Then it starts working again.
