
# Characteristics (storage, Version control, concurrent, etc)


- Can store semi-structured data (JSON, Avro, ORC, Parquet and XML) alongside relational data
- Can query all of the data with standard ACID compliant SQL
- Snowflake offers instant scaling
- Automation of maintenance
- Built-in SQL autocomplete feature
- Seamless data sharing outside and inside an organization

## Storage

Data is compressed.

The cost is more than cold storage (like S3 or Azure).
The more data is stored the larger the discount given.

## Version control

There is a feature called dynamic Time Travel that allows access to prior versions of data for recovery and auditing purposes.

## Concurrent 

Great concurrency can be achieved with Snowflake because multiple virtual warehouses can be used on the same data.

One or more VM servers are organised as a virtual Warehouse cluster. The number of parallel threads depends on the resource available to the Virtual machine size chosen.

Snowflake tries to use as many parallel threads as possible for each query (depends on the virtual warehouse size).
If the data volume is very small and has a limited number of micro-partitions, the compiler can choose to use fewer threads.
The number of threads does not depend on concurrency, it does depend on the virtual warehouse size.

The number of concurrently running queries can be lowered using a parameter. This boosts the performance for individual queries.
But this can lead to more queries being placed in a queue, which lowers the performance for those queries.
