Seed is a fully-managed-code pipeline for Serverless application. The front men of Seed Frank Wang and Jay V, and are backed by a very impressive board. Before we get to more on Seed, let us talk little about Serverless.

## Introducing PaaS, Serverless, and Lambda

With Heroku, Beanstalk and other PaaS solutions out there, we now find parts of application development (primarily APIs, micro-services) extremely quick and deployment and management much easier.

AWS has released a service called Lambda, whose concept is similar to running your application on the cloud (Heroku, Beanstalk, etc), although, Lambda would just expose “functions” that can be invoked. Think of it as just smaller pieces of code that are present on the cloud. It is not present on a particular server/machine but is compiled and executed whenever invoked, fundamentally meaning it can scale to any size, as concurrent invocations would bring up new instances.

Lambda, Serverless, Function-as-a-service is turning a lot of heads. There are a lot of experiments and products already in this space. Seed perfectly solves one problem, the “code-pipeline, and deployment”. What Heroku did for Ruby projects (especially Ruby on Rails) Seed brilliantly does for Serverless applications. They have built their product respecting all the features of Serverless, which we love, and have delivered a truly effective product for deploying applications.

We started using Serverless for one of the large projects and much to our luck, Jay just shot a mail to us introducing Seed and that is exactly what we needed, especially because deployments in Serverless are not the most convenient (more so when the project dependencies are not few).

When we tested their product, we immediately noticed the value of it. We were experimenting and using Seed while it was still in Beta and we had incredible personal support from Frank and Jay. We knew the product had value, but it was so new and still in Beta. However, after our interactions with Frank and Jay, we were certain we include Seed into our stack.

We are in love with Seed and the team! We wish Seed a lot of success and we are looking forward to seeing everything they will create.