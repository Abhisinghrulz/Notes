<h1>Monolith</h1>

Its like big container wherein all the software components of an application are assembled together and 
tightly coupled.

Issues with it:
* Agility : In case of adding new services, you need to change whole architecture of the platform. 
* Scalability
* Fault Tolerance : In case of something is down, whole system is down
* Single Framework

<h1>MicroServices Architecture</h1>

* Monolith application is decomposed to different component.
* Different services for different component & interact with each other through Restful.
* Microservices : one for search, other for notification ,index, etc.
* Each have their LB, cache, indexes, REST api
* Benefits :
    - Single capabilities
    - Independent as Product
    - Decoupling
    - Continuous Delivery
    - Componentization
    - Autonomy
    - Scalability
    
Best Practices :
* Separate Data Stores
* Separate as per feature
* Server which are stateless    
