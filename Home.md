This is the repository that we will use for the fifth assignment of the course 2015-2016. This repository has a [master](/UNIZAR-30246-WebEngineering/Laboratory-6-microservices/tree/master) and a [control](/UNIZAR-30246-WebEngineering/Laboratory-6-microservices/tree/control) branch. The master branch contains the code of the laboratory and the control branch only the list where you must register your results. 

The code is based on the post [Microservices with Spring](https://spring.io/blog/2015/07/14/microservices-with-spring) developed by [Paul Chapman](https://spring.io/team/pchapman). The laboratory shows a simple example of setting up a [microservices](http://martinfowler.com/articles/microservices.html) system using Spring, Spring Boot and Spring Cloud. The project contains three apps:
* Service Registration (`registration`): It launches an open source service registration server called [Eureka](https://github.com/Netflix/eureka) that will use the port 1111. The dashboard of the registration server is exposed in `http://localhost:1111p`
* Microservice account service (`accounts`): It is a standalone process that provides a RESTful server to a repository of accounts that will use the port 2222. What it makes special is that it registers itself to the registration service with the name `ACCOUNTS-SERVICE`. After launching this service you can see in the dashboard of the registration server that after a few seconds (10-20 secs) the  `ACCOUNTS-SERVICE` service appears.
* Microservice web service (`web`): It is a standalone process that provides a MVC front-end to the application of accounts that will use the port 3333. What it makes special is that it registers itself to the registration service with the name `WEB-SERVICE` and asks the registration service where is the `ACCOUNTS-SERVICE`. Spring configures automatically the class  `RestTemplate` for using the discovery service transparently!!!

This is a *NOT* a speed competition. The objective is to show by mean of evidences (screenshots) and a personal account that contains:
* The two microservices are running and registered (two terminals, logs screenshots).
* The service registration service has the two microservices registered (a third terminal, dashboard screenshots)
* A second account microservice is running in the port 4444 and it is registered (a fourth terminal, log screenshots).
* A brief report describing what happens when you kill the microservice with port 2222. Can the web service provide information about the accounts? Why?

This Lab will not use Travis for checks. 

In order to pass this lab you should:
- Fork this repository, and configure in a similar way as you did for lab 1
- Do the above procedures.
- _Master branch_: Modify [README.md](/UNIZAR-30246-WebEngineering/Laboratory-6-microservices/tree/master/README.md) so it contains the screenshots and the report. 
- _Control branch_: Update your corresponding row in [README.md](/UNIZAR-30246-WebEngineering/Laboratory-6-microservices/tree/control/README.md) with the link to your repo
- _Control branch_: Request a pull request only of your control branch

Ok, the above is easy to medium. Now, how to get the cumulative bonus of 5% in your personal score? It is obvious, improve the existing application by using the goodies provided by [Spring Cloud](http://projects.spring.io/spring-cloud/). Explore and propose ideas. 
- First, make a proposal by adding a proposal in your corresponding row in [README.md](/UNIZAR-30246-WebEngineering/Laboratory-6-microservices/tree/control/README.md). 
- Second, if nobody has requested previously the same improvement and I believe that it is worthwhile, I reserve the topic for you by accepting your pull request. Otherwise, I will reject it and will provide feedback.
- Third, start to work on it; remember that I will check if there are tests that test your improvement and your code pass Travis checks.
- Fourth, when you think it is ready add a :gift: to your corresponding row in [README.md](/UNIZAR-30246-WebEngineering/Laboratory-6-microservices/tree/control/README.md). Then do a pull request of your _Control branch_.
- Fifth, I will review your contribution. If it deserves the :gift: I will accept your pull request. Otherwise, I will reject it and will provide feedback.

 