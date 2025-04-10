1. All newly created fields should have capitalized names.
2. New queries should work with the most up-to-date database version. If you make multiple changes, all queries should still work after the final updates.
3. For some queries, you may need to change the database schema.
4. When you are applying specific patterns, like polymorphic, subset, or bucket, name them accordingly. 
5. Document each major transformation using this format:
*“We applied {transformation name} because {reasoning behind it}. We expect {change/result} based on {observable measure, such as query speed, number of documents returned, index use, etc.}.”*



**Data Cleanup and Schema Adjustments:** [9 points in total]

1) Before working on the queries below, review the data and adjust the schema based on the typical use case described.

**Typical Use Case**: The most common use of the database is to show property listing information to customers. A query retrieves a listing document from the database. Currently, retrieving a listing takes too long. Decide what information should be included in a typical query and optimize the structure accordingly. For example, customers usually only need a sample of reviews, not all reviews (even though all reviews are stored). They also don’t need past transaction data. Update the document schema to fit this use case. This might involve creating new collections or documents.

**Data Cleanup**: Review the data for any errors (such as transactions that don’t belong to the listing) or unnecessary duplication, and clean it up where needed.