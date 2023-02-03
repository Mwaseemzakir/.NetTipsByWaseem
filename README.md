# Table of Content

**Episode 1 : What is .AsNoTracking() and its benefits**

**Episode 2 : SingleAsync and FirstAsync Methods of LINQ in .NET**

**Episode 3 : Basic overview of Monolithic and Microservices applications**

**Episode 4 : Difference b/w Boxing and Unboxing in C#**

**Episode 5 : Benefit of using AsReadOnly Method of List<T> in .NET**

**Episode 6 : Difference b/w Any and All Method for Collection in .NET**

**Episode 7 : Lazy Loading vs Eager Loading in EntityFramework**

**Episode 8 : Aggregate function over List<T> by Default Provided**

**Episode 9 : Difference b/w Include and ThenInclude in Entity Framework**

**Episode 10 : Use ToQueryString() Extension method while debugging**

**Episode 11 : How to avoid DbContext threading issues in Entity Framework**

**Episode 12 : How to register Open Generics in .NET Core Dependency Injection**

**Episode 13 : What are CORS and how to enable them in .NET at API Level**

**Episode 14 : Common Middlewares in .NET API**

**Episode 15 : Response Compression in .NET Core and how to configure its middleware**

**Episode 16 : Count() vs TryGetNonEnumeratedCount() and Which one is better ?**

**Episode 17 : Everything about Rate Limiting in .NET**

**Episode 18 : A basic visit to Response Caching along with its implementation in .NET**

**Episode 19 : Do you know how to initialize an Empty Enumerable in .NET ?**

**Episode 20 : Dependency Injection Explained in .NET**

**Episode 21 : IEnumerable vs IQueryable in .NET**

**Episode 22 : Why is it generally considered good practice to keep Dependency Injections in seperate class !**

**Episode 23 : Difference b/w GetType() and typeOf() Methods in .NET**

**Episode 24 : Difference b/w VAR and DYNAMIC keyword in C#**

**Episode 25 : StringBuilder vs string in C#**

**Episode 26 : Arrays vs ArrayList in C#**

**Episode 27 : Extension Methods in C#**

**Episode 28 : Common design principles you should keep in mind while developing applications**
 
**Episode 29 : Sealed keyword in C#**

**Episode 30 : String Interpolation vs Verbitam Identifier vs Raw String Literal**

**Episode 31 : Pad Left and Pad Right Method of String in C#**

**Episode 32 : How to read values from appsetting.json through IOptions and apply validation on it**

**Episode 33 : How to add DbContext Dependency Injection in .NET Core API ?**

-------------------------------------------------------------------------------------------------------------------------

# **Episode 1 : What is .AsNoTracking() and its benefits**

   𝐖𝐡𝐢𝐥𝐞 𝐮𝐬𝐢𝐧𝐠 𝐀𝐬𝐍𝐨𝐓𝐫𝐚𝐜𝐤𝐢𝐧𝐠
 
  1. The entity is not tracked by the context.
 
  2. EF does not know the state of its entity.
 
  3. Not recommended when you are performing Add/Update/Delete kind operations
 
  4. Improved performance over regular LINQ queries.
 
  5. Only recommended when you are doing read-only operations.
 
  6. Most efficient when we have to retrieve large set of data.
    
   𝐖𝐢𝐭𝐡𝐨𝐮𝐭 𝐀𝐬𝐍𝐨𝐓𝐫𝐚𝐜𝐤𝐢𝐧𝐠
 
  1. The entity is tracked by the context.
 
  2. EF knows the state of this entity.
 
  3. We can use this entity to save/update and we don't need to set the state of entity again.


![1](https://user-images.githubusercontent.com/44539744/214570292-85ababe2-8126-4c42-83da-04a293c7c7bf.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 2 : SingleAsync and FirstAsync Methods of LINQ in .NET**

1. In .NET, SingleAsync and FirstAsync are methods that can be used to retrieve a single element from a collection of elements.
2. Both methods are similar in that they return the first element in a collection that satisfies a specified condition.
3. The main difference between SingleAsync and FirstAsync is that SingleAsync will throw an exception if there is more than one element in the collection that satisfies the specified condition, while FirstAsync will return the first element it finds and then stop.
4. SingleAsync can be used to ensure that there is exactly one element in the collection that satisfies the condition, while FirstAsync can be used to simply retrieve the first element that satisfies the condition, regardless of how many elements in the collection satisfy the condition.

![2](https://user-images.githubusercontent.com/44539744/214570781-9d81668d-fd7c-4aca-a8b8-c5ac8403fe37.png)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 3 : Basic overview of Monolithic and Microservices applications**

Lets see the difference b/w monolithic and microservices 

𝐌𝐨𝐧𝐨𝐥𝐢𝐭𝐡𝐢𝐜:
1. A monolithic application is a single, self-contained program that consists of a single codebase.
2. It is typically built and deployed as a single unit
3. It tends to be more tightly coupled
4. It can be more brittle, since a failure in one part of the application can affect the entire system

𝐌𝐢𝐜𝐫𝐨𝐬𝐞𝐫𝐯𝐢𝐜𝐞𝐬:
1. A microservices application is a collection of small, independent services that communicate with each other to form a complete application.
2. It is built as a set of independent services that are deployed and managed separately
3. It is flexible and scalable as individual services can be updated and deployed without affecting the entire application.
4. It tends to be loosely coupled.
5. These applications can be more complex to build and manage, since they require coordination among multiple services.
6. They can also be more expensive to run, since each service needs to be individually managed and scaled.

![3](https://user-images.githubusercontent.com/44539744/214571188-e49795bb-3653-4e3c-bbad-d3dad76218c5.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 4 : Difference b/w Boxing and Unboxing in C#**

𝐁𝐨𝐱𝐢𝐧𝐠 and 𝐔𝐧𝐛𝐨𝐱𝐢𝐧𝐠 are used to convert value types to reference types and vice versa.
When value type is moved to a reference type it’s called as 𝐁𝐨𝐱𝐢𝐧𝐠 . 
The vice-versa is termed as 𝐔𝐧𝐛𝐨𝐱𝐢𝐧𝐠.

![4](https://user-images.githubusercontent.com/44539744/214574984-028acec4-6687-4060-810a-bd665f4e6c87.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 5 : Benefit of using AsReadOnly Method of List<T> in .NET**

Here are some benefits of 𝐀𝐬𝐑𝐞𝐚𝐝𝐎𝐧𝐥𝐲 Method of 𝐋𝐢𝐬𝐭<𝐓>
1. It gives you read only view of your collection.
2. It allows you to prevent the collection from being modified, either accidentally or intentionally
3. It can improve the performance of your code in some cases because the read-only wrapper provides a more restricted view of the collection.
4. This can be particularly beneficial when working with large collections, where even small performance improvements can make a significant difference.

![5](https://user-images.githubusercontent.com/44539744/214575801-06ee0b84-89b9-4607-b48e-65733f92acea.PNG)


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 6 : Difference b/w Any and All Method for Collection in .NET**
   
𝐀𝐧𝐲 𝐯𝐬 𝐀𝐥𝐥 𝐄𝐱𝐭𝐞𝐧𝐬𝐢𝐨𝐧 𝐌𝐞𝐭𝐡𝐨𝐝 𝐨𝐟 𝐋𝐢𝐬𝐭<𝐓>
   
1.The 𝐀𝐥𝐥 method checks if all elements of a list satisfy a specified condition.
   
2.The 𝐀𝐧𝐲 method checks if any elements of a list satisfy a specified condition.

   ![6](https://user-images.githubusercontent.com/44539744/214576987-08fca7a8-531d-4a29-94d4-799d9050566d.PNG)
   
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 7 : Lazy Loading vs Eager Loading in EntityFramework**

𝐋𝐚𝐳𝐲 𝐋𝐨𝐚𝐝𝐢𝐧𝐠 (𝐋𝐋)
1. Lazy Loading is a process where EF loads the related entities on demand.

2. It is the default behavior of EF

3. It delays the loading of related entities until you specifically request it.

4. You can go with it when you are sure that you are not using the related entities Instantly.

5. The number of round trips to the database is more as for each master entity data, it will issue a separate SQL query to get the child-related entity data.

6. It simply uses the SELECT Statement without any join.

7. If you are not interested in related entities or the related entities are not used instantly, then you can use it.

𝐄𝐚𝐠𝐞𝐫 𝐋𝐨𝐚𝐝𝐢𝐧𝐠 (𝐄𝐋)
1. Eager loading is a Process where EF loads the related entities along with the main entity

2. EF will not execute separate SQL queries for loading the related entities.

3. All the entities are loaded from the database with a single query saving bandwidth and server CPU time.

4. You can go with EL when you are sure that you will be using the related entities with the main entity everywhere

5. It is a good practice to reduce the number of SQL queries to be sent to the database server to fetch the related entities

6. It will use SQL Joining to join the related tables with the main table and then return the Main entity data along with the related entities.

7. If you are interested in related entities used instantly in your application, then you need to go with it.

𝐍𝐨𝐭𝐞 : If you want to check the 𝐒𝐐𝐋 𝐆𝐞𝐧𝐞𝐫𝐚𝐭𝐞𝐝 𝐐𝐮𝐞𝐫𝐲 when a LINQ query executes then you can check it by clicking on 𝐓𝐨𝐨𝐥𝐬 -> 𝐒𝐐𝐋 𝐒𝐞𝐫𝐯𝐞𝐫 𝐏𝐫𝐨𝐟𝐢𝐥𝐞𝐫 in SQL Server Management Studio.

![7](https://user-images.githubusercontent.com/44539744/214578049-6bb6cdea-5dff-40be-927d-fd04a9ceef5e.PNG)
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 8 : Aggregate function over List<T> by Default Provided**

You would be familiar with aggregate functions from SQL, let’s see how to use Entity Framework Queryable Extension Methods for aggregate functions over the List

1. Sum
2. Average
3. Minimum
4. Maximum
5. Count

.NET 6.0 has 12 overloads of these all methods for all numeric data types used in code ⏬

![8](https://user-images.githubusercontent.com/44539744/214580670-beecdbe6-1884-4eb1-acc6-f0d3f3277937.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 9 : Difference b/w Include and ThenInclude in Entity Framework**

Include and ThenInclude are two methods in EF that can be useful for improving the performance of a query by reducing the number of databases round trips.

Include is used for eager loading that’s why related entities come in a single query and database round trips are reduced. 

Main difference b/w them is level, include is used for 𝐒𝐢𝐧𝐠𝐥𝐞 𝐋𝐞𝐯𝐞𝐥 travelling along entities and ThenInclude is helpful in 𝐌𝐮𝐥𝐭𝐢𝐥𝐞𝐯𝐞𝐥 𝐑𝐞𝐭𝐫𝐢𝐞𝐯𝐚𝐥.

![9](https://user-images.githubusercontent.com/44539744/214586003-1859945a-b2eb-4234-9c0f-2e8c3eadf174.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 10 : Use ToQueryString() Extension method while debugging**

ToQueryString is a custom extension method that converts IQueryable to SQL Query at the back-end side, especially helpful for debugging. ⏬

![10](https://user-images.githubusercontent.com/44539744/214630757-2de6e6f9-c8c7-4c60-b297-37dac38051f0.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 11 : How to avoid DbContext threading issues in Entity Framework**

When EF Core detects an attempt to use a DbContext instance concurrently, you'll see an InvalidOperationException with a message like this:

"A second operation started in this context before a previous operation was completed."

There are few ways that can help you to avoid threading issues in EF.

1. Use a separate DbContext instance for each thread. This ensures that each thread has its own DbContext instance, which means that there is no shared state between threads and no potential for threading conflicts.

𝐏𝐫𝐨𝐛𝐥𝐞𝐦: Costly in terms of memory usage

2. Use a thread-safe DbContext wrapper. In this approach, you would create a wrapper class for DbContext that uses synchronization techniques, such as the lock keyword to ensure that only one thread can access the DbContext instance at a time.

𝐏𝐫𝐨𝐛𝐥𝐞𝐦: It can impact performance because threads may have to wait for access to the DbContext instance.

3. Use 𝐚𝐬𝐲𝐧𝐜𝐡𝐫𝐨𝐧𝐨𝐮𝐬 methods that allows you to write code that can run concurrently on multiple threads. It can help improve the performance of your application by allowing multiple operations to be executed concurrently. We can use 𝐚𝐰𝐚𝐢𝐭 and 𝐚𝐬𝐲𝐧𝐜 to perform asynchronous operation.

I have so far used 𝐚𝐬𝐲𝐧𝐜𝐡𝐫𝐨𝐧𝐨𝐮𝐬 methods, which one do you practice frequently?

![11](https://user-images.githubusercontent.com/44539744/214631230-ed0f63a5-daf7-4f3e-9edb-641b6299ade8.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **Episode 12 : How to register Open Generics in .NET Core Dependency Injection**

If you have a generic interface and its generic implementation like we mostly do when we make a generic repository for CRUD operations and you want to register its dependency injection at startup, then there is a simple way of registering the DI.

1. For .NET 3.1 register in ConfigureServices in 𝐒𝐭𝐫𝐚𝐭𝐮𝐩.𝐜𝐬

2. For latest versions of .NET(6.0 ,7.0) register in 𝐏𝐫𝐨𝐠𝐫𝐚𝐦.𝐜𝐬

![12](https://user-images.githubusercontent.com/44539744/214640932-8a34f995-934c-43c4-a521-7f86625eda21.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 13 : What are CORS and how to enable them in .NET at API Level**

CORS stands for Cross Origin Resource sharing, so what exactly is cross origin.

These two URLs have the same origin:
𝗁𝗍𝗍𝗉𝗌://𝗆𝗒-𝗌𝗂𝗍𝖾-𝗇𝗈-𝟣.𝖼𝗈𝗆/𝖦𝖾𝗍/𝖧𝖺𝗄𝗎𝗇𝖺𝖬𝖺𝗍𝖺𝗍𝖺
𝗁𝗍𝗍𝗉𝗌://𝗆𝗒-𝗌𝗂𝗍𝖾-𝗇𝗈-𝟣.𝖼𝗈𝗆/𝖦𝖾𝗍/𝖠𝗅𝗅𝖨𝗌𝖶𝖾𝗅𝗅

These URLs have different origins
𝗁𝗍𝗍𝗉𝗌://𝗆𝗒-𝗌𝗂𝗍𝖾-𝗇𝗈-𝟣.𝖼𝗈𝗆/𝖦𝖾𝗍/𝖧𝖺𝗄𝗎𝗇𝖺𝖬𝖺𝗍𝖺𝗍𝖺
𝗁𝗍𝗍𝗉://𝗆𝗒-𝗌𝗂𝗍𝖾-𝗇𝗈-𝟣.𝗇𝖾𝗍/𝖦𝖾𝗍/𝖠𝗅𝗅𝖨𝗌𝖶𝖾𝗅𝗅

To facilitate requests from different origins you need to enable CORS in .NET.

In .NET 6 by using the combination of these methods you can enable CORS as per your requirement.

𝐀𝐥𝐥𝐨𝐰𝐀𝐧𝐲𝐎𝐫𝐢𝐠𝐢𝐧: This policy allows requests from any origin.

𝐖𝐢𝐭𝐡𝐎𝐫𝐢𝐠𝐢𝐧𝐬: This policy allows requests from specific origins. You can specify one or more origins as arguments to this method.

𝐀𝐥𝐥𝐨𝐰𝐀𝐧𝐲𝐇𝐞𝐚𝐝𝐞𝐫: This policy allows requests with any header.

𝐖𝐢𝐭𝐡𝐇𝐞𝐚𝐝𝐞𝐫𝐬: This policy allows requests with specific headers. You can specify one or more headers as arguments to this method.

𝐀𝐥𝐥𝐨𝐰𝐀𝐧𝐲𝐌𝐞𝐭𝐡𝐨𝐝: This policy allows requests with any HTTP method (e.g., GET, POST, PUT, DELETE).

𝐖𝐢𝐭𝐡𝐌𝐞𝐭𝐡𝐨𝐝𝐬: This policy allows requests with specific HTTP methods. You can specify one or more methods as arguments to this method.

Few Things to Keep in mind

✔️CORS is not a security feature. CORS is a W3C standard that allows a server to relax the same-origin policy.

✔️An API isn't safer by allowing CORS.

✔️It's a way for a server to allow browsers to execute a cross-origin request that otherwise would be forbidden.

✔️Browsers without CORS can't do cross-origin requests.

![CORS](https://user-images.githubusercontent.com/44539744/214822094-1ebea86a-a340-4ded-8ec5-1b4cbb180234.jpg)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **Episode 14 : Common Middlewares in .NET API**

Middleware is software that's assembled into an app pipeline to handle requests and responses. Each component:

Chooses whether to pass the request to the next component in the pipeline.

Can perform work before and after the next component in the pipeline.

Here are some common types of middleware that might be used in a .NET API program:

1. Routing
2. Exception handling
3. Authentication and authorization
4. CORS (Cross-Origin Resource Sharing)
5. Response compression
6. Request validation
7. Response caching
8.Static file serving

𝐑𝐨𝐮𝐭𝐢𝐧𝐠 𝐦𝐢𝐝𝐝𝐥𝐞𝐰𝐚𝐫𝐞: This middleware is responsible for determining which endpoint should handle a particular request based on the request's path and method.

𝐄𝐱𝐜𝐞𝐩𝐭𝐢𝐨𝐧 𝐡𝐚𝐧𝐝𝐥𝐢𝐧𝐠 𝐦𝐢𝐝𝐝𝐥𝐞𝐰𝐚𝐫𝐞: This middleware is responsible for catching and handling exceptions that occur during the processing of a request.

𝐀𝐮𝐭𝐡𝐞𝐧𝐭𝐢𝐜𝐚𝐭𝐢𝐨𝐧 𝐚𝐧𝐝 𝐚𝐮𝐭𝐡𝐨𝐫𝐢𝐳𝐚𝐭𝐢𝐨𝐧 𝐦𝐢𝐝𝐝𝐥𝐞𝐰𝐚𝐫𝐞: This middleware is responsible for verifying that a request is from an authenticated and authorized user.

𝐂𝐎𝐑𝐒 (𝐂𝐫𝐨𝐬𝐬-𝐎𝐫𝐢𝐠𝐢𝐧 𝐑𝐞𝐬𝐨𝐮𝐫𝐜𝐞 𝐒𝐡𝐚𝐫𝐢𝐧𝐠) 𝐦𝐢𝐝𝐝𝐥𝐞𝐰𝐚𝐫𝐞: This middleware is responsible for adding the necessary headers to allow a browser to make cross-origin requests to the API.

𝐑𝐞𝐬𝐩𝐨𝐧𝐬𝐞 𝐜𝐨𝐦𝐩𝐫𝐞𝐬𝐬𝐢𝐨𝐧 𝐦𝐢𝐝𝐝𝐥𝐞𝐰𝐚𝐫𝐞: This middleware is responsible for compressing the response payload in order to reduce the size of the response and improve performance.

𝐑𝐞𝐪𝐮𝐞𝐬𝐭 𝐯𝐚𝐥𝐢𝐝𝐚𝐭𝐢𝐨𝐧 𝐦𝐢𝐝𝐝𝐥𝐞𝐰𝐚𝐫𝐞: This middleware is responsible for validating incoming requests to ensure that they conform to the expected format.

𝐑𝐞𝐬𝐩𝐨𝐧𝐬𝐞 𝐜𝐚𝐜𝐡𝐢𝐧𝐠 𝐦𝐢𝐝𝐝𝐥𝐞𝐰𝐚𝐫𝐞: This middleware is responsible for caching responses in order to reduce the load on the server and improve performance.

𝐒𝐭𝐚𝐭𝐢𝐜 𝐟𝐢𝐥𝐞 𝐬𝐞𝐫𝐯𝐢𝐧𝐠 𝐦𝐢𝐝𝐝𝐥𝐞𝐰𝐚𝐫𝐞: This middleware is responsible for serving static files, such as HTML, CSS, and JavaScript files, from the file system.

It’s important to note that the order in which middleware is added to the pipeline can be important, as the middleware will be executed in the order in which it is added. For example, if the authentication middleware is added before the routing middleware, the routing middleware will not be executed until the authentication middleware has completed.

![14](https://user-images.githubusercontent.com/44539744/214941977-4da2f56f-6ff1-404f-aa92-960e83989927.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **Episode 15 : Response Compression in .NET Core and how to configure its middleware**

Network bandwidth is a limited resource. Reducing the size of the response usually increases the responsiveness of an app, often dramatically. One way to reduce payload sizes is to compress an app's responses.

𝐖𝐡𝐚𝐭 𝐢𝐬 𝐑𝐞𝐬𝐩𝐨𝐧𝐬𝐞 𝐂𝐨𝐦𝐩𝐫𝐞𝐬𝐬𝐢𝐨𝐧
Response compression is a technique that can be used to reduce the size of HTTP responses, which can improve the performance of a web application by reducing the amount of data that needs to be transmitted over the network.

𝐁𝐞𝐧𝐞𝐟𝐢𝐭𝐬 𝐨𝐟 𝐑𝐞𝐬𝐩𝐨𝐧𝐬𝐞 𝐂𝐨𝐦𝐩𝐫𝐞𝐬𝐬𝐢𝐨𝐧

1.Improved performance: Compressing the response can reduce the amount of data that needs to be transmitted over the network, which can lead to faster page load times and a better user experience.

2.Reduced bandwidth usage: By compressing the response, you can reduce the amount of data that is transmitted over the network, which can lead to reduced bandwidth usage and lower costs for hosting and bandwidth.

3.Better SEO: Search engines take page load times into account when ranking websites, so a faster loading website may rank higher in search results.

𝐇𝐨𝐰 𝐭𝐨 𝐜𝐨𝐧𝐟𝐢𝐠𝐮𝐫𝐞 𝐑𝐞𝐬𝐩𝐨𝐧𝐬𝐞 𝐂𝐨𝐦𝐩𝐫𝐞𝐬𝐬𝐢𝐨𝐧 𝐌𝐢𝐝𝐝𝐥𝐞𝐰𝐚𝐫𝐞 𝐢𝐧 .𝐍𝐄𝐓
We can configure it using the . NET middleware, AddResponseCompression.

.NET also Provides built in providers for compression we can configure their options as per our need.

1.BrotliCompressionProvider
Using it a text file response at 2,044 bytes was compressed to ~979 bytes.

2. GzipCompressionProvider
Using it a Scalable Vector Graphics (SVG) image response at 9,707 bytes was compresses to ~4,459 bytes

𝐔𝐑𝐋: https://bit.ly/3G3rsIj

𝐂𝐨𝐦𝐩𝐫𝐞𝐬𝐬𝐢𝐨𝐧 𝐋𝐞𝐯𝐞𝐥𝐬
𝐎𝐩𝐭𝐢𝐦𝐚𝐥 - The compression operation should be optimally compressed, even if the operation, it takes a longer time to complete.

𝐅𝐚𝐬𝐭𝐞𝐬𝐭 - The compression operation should complete as quickly as possible, even if the resulting file is not optimally compressed.

𝐍𝐨 𝐂𝐨𝐦𝐩𝐫𝐞𝐬𝐬𝐢𝐨𝐧 - No compression should be performed on the file.

𝐒𝐦𝐚𝐥𝐥𝐞𝐬𝐭 𝐒𝐢𝐳𝐞 - The compression operation should create output as small as possible, even if the
operation takes a longer time to complete.

𝐌𝐈𝐌𝐄 𝐓𝐲𝐩𝐞𝐬 𝐛𝐲 𝐃𝐞𝐟𝐚𝐮𝐥𝐭 𝐒𝐮𝐩𝐩𝐨𝐫𝐭𝐞𝐝 𝐁𝐲 .𝐍𝐄𝐓 𝐏𝐫𝐨𝐯𝐢𝐝𝐞𝐫𝐬

1. text/plain
2. text/css
3. application/javascript
4. text/html
5. application/xml
5. text/xml
7. application/json
8. text/json
9. application/wasm

![15](https://user-images.githubusercontent.com/44539744/215045805-5d95ca27-aafa-4589-b38c-bb32b89cd66c.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **Episode 16 : Count() vs TryGetNonEnumeratedCount() and Which one is better ?**
  
 𝐂𝐨𝐮𝐧𝐭()
   
 This method will make an enumeration to calculate the count of elements.

 Available in all versions of .NET

   
𝐓𝐫𝐲𝐆𝐞𝐭𝐍𝐨𝐧𝐄𝐧𝐮𝐦𝐞𝐫𝐚𝐭𝐞𝐝𝐂𝐨𝐮𝐧𝐭()
   
 This attempts to determine the number of elements in a sequence without forcing an enumeration.

 It is available in .NET 6 and .NET 7

 It is available only on the ICollection<T> interface.

 It is typically a constant-time operation, but ultimately this depends on the complexity characteristics of the underlying collection's implementation.
   
![16](https://user-images.githubusercontent.com/44539744/215046453-f293906b-2799-43c5-b7ed-77299d39c2a3.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **Episode 17 : Everything about Rate Limiting in .NET**

Rate limiting is a technique used to control the amount of incoming and outgoing traffic to a network or service. It is often used to protect servers and other resources from being overwhelmed by too many requests, or to prevent abuses such as distributed denial of service (DDoS) attacks.

𝐇𝐨𝐰 𝐢𝐭 𝐰𝐨𝐫𝐤𝐬?
Rate limiting works by setting a limit on the number of requests that a client can make to a server within a specified time period. If the client exceeds the rate limit, the server will return an error, typically an HTTP status code 429 (Too Many Requests), to the client.

𝐁𝐞𝐧𝐞𝐟𝐢𝐭𝐬 𝐨𝐟 𝐑𝐚𝐭𝐞 𝐋𝐢𝐦𝐢𝐭𝐢𝐧𝐠?
1. Protecting against denial-of-service attacks of specific types.
2. Maintaining service availability.
3. Reducing resource consumption.
4. Detecting & blocking maliciousbehavior.
5. Improving user experience.

𝐂𝐨𝐧𝐬 𝐨𝐟 𝐑𝐚𝐭𝐞 𝐋𝐢𝐦𝐢𝐭𝐢𝐧𝐠?
Rate limiting cannot distinguish between good and bad traffic, it will just look into IP and number of requests, so in some cases by changing the IP address attack is still possible.

𝐀𝐭 𝐰𝐡𝐢𝐜𝐡 𝐩𝐨𝐢𝐧𝐭 𝐰𝐞 𝐜𝐚𝐧 𝐚𝐩𝐩𝐥𝐲 𝐑𝐚𝐭𝐞 𝐋𝐢𝐦𝐢𝐭𝐢𝐧𝐠?
1. Network Edge
2. Application Layer
3. Database Layer
4. Service Level

𝐇𝐨𝐰 𝐜𝐚𝐧 𝐈 𝐯𝐞𝐫𝐢𝐟𝐲 𝐭𝐡𝐚𝐭 𝐑𝐚𝐭𝐞 𝐋𝐢𝐦𝐢𝐭𝐢𝐧𝐠 𝐡𝐚𝐬 𝐛𝐞𝐞𝐧 𝐚𝐝𝐝𝐞𝐝?
You can check from response headers of your request there would be complete information that is your remaining limit, what is limit time etc. if your Rate Limiting has successfully configured.

𝐇𝐨𝐰 𝐭𝐨 𝐚𝐝𝐝 𝐑𝐚𝐭𝐞 𝐋𝐢𝐦𝐢𝐭𝐢𝐧𝐠 𝐢𝐧 .𝐍𝐄𝐓 𝐀𝐩𝐩𝐥𝐢𝐜𝐚𝐭𝐢𝐨𝐧?
We can apply rate limiting on Application Layer in our project using Asp Net Core Rate Limit NuGet Package⏬

![17](https://user-images.githubusercontent.com/44539744/215259530-e9bddc93-0be9-40cd-b33a-77e04991badf.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **Episode 18 : A basic visit to Response Caching along with its implementation in .NET**

Response caching is a technique for storing the responses of an API or web application in a cache so that they can be served faster to subsequent requests. The responses are stored in a cache with a key that uniquely identifies them, and the cache has a limited size and a policy for removing items when it becomes full.

𝐁𝐞𝐧𝐞𝐟𝐢𝐭𝐬 𝐨𝐟 𝐑𝐞𝐬𝐩𝐨𝐧𝐬𝐞 𝐂𝐚𝐜𝐡𝐢𝐧𝐠?
1. Improved performance by reducing the load on the server.

2. Reduced server load, as it can serve the cached response instead of generating a new one.

3. Reduced bandwidth usages it reduces the amount of data that needs to be transferred between the server and the client.

4. Improved security as it can reduce the number of requests that reach the server, reducing the risk of certain types of attacks.

𝐎𝐧 𝐰𝐡𝐢𝐜𝐡 𝐫𝐞𝐪𝐮𝐞𝐬𝐭𝐬 𝐰𝐞 𝐜𝐚𝐧 𝐚𝐩𝐩𝐥𝐲 𝐑𝐞𝐬𝐩𝐨𝐧𝐬𝐞 𝐂𝐚𝐜𝐡𝐢𝐧𝐠
1. Get
2. Head

𝐅𝐞𝐰 𝐜𝐨𝐧𝐬𝐭𝐫𝐚𝐢𝐧𝐭𝐬 𝐟𝐨𝐫 𝐑𝐞𝐬𝐩𝐨𝐧𝐬𝐞 𝐂𝐚𝐜𝐡𝐢𝐧𝐠
1.The request must result in a server response with a 200 (OK) status code.

2.Response Caching Middleware must be placed before middleware that require caching. For more information, see ASP.NET Core Middleware.

3.The Authorization header must not be present.

4. Cache-Control header parameters must be valid, and the response must be marked public and not marked private.

5. The Content-Length header value (if set) must match the size of the response body.

𝐒𝐨𝐦𝐞 𝐫𝐞𝐚𝐥-𝐰𝐨𝐫𝐥𝐝 𝐞𝐱𝐚𝐦𝐩𝐥𝐞𝐬 𝐨𝐟 𝐑𝐞𝐬𝐩𝐨𝐧𝐬𝐞 𝐂𝐚𝐜𝐡𝐢𝐧𝐠
1. News website
2. E-commerce websites
In your application you can apply response caching to those requests whose response is changed after a time and you are sure about it.

𝐇𝐨𝐰 𝐜𝐚𝐧 𝐈 𝐯𝐞𝐫𝐢𝐟𝐲 𝐢𝐭?
Create an application apply caching and then request it from Postman and set time to 60 minutes, you will notice that only first request will reach the controller, after that even if you try request will not reach controller.

![18](https://user-images.githubusercontent.com/44539744/215290913-3cd19681-1727-4d01-9c13-41ae24958c7f.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 19 : Do you know how to initialize an Empty Enumerable in .NET ?**

✔️ .NET provides us the Empty() method to initialize an empty Enumerable of any type.

✔️This method is useful for passing an empty sequence to a user defined method that takes an IEnumerable<T> ⤵️
 
 ![19](https://user-images.githubusercontent.com/44539744/215291120-3d169215-d298-4603-a070-2919718246f5.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 20 : Dependency Injection Explained in .NET**

This post crossed 100K views on my LinkedIn
   
![100K](https://user-images.githubusercontent.com/44539744/215291282-0472c8aa-ce7c-43b6-be0f-81f995edb9f3.PNG)

Dependency injection involves providing a class with its required dependencies from an external source rather than having the class create them itself.

This helps to decouple the object creation process from the caller, leading to a more modular and flexible system.

In other words, it allows a class to focus on its core functionality rather than worrying about how to create and manage its dependencies.

𝐖𝐡𝐲 𝐝𝐨 𝐰𝐞 𝐧𝐞𝐞𝐝 𝐝𝐞𝐩𝐞𝐧𝐝𝐞𝐧𝐜𝐲 𝐢𝐧𝐣𝐞𝐜𝐭𝐢𝐨𝐧?
By using DI classes are decoupled from each other so you make changes at one place and it is reflected all over the places.

𝐇𝐨𝐰 𝐭𝐨 𝐢𝐦𝐩𝐥𝐞𝐦𝐞𝐧𝐭 𝐝𝐞𝐩𝐞𝐧𝐝𝐞𝐧𝐜𝐲 𝐢𝐧𝐣𝐞𝐜𝐭𝐢𝐨𝐧?

✅ In .NET 6 we implement DI in Program.cs class by using builder.Services

✅ For previous versions of .NET, to implement DI we need to add the service in “ConfigureServices” method which is in Startup.cs file

𝐃𝐢𝐟𝐟𝐞𝐫𝐞𝐧𝐭 𝐰𝐚𝐲𝐬 𝐨𝐟 𝐢𝐦𝐩𝐥𝐞𝐦𝐞𝐧𝐭𝐢𝐧𝐠 𝐃𝐞𝐩𝐞𝐧𝐝𝐞𝐧𝐜𝐲 𝐈𝐧𝐣𝐞𝐜𝐭𝐢𝐨𝐧
There are three ways of doing DI:

1.Scoped ➡️ It will create an instance per scope, if we are in same scope same instance would be used. Whenever we go out of scope new instance would be created.

2. Transient ➡️ It creates new instances every time its injected.

3. Singleton ➡️ It instantiates one global object for all requests coming to the server from any user.

𝐁𝐞𝐧𝐞𝐟𝐢𝐭𝐬 𝐨𝐟 𝐃𝐞𝐩𝐞𝐧𝐝𝐞𝐧𝐜𝐲 𝐈𝐧𝐣𝐞𝐜𝐭𝐢𝐨𝐧

1.Improved testability: Dependency injection makes it easier to write unit tests for your code, as you can easily substitute mock objects for the real dependencies.

2. Enhanced flexibility: By injecting dependencies from the outside, you can easily change the implementation of a class's dependencies without having to modify the class itself. This makes it easier to adapt your application to changing requirements.

3. Increased modularity: Dependency injection encourages the use of small, single-purpose classes that are easy to test and reuse in different contexts. This can lead to a more modular and maintainable codebase.

4. Better separation of concerns: Dependency injection helps to separate the concerns of different parts of your application, making it easier to understand and maintain the code.

5. Enhanced decoupling: Dependency injection promotes loose coupling between classes, which can make your application more resilient to change and easier to test.
   
![20](https://user-images.githubusercontent.com/44539744/215291108-86fda617-37a5-4514-85f3-da75c142ad11.PNG)
   
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 21 : IEnumerable vs IQueryable in .NET**

IEnumerable and IQueryable interfaces are both used to work with collections of data and both support LINQ (Language Integrated Query).

𝐈𝐐𝐮𝐞𝐫𝐲𝐚𝐛𝐥𝐞

✅ IQueryable executes queries on the server side.

✅ It is designed specifically to work with LINQ

✅ It extends IEnumerable, which means it includes all of the functionality of IEnumerable.

✅ It can be more efficient when working with large data

✅ It can be more helpful when you have to apply a lot of filtrations, you can apply all filters on Queryable and when you are done you can convert data to desired collection

𝐈𝐄𝐧𝐮𝐦𝐞𝐫𝐚𝐛𝐥𝐞
✔️ IEnumerable executes queries on the client side.

✔️ It is generally used to work with in-memory data collections.

Explanation with code ⤵️

![21](https://user-images.githubusercontent.com/44539744/215313172-38f4a4cf-25ed-48ee-81d3-add2925feb34.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **Episode 22 : Why is it generally considered good practice to keep Dependency Injections in seperate class !**

It is good practice to move all of your dependency injection work in a separate class instead of filling your Program.cs with all Injections. Here are some benefits of this approach

1. By keeping dependency injections in separate classes, you can better adhere to the principle of separation of concerns. So, your Program.cs is just focusing on configuration and its DI class headache to manage dependencies.

2. Keeping dependency injections in separate classes can make it easier to maintain the application over time. For any change in DI’s, you would not be changing the Program.cs rather you would just change the desired dependency injection class

3. For better understanding we can create different DI classes that would be dealing with similar dependencies.

How you prefer to keep your dependencies? 📝⤵️

![22](https://user-images.githubusercontent.com/44539744/215313347-c01c5130-1aa6-41a4-9b65-7939e3818e40.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 23 : Difference b/w GetType() and typeOf() Methods in .NET**

Both TypeOf and GetType help you to get the type with a little difference

✅ typeof gets the type from a class while GetType gets type from an object.

✅ The GetType method is used to retrieve the type of an object at runtime, while the typeof operator is used to retrieve the type of an object at compile-time.

I have described one example where typeof can prove helpful , what other situations could be where GetType and typeof can save us 📝⏬

![23](https://user-images.githubusercontent.com/44539744/215313409-ee654e19-f2e8-4f41-a3d4-3d26be8a76d9.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 24 : Difference b/w VAR and DYNAMIC keyword in C#**

𝐕𝐀𝐑
✅ VAR is early binded (statically checked)

✅ It looks at your right-hand side data and then during compile time it decides the left-hand side data type

✅ Use of var makes your code more readable, simplified and reduces the typing.

𝐃𝐘𝐍𝐀𝐌𝐈𝐂
✔️ Dynamic is late binded (dynamically evaluated).

✔️ It is used to work on dynamic objects.

✔️ It helps us when we are not sure about the data type of objects, saves us from a lot of data type-oriented checking (because the compiler ignores them).

💭
There is a debate over var or proper type. I would like to hear your opinion, many people say that we should use var instead of proper type, but some say that if you are familiar with type then why would you go for var. 📝⏬

![24](https://user-images.githubusercontent.com/44539744/215313533-05a44ce5-41b2-4b51-828f-46dd8f38e7cc.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **Episode 25 : StringBuilder vs string in C#**

Difference b/w String and StringBuilder

𝐒𝐭𝐫𝐢𝐧𝐠𝐁𝐮𝐢𝐥𝐝𝐞𝐫
1. StringBuilder is mutable

2. StringBuilder will only create one object on heap and every time it would be updated with new value even if you append/insert 1 million values.

𝐒𝐭𝐫𝐢𝐧𝐠
1. String is immutable.

2. Every time when we update data in string it creates a new instance of object. So, if you update value 1K times it will create 1K new instances.

𝐓𝐢𝐦𝐞 𝐝𝐢𝐟𝐟𝐞𝐫𝐞𝐧𝐜𝐞 𝐨𝐯𝐞𝐫 𝟏𝟎,𝟎𝟎𝟎 𝐢𝐭𝐞𝐫𝐚𝐭𝐢𝐨𝐧𝐬
A good rule of thumb is to use strings when you aren't going to perform operations like(Append/Remove) repetitively, use StringBuilder for vice versa.

I took 10,000 iterations and checked the difference for that see the difference in picture.⏬

![25](https://user-images.githubusercontent.com/44539744/215313615-903ad9cc-4550-4a46-b4ba-368f2a643c1c.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# **Episode 26 : Arrays vs ArrayList in C#**

Difference b/w Array and Arraylist and which one is faster.

𝐀𝐫𝐫𝐚𝐲
   
1. Arrays are fixed in size.
2. It is strongly typed, in other words when you create an array it can store only one data type.

𝐀𝐫𝐫𝐚𝐲 𝐋𝐢𝐬𝐭

1. It is a collection from System.Collection in .NET
   
2. It is dynamically resizable.
   
3. It can store any data type

𝐖𝐡𝐢𝐜𝐡 𝐨𝐧𝐞 𝐢𝐬 𝐟𝐚𝐬𝐭𝐞𝐫 𝐚𝐧𝐝 𝐖𝐡𝐲 ?
Array list takes any data type which leads to boxing and unboxing. As arrays are strongly typed, they do not do boxing and unboxing. So, arrays are faster as compared to array lists.

When boxing and unboxing happens the data needs to jump from stack memory to heap and vice-versa which is a bit of memory intensive process. As a good practice avoid boxing and unboxing wherever possible.

𝐑𝐞𝐜𝐚𝐩 𝐨𝐟 𝐁𝐨𝐱𝐢𝐧𝐠 𝐚𝐧𝐝 𝐔𝐧𝐛𝐨𝐱𝐢𝐧𝐠
Boxing and Unboxing are used to convert value types to reference types and vice versa.
When the value type is moved to a reference type it’s called Boxing. The vice-versa is termed as Unboxing.

𝐖𝐡𝐞𝐧 𝐬𝐡𝐨𝐮𝐥𝐝 𝐰𝐞 𝐮𝐬𝐞 𝐀𝐫𝐫𝐚𝐲𝐥𝐢𝐬𝐭 𝐨𝐫 𝐀𝐫𝐫𝐚𝐲?
Overall, Arraylist is a more flexible and convenient choice when you need to work with a collection of objects that can change size over time, while an array is a good choice when you need to work with a fixed-size collection of elements of the same data type.

![26](https://user-images.githubusercontent.com/44539744/215477772-a9e050b3-c06e-4e07-99ae-a14ed7822ad5.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **Episode 27 : Extension Methods in C#**

An extension method is a special kind of static method that allows you to "add" methods to an existing type without modifying the type itself.

You already know about extension method let me remind you, you might have used method ToString() that is extension Method for string

𝐁𝐞𝐧𝐞𝐟𝐢𝐭𝐬 𝐨𝐟 𝐮𝐬𝐢𝐧𝐠 𝐞𝐱𝐭𝐞𝐧𝐬𝐢𝐨𝐧 𝐦𝐞𝐭𝐡𝐨𝐝𝐬
1. Extension methods allow you to reuse code across multiple types without having to create a new subclass or interface for each type.

2. They reduce code duplication and improve the maintainability of your code.

3. They can make your code more readable by allowing you to define methods that are directly related to the type they are extending

4. These methods are used extensively in the LINQ (Language Integrated Query) library.

5. They are very simple to develop just a static method of static class and in parameter you add this keyword.

𝐇𝐨𝐰 𝐭𝐨 𝐜𝐫𝐞𝐚𝐭𝐞 𝐄𝐱𝐭𝐞𝐧𝐬𝐢𝐨𝐧 𝐌𝐞𝐭𝐡𝐨𝐝?
Extension methods are defined as static methods in a static class, and use the "this" keyword to specify the type they are extending.

𝐒𝐨𝐦𝐞 𝐬𝐜𝐞𝐧𝐞𝐫𝐢𝐨
Suppose you are creating some game and your text should be in some weird notations that all characters should be lower case followed by upper case, so it’s better to create an extension method for string and then use it throughout the application.
 
![27](https://user-images.githubusercontent.com/44539744/215479510-4a3bbffa-93fa-4d57-aa14-5b643ba61f8f.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **Episode 28 : Common design principles you should keep in mind while developing applications**

✅𝐒𝐞𝐩𝐚𝐫𝐚𝐭𝐢𝐨𝐧 𝐨𝐟 𝐜𝐨𝐧𝐜𝐞𝐫𝐧𝐬
This principle asserts that software should be separated based on the kinds of work it performs.

Consider a media player application that has a feature to create and save playlists. The application has logic to retrieve a list of songs from the user's library and logic to organize the songs into playlists. The behavior for retrieving the list of songs should be separate from the behavior for creating the playlists, since these are separate concerns.

✅ 𝐄𝐧𝐜𝐚𝐩𝐬𝐮𝐥𝐚𝐭𝐢𝐨𝐧
Encapsulation is a way to protect the data inside an object from being changed by code outside of that object.

In other words, it helps to keep the internal state of an object hidden from the rest of the program. Instead of allowing other parts of the program to directly access and change the data inside an object, we should provide specific methods (getter/setter) that can be used to manipulate the data in a controlled way.

✅𝐒𝐢𝐧𝐠𝐥𝐞 𝐫𝐞𝐬𝐩𝐨𝐧𝐬𝐢𝐛𝐢𝐥𝐢𝐭𝐲
The single responsibility principle is a concept in software development that says that each object or component in a program should only have one job or responsibility.

For example, the user interface should be responsible for presenting information to the user, while the data access layer should be responsible for storing and retrieving data. The business logic, which is the part of the program that does the important work, should be kept in its own section so it can be tested and changed without affecting other parts of the program.

✅𝐃𝐨𝐧’𝐭 𝐫𝐞𝐩𝐞𝐚𝐭 𝐲𝐨𝐮𝐫𝐬𝐞𝐥𝐟 (𝐃𝐑𝐘)
The application should avoid specifying behavior related to a particular concept in multiple places as this practice is a frequent source of errors.

Avoid binding together behavior that is only coincidentally repetitive. For example, just because two different constants both have the same value, that doesn’t mean you should have only one constant, if conceptually they’re referring to different things. Duplication is always preferable to coupling to the wrong abstraction.

✅𝐃𝐞𝐩𝐞𝐧𝐝𝐞𝐧𝐜𝐲 𝐈𝐧𝐯𝐞𝐫𝐬𝐢𝐨𝐧
The direction of dependency within the application should be in the direction of abstraction, not implementation details.

The practice of dependency injection is made possible by following the dependency inversion principle. See the difference of graph when Dependency Inversion is applied.

![28](https://user-images.githubusercontent.com/44539744/215480165-4cdb04f2-d827-463f-b0da-296e4fde9d9f.PNG)
   
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

 # **Episode 29 : Sealed keyword in C#**

When applied to a class, the sealed modifier prevents other classes from inheriting from it.

When applied to a method or property, the sealed modifier must always be used with override because structs are implicitly sealed, they cannot be inherited.

𝐖𝐡𝐞𝐧 𝐬𝐡𝐨𝐮𝐥𝐝 𝐰𝐞 𝐦𝐚𝐤𝐞 𝐨𝐮𝐫 𝐜𝐥𝐚𝐬𝐬 𝐬𝐞𝐚𝐥𝐞𝐝
1. It ensures that a class cannot be subclasses / used as base class, either to maintain the integrity of the class's design or to improve performance.
2. When you want to create a class that can be used as a singleton, to ensure that only one instance of the class can be created (Although defining a class does not ensure that it would become singleton, we need to take care for few more things for singleton).

𝐇𝐨𝐰 𝐦𝐚𝐤𝐢𝐧𝐠 𝐚 𝐜𝐥𝐚𝐬𝐬 𝐬𝐞𝐚𝐥𝐞𝐝 𝐢𝐦𝐩𝐫𝐨𝐯𝐞𝐬 𝐭𝐡𝐞 𝐩𝐞𝐫𝐟𝐨𝐫𝐦𝐚𝐧𝐜𝐞
A sealed class does not have to worry about executing code in derived classes that may override members of the sealed class at runtime
It reduces the number of methods calls that need to be made at runtime. When a method is called on an object, the runtime must determine which method to execute by checking the object's type and searching up the inheritance hierarchy until it finds a matching method.
   
![29](https://user-images.githubusercontent.com/44539744/215480857-9f6d53ec-e666-45b8-baed-e39883c7bd03.PNG)
   
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Episode 30 : String Interpolation vs Verbitam Identifier vs Raw String Literal

Let's see the difference b/w them

𝐒𝐭𝐫𝐢𝐧𝐠 𝐢𝐧𝐭𝐞𝐫𝐩𝐨𝐥𝐚𝐭𝐢𝐨𝐧 𝐮𝐬𝐢𝐧𝐠 $
The $ special character identifies a string literal as an interpolated string. An interpolated string is a string literal that might contain interpolation expressions.
String interpolation provides a more readable, convenient syntax to format strings. It's easier to read than string composite formatting.
 
𝐕𝐞𝐫𝐛𝐚𝐭𝐢𝐦 𝐈𝐝𝐞𝐧𝐭𝐢𝐟𝐢𝐞𝐫 - @
The @ special character serves as a verbatim identifier. It can be used in the following ways
1. To enable C# keywords to be used as identifiers.
2. It helps to specify a string that should be interpreted literally, without any escape characters being processed.

𝐑𝐚𝐰 𝐬𝐭𝐫𝐢𝐧𝐠 𝐥𝐢𝐭𝐞𝐫𝐚𝐥 - """
A raw string literal (Available in C# 11.0) starts and ends with a minimum of three double quote (") characters.

1. It can span multi lines
2. Like @ it can also specify a string that should be interpreted literally
3. It can combine work with interpolated string
4. It can be helpful in designing server-side emails as well

While working with them following rules should be kept in mind.

1. Both opening/closing quote characters must be on their own line.
2. Any whitespace to the left of the closing quotes is removed from all lines of the raw string literal.
3. Whitespace following the opening quote on the same line is ignored.
4. Whitespace only lines following the opening quote are included in the string literal.
 
![30](https://user-images.githubusercontent.com/44539744/215483678-8256e836-0a55-460d-97f9-a7117defa079.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Episode 31 : Pad Left and Pad Right Method of String in C#

The 𝐏𝐚𝐝𝐋𝐞𝐟𝐭 and 𝐏𝐚𝐝𝐑𝐢𝐠𝐡𝐭 methods of the 𝐒𝐭𝐫𝐢𝐧𝐠 class in C# can be used to pad the current string with a specified number of characters on the left or right side, respectively.

🎯 These methods can be useful when you want to align strings in a particular way.

🎯 They can give you a helping hand when you want to ensure that a string meets a minimum length requirement.

![31](https://user-images.githubusercontent.com/44539744/215843344-2991a7af-1b6f-4b85-b040-f5c94fe22183.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Episode 32 : How to read values from appsetting.json through IOptions and apply validation on it

🎯 𝐒𝐭𝐞𝐩 𝟏 : Define your properties in key-value format in json file.

🎯 𝐒𝐭𝐞𝐩 𝟐 : Make a class with same properties , make sure names should be exactly same.

🎯 𝐒𝐭𝐞𝐩 𝟑 : Inject configurations in Program.cs (For .NET 6) and in ConfigureServices Method (Below than .NET 6)

🎯 𝐒𝐭𝐞𝐩 𝟒 : Now Inject class containing properties in constructor of your desired class where you need.

![32](https://user-images.githubusercontent.com/44539744/215964504-61dc5aa9-5541-498a-ab7f-505e45ba6f02.PNG)

If you want to add validations on your IOptions you can visit my friend Milans's blog post [here](https://www.milanjovanovic.tech/blog/adding-validation-to-the-options-pattern-in-asp-net-core)
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Episode 33 : How to add DbContext Dependency Injection in .NET Core API ?

🎯 𝐒𝐭𝐞𝐩 𝟏 : Define a DbContext class that represents the database context in your application.

🎯 𝐒𝐭𝐞𝐩 𝟐 : In the ConfigureServices/Program.cs add a call to the AddDbContext method to register the DbContext with the dependency injection container.

🎯 𝐒𝐭𝐞𝐩 𝟑 : Inject the DbContext instance into the constructor of your controllers or services that require it or maybe you can use Unit of work class as well , its up to you :)

![33](https://user-images.githubusercontent.com/44539744/216597151-d4353f4b-7c68-4bc8-a715-10825950f9bd.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

