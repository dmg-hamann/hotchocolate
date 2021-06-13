---
title: Overview
---

In this section we will learn everything about fetching data with Hot Chocolate.

# Resolvers

[Resolvers](/docs/hotchocolate/fetching-data/resolvers) are the main building blocks when it comes to fetching data. Every field in our GraphQL schema is backed by such a resolver function, responsible for fetching the data associated with this field. Since a resolver is just a function we can use it to retrieve data from a database, a REST service or any other data source.

# Datasource examples

Even though we can connect Hot Chocolate to any data source, most of the time it will be either a database or a REST service.

Therefore we prepared tutorials on how to fetch data from a

- [Database](/docs/hotchocolate/fetching-data/fetching-from-databases)
- [REST service](/docs/hotchocolate/fetching-data/fetching-from-rest)

# DataLoader

[DataLoaders](/docs/hotchocolate/fetching-data/dataloader) provide a way to deduplicate and batch requests to data sources. They can significantly improve the performance of our queries and ease the load on our data sources.

# Pagination

Hot Chocolate provides [pagination](/docs/hotchocolate/fetching-data/dataloader) capabilities out of the box. They allow us to expose pagination in a standardized way and can even take care of crafting the necessary pagination queries to our databases.

# Filtering and Sorting

When exposing a collection of entities, most of the time consumers need some sort of [filtering](/docs/hotchocolate/fetching-data/filtering) or [sorting](/docs/hotchocolate/fetching-data/sorting) capabilities.

Hot Chocolate makes implementing this a lot easier, by handling the generation of necessary input types and even translating the applied filters/sort into native database queries.

# Projections

[Projections](/docs/hotchocolate/fetching-data/projections) allow Hot Chocolate to project incoming GraphQL queries to the database.

If we for example only select the `Name` and `Id` of a user in our GraphQL query, Hot Chocolate will only select those two fields when querying the user in the database.
