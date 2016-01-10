# Web Engineering 2015-2016 / Microservices
Please, go to the [Wiki](https://github.com/UNIZAR-30246-WebEngineering/Laboratory-6-microservices/wiki) in order to get the instructions for this assignment.

## 1. The two microservices are running and registered

### 1.1. Accounts
![](https://raw.githubusercontent.com/marcosruiz/Laboratory-6-microservices/master/screenshots/1-1.png)

### 1.2. Web
![](https://github.com/marcosruiz/Laboratory-6-microservices/blob/master/screenshots/1-2.png?raw=true)

## 2. The service registration service has the two microservices registered
![](https://github.com/marcosruiz/Laboratory-6-microservices/blob/master/screenshots/2.png?raw=true)


## 3. A second account microservice is running in the port 4444 and it is registered
![](https://github.com/marcosruiz/Laboratory-6-microservices/blob/master/screenshots/3.png?raw=true)


## 4. A brief report describing what happens when you kill the microservice with port 2222. Can the web service provide information about the accounts? Why?

When you kill the microservice with port 2222, the second microservice will take over. We can check this because localhost:2222 is down, localhost:4444 is up and, in the registration server (localhost:1111), the applications ACCOUNTS-SERVICE and WEB-SERVICE are operating.

This is because the registration server knows when a microservice gets down, in this moment the registration server starts to use the microservice registered with the same name (ACCOUNTS-SERVICE) without no one takes notices of that.
