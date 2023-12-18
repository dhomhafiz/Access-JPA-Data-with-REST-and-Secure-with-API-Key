# Access-JPA-Data-with-REST-and-Secure-with-API-Key
Access JPA Data with REST and Secure with API Key
Learn from Spring.io:
Accessing JPA Data with REST
https://spring.io/guides/gs/accessing-data-rest/

Curl command:
to see the top level service:
$ curl http://localhost:8080

to see the people records (none at present):
$ curl http://localhost:8080/people

create a new Person:
$ curl -i -H "Content-Type:application/json" -d '{"firstName": "Frodo", "lastName": "Baggins"}' http://localhost:8080/people
$ curl http://localhost:8080/people/1

how to use the findByLastName query:
$ curl http://localhost:8080/people/search/findByLastName?name=Baggins

uses a PUT call:
$ curl -X PUT -H "Content-Type:application/json" -d '{"firstName": "Bilbo", "lastName": "Baggins"}' http://localhost:8080/people/1
$ curl http://localhost:8080/people/1

uses a PATCH call:
$ curl -X PATCH -H "Content-Type:application/json" -d '{"firstName": "Bilbo Jr."}' http://localhost:8080/people/1
$ curl http://localhost:8080/people/1

delete records:
$ curl -X DELETE http://localhost:8080/people/1
$ curl http://localhost:8080/people

Learn Securing with API Key:
Learned from https://www.baeldung.com/spring-boot-api-key-secret
Securing Spring Boot API With API Key and Secret

use Maven, you can run the application by using ./mvnw spring-boot:run
