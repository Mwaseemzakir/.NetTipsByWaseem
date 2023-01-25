# Table of Content

1. **Episode 1 : What is .AsNoTracking() and its benefits**
2. **Episode 2 : SingleAsync and FirstAsync Methods of LINQ in .NET**
3. **Episode 3 : Basic overview of Monolithic and Microservices applications**

-------------------------------------------------------------------------------------------------------------------------

1. **Episode 1 : What is .AsNoTracking() and its benefits**

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
**Episode 2 : SingleAsync and FirstAsync Methods of LINQ in .NET**

1. In .NET, SingleAsync and FirstAsync are methods that can be used to retrieve a single element from a collection of elements.
2. Both methods are similar in that they return the first element in a collection that satisfies a specified condition.
3. The main difference between SingleAsync and FirstAsync is that SingleAsync will throw an exception if there is more than one element in the collection that satisfies the specified condition, while FirstAsync will return the first element it finds and then stop.
4. SingleAsync can be used to ensure that there is exactly one element in the collection that satisfies the condition, while FirstAsync can be used to simply retrieve the first element that satisfies the condition, regardless of how many elements in the collection satisfy the condition.

![2](https://user-images.githubusercontent.com/44539744/214570781-9d81668d-fd7c-4aca-a8b8-c5ac8403fe37.png)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
**Episode 3 : Basic overview of Monolithic and Microservices applications**

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

