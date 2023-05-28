1. What is the difference between IQueryable and IEnumerable interfaces? Provide some examples.
IEnumerable is the base interface for all collections in .NET. It provides a way to iterate over a collection of objects. 
When you use IEnumerable, the entire data set is loaded into memory and then filtered, sorted, or projected. This can be inefficient when working with large data sets.
IQueryable, on the other hand, is designed to work with data sources that support querying, such as databases. When you use IQueryable, 
the query is not executed immediately. Instead, it is translated into a query that can be executed against the data source. This can be more efficient when working with large data sets.

2. Describe IQueryProvider interface. What is it used for?
IQueryProvider is an interface in .NET that is used to translate LINQ queries into a format that can be executed against a specific data source.
It is used in conjunction with IQueryable to provide a way to query data sources that support it, such as databases.

The IQueryProvider interface has two methods:
CreateQuery(Expression expression): This method creates a new IQueryable object that represents the query specified by the expression parameter.
Execute(Expression expression): This method executes the query specified by the expression parameter and returns the result.

3. What is the role of Expressions for IQueryProvider?
Expressions play a crucial role in IQueryProvider because they represent the LINQ query as an expression tree. 
An expression tree is a data structure that represents the structure of a LINQ query as a set of expressions that can be analyzed and transformed.
When a LINQ query is executed against a data source that supports IQueryable, the query is translated into an expression tree.
The IQueryProvider then uses this expression tree to generate the appropriate query for the data source.
