![Alt Text](https://montykamath.files.wordpress.com/2018/02/graphql.png?w=300&h=300)


GraphQL is a query language for APIs and a runtime for fulfilling those queries with your existing data. GraphQL provides a complete and understandable description of the data in your API, gives clients the power to ask for exactly what they need and nothing more, makes it easier to evolve APIs over time, and enables powerful developer tools.

* https://facebook.github.io/graphql/October2016/
* https://graphql.org/
* https://github.com/facebook/graphql
* https://github.com/graphql

------------------------------------------------------

* https://www.robinwieruch.de/getting-started-github-graphql-api/
* https://graphql.org/learn/

------------------------------------------------------
### Problem with Rest

Each resource in REST usually has an endpoint. For example, when writing a blog application, you may have an /article endpoint to fetch the information of the article, a /profile endpoint to fetch the information of the user profile and perhaps even a /comments endpoint to retrieve the comments for a given article.

The issue is that, when you’re retrieving the articles to show a list of articles, you need different data compared to when you’re retrieving the full blown article with all of its details. This leads to a lot of overfetching, considering that you’ll fetch too much data to build the article overview page if you use the same endpoints to handle both the article overview and the article detail page.

### Traffic flow when using REST APIs

A possible solution is to provide less information when someone calls /api/article compared to when someone is calling /api/article/123. This might solve the issue, but what if you want to write your application for both mobile devices and web browsers? Your mobile application might need even less data, so you could still be overfetching. A possible solution to this problem is to have multiple endpoints, for example /api/article/mobile and /api/article/desktop. This however, leads to a much higher coupling between the view and the REST APIs.

- from g00glen00b

-----------------------------------------------------------

### GraphQL vs Rest

* https://blog.goodapi.co/rest-vs-graphql-a-critical-review-5f77392658e7
* https://philsturgeon.uk/api/2017/01/24/graphql-vs-rest-overview/
* https://medium.com/codingthesmartway-com-blog/rest-vs-graphql-418eac2e3083
* https://dev.to/sadarshannaiynar/graphql-or-rest-what-should-i-use-38mj
* https://jaxenter.com/graphql-good-no-alternative-rest-services-142814.html
* https://www.quora.com/Is-GraphQL-a-REST-killer
* https://github.com/luisw19/graphql-samples
* https://github.com/ameizi/graphql-example
* https://github.com/gregwhitaker/springboot-graphql-example
* https://github.com/npalm/graphql-java-demo
* https://github.com/vladimir-dejanovic/graphql-spring-boot-example
* https://github.com/vaquarkhan/microservices-with-graphq-springboot


### POC

#### Scenario 1: 

- Imagine that the you have region "Account" with big list of account information .
- If the user A want filter based on business rues 
- If the user B want  records excepts some  extra filter on top of A 
- if the user C want all records.

You have created parent service which fetching all records based on conditions and child service going to hit parent service and return filter results ... look like plan :)

Now because of some bug fix you need to change the schema  or data type of some service, it will be synced, other services that relies in the old format will break. You can minimize this problem by writing a giant integration test that runs after changes on each component, but a change in one service should not impact other service (Anti pattern in microservice ).

                                                    or 

Create 3 diffrent microservice with almost same query that returns the  three similar account list then filter and use it.



#### Scenario 2: 

### POC:  GraphQL API With Java,Spring Boot,HQL




Starting soon..
