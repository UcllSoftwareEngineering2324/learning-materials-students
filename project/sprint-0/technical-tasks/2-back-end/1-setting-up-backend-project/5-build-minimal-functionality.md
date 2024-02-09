# Build minimal functionality

It is useful to let the application do _something_ before building deployment pipelines.

In this task we will build a simple HTTP endpoint that returns a greeting.

We can then use this endpoint to verify our deployment pipelines.

## 1. Acceptance Criteria

When calling `http://localhost:8080/hello` with an HTTP GET request, your application should return the following JSON:

```js
{
    "id": 1,
    "message": "Hello World!"
}
```

The returned Greeting should be retrieved from an H2 database.

## 2. Implementation Details

Below is a condensed flow to follow if you need a small refresher:
1. Add the following Spring Boot starter dependencies to your `pom.xml` file
    * `spring-boot-starter-web`
    * `spring-boot-starter-data-jpa`
1. Add the dependency for the H2 database to your `pom.xml` file
1. Add an Entity for the Greeting object
1. Add a Repository to be able to retrieve the Greeting object from the database
1. Add a Controller/Service to return the result from the Repository as an answer to the GET request
1. You can adapt the following code to insert a Greeting in the H2 database when your application starts:

    ```java
    @Component
    public class InitGreetings {

        @Autowired
        private GreetingRepository greetingRepository;

        @PostConstruct
        public void insertGreeting() {
            greetingRepository.save(new Greeting("Hello world"));
        }
    }
    ```