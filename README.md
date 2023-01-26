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



-------------------------------------------------------------------------------------------------------------------------

# **Episode 1 : What is .AsNoTracking() and its benefits**

   𝐖𝐡𝐢𝐥𝐞 𝐮𝐬𝐢𝐧𝐠 𝐀𝐬𝐍𝐨𝐓𝐫𝐚𝐜𝐤𝐢𝐧𝐠
    1. The entity is not tracked by the context.
    2. EF does not know the state of its entity.
    3 Not recommended when you are performing Add/Update/Delete kind operations
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
