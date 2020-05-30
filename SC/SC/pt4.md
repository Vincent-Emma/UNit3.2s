### Part 4 - Questions (and your Answers)

Answer the following questions, baseline ~3-5 sentences each, as if they were
interview screening questions (a form you fill when applying for a job):

- In the Northwind database, what is the type of relationship between the
  `Employee` and `Territory` tables?

Single (employee) to multiple (territories).
 The relationship between these tables is indicated in EmployeeTerritory. 
Each territory has a minimum of one employee associated with it while many territories are associated with single employees

- What is a situation where a document store (like MongoDB) is appropriate, and
  what is a situation where it is not appropriate?

A document store best if you start out with a big mess of unstructured data, and you want to incrementally make some sense out of it. An example would be if you're given files with zero type information (everything is strings).

If your data is already clean enough to be reasonably-well represented in a pandas dataframe, meaning it's a CSV, not everything is string when it can be something else, etc. and your pipeline isn't going to interact with webapps that add unverified input to them, then you'd probably want to skip JSON and document store and go straight to databases or dataframes.

- What is "NewSQL", and what is it trying to achieve?

NewSQL is tring to bridging the gap between NoSQL and SQL. 
It brings ACID compliance to a NoSQL database so data sensitive companies can get the benefits of the unstructured ways of NoSQL. 
For companies considering a relational db but need the scalablity of the unstructure NoSQL, then the NewSQL choice may be the right one.

(ACID (Atomicity (transactions decomposable to discrete units), Consistency (applying a valid transaction to a valid state returns a valid state), Isolation (equivalence between concurrent and sequential execution), and Durability (safe to e.g. a power outage mid-computation)) is a strong set of guarantees that make apps more accurate and less stressful for everybody.)
