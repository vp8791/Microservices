1) Start Book Store
Murali@DESKTOP-SLU6JHH MINGW64 /c/github/MicroServices/circuitbreaker/gs-circuit-breaker/complete/bookstore/target (master)
$ java -jar bookstore-0.0.1-SNAPSHOT.jar

2) Start Book Reading Store
Murali@DESKTOP-SLU6JHH MINGW64 /c/github/MicroServices/circuitbreaker/gs-circuit-breaker/complete/reading/target (master)
$ java -jar reading-0.0.1-SNAPSHOT.jar


3) Execute Read from URI:

http://localhost:8080/to-read
Gets following output:

Spring in Action (Manning), Cloud Native Java (O'Reilly), Learning Spring Boot (Packt)


4) Take down Book Service:

Murali@DESKTOP-SLU6JHH MINGW64 /c/github/MicroServices/circuitbreaker/gs-circuit-breaker/complete/bookstore/target (master)

Stop

5) Execute Read from URI(Same as 3):

http://localhost:8080/to-read
Gets following output(Goes back to fall back indicating service is down):

Cloud Native Java (O'Reilly) 

https://spring.io/guides/gs/circuit-breaker/