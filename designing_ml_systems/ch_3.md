## Data Sources

- user-input data: very messy, can be malformatted, error filled. Also, users expecting output expect very low latency
- system-generated data: various logs and system outputs

**Data Serialization:** Process of converting a data structure or object state into a format that can be stored or transmitted and reconstructed later

Common Data Formats
![alt text](../artifacts/common_data_formats.png)

**JSON (Javascript Objecy Notation)**
- key-value pair paradign to handle different levels of structuredness
- json schemas are hard to edit once committed

*CSV (comma seperated values) is row major, Parquet is column major* Row major data access is faster for computers due to sequential nature
- CSV and JSOn are text files, Parquet are binary files
- Parquet files are smalled in size due to the binary nature

### Data Models

**Relational Models:**
- Accessed via query language
- Declarative language: You specify the outputs you want, and the computer figures out the steps needed to get the queried outputs
- Imperative language: You specify the steps needed for an action and the computer executes these steps to return the outputs
- Declarative ML is being researched (H2O AutoML). You mention the feature schema and output, it figures out the best model architecture

**NoSQL**
- Not only SQL models can also support relational models (eg document model, graph model)
- Document model: single continuous string (eg JSON, XML, Binary JSON)
- Each document has a unique key for retrieval. Document model doesnt enforce any schema (called schemaless)
- Document dbs have each document in priority, graph dbs have relationships between data items as priority.
- Repository for storing structured data is a data warehouse. Repository for storing unstructured data is called data lake.

![alt text](../artifacts/structured_vs_unstructured.png)

### Data Storage Engines and Processing

Workloads dbs are optimized for-

**Transactional & Analytical Processing**
- Transaction refers to any kind of action. Transactions are inserted as they are generated, occasionally updated when something changes, or deleted when no longer needed. This is called *Online Transaction Processing (OLTP)*
- Since they r user driven, they have low latency, high availability requirements.
- **ACID**
- Atomicity: guarantee all steps ina transaction are completed. If one fails, all should fail
- Consistency: all transactions must follow predefined rules
- Isolation: Guarantee 2 transactions happen at the same time as if they were isolated.
- Durability: once a transaction is committed, it remains committed even in a case of system failure




