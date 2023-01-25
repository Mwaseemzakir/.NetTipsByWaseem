# Table of Content

1. **Episode 1 : What is .AsNoTracking() and its benefits**
2. **Episode 2 : SingleAsync and FirstAsync Methods of LINQ in .NET**
3. **Episode 3 : Basic overview of Monolithic and Microservices applications**
4. **Episode 4 : Difference b/w Boxing and Unboxing in C#**
5. **Episode 5 : Benefit of using AsReadOnly Method of List<T> in .NET**
6. **Episode 6 : Difference b/w Any and All Method for Collection in .NET**
7. **Episode 7 : Lazy Loading vs Eager Loading in EntityFramework**

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

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
**Episode 4 : Difference b/w Boxing and Unboxing in C#**

𝐁𝐨𝐱𝐢𝐧𝐠 and 𝐔𝐧𝐛𝐨𝐱𝐢𝐧𝐠 are used to convert value types to reference types and vice versa.
When value type is moved to a reference type it’s called as 𝐁𝐨𝐱𝐢𝐧𝐠 . 
The vice-versa is termed as 𝐔𝐧𝐛𝐨𝐱𝐢𝐧𝐠.

![4](https://user-images.githubusercontent.com/44539744/214574984-028acec4-6687-4060-810a-bd665f4e6c87.PNG)

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
**Episode 5 : Benefit of using AsReadOnly Method of List<T> in .NET**

Here are some benefits of 𝐀𝐬𝐑𝐞𝐚𝐝𝐎𝐧𝐥𝐲 Method of 𝐋𝐢𝐬𝐭<𝐓>
1. It gives you read only view of your collection.
2. It allows you to prevent the collection from being modified, either accidentally or intentionally
3. It can improve the performance of your code in some cases because the read-only wrapper provides a more restricted view of the collection.
4. This can be particularly beneficial when working with large collections, where even small performance improvements can make a significant difference.

![5](https://user-images.githubusercontent.com/44539744/214575801-06ee0b84-89b9-4607-b48e-65733f92acea.PNG)


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
**Episode 6 : Difference b/w Any and All Method for Collection in .NET**
   
𝐀𝐧𝐲 𝐯𝐬 𝐀𝐥𝐥 𝐄𝐱𝐭𝐞𝐧𝐬𝐢𝐨𝐧 𝐌𝐞𝐭𝐡𝐨𝐝 𝐨𝐟 𝐋𝐢𝐬𝐭<𝐓>
   
1.The 𝐀𝐥𝐥 method checks if all elements of a list satisfy a specified condition.
   
2.The 𝐀𝐧𝐲 method checks if any elements of a list satisfy a specified condition.

   ![6](https://user-images.githubusercontent.com/44539744/214576987-08fca7a8-531d-4a29-94d4-799d9050566d.PNG)
   
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
7. **Episode 7 : Lazy Loading vs Eager Loading in EntityFramework**

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

