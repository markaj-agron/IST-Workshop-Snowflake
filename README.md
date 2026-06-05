
# Characteristics

## Data Storage

- Support structured, semi-structured and unstructured data
- Native support for JSON, Avro, ORC, Parquet, and XML
- Data is automatically compressed and stored in cloud object storage
- Uses micro-partitioning for efficient storage and query performance
- Separation of storage and compute

## Querying

- Standard ANSI SQL
- ACID-compliant transactions
- Built-in support for analytics, ETL, data warehousing and data sharing

## Scalability

- Compute resources are organized into Virtual Warehouses
- Warehouses can be scaled up (more resources) or scaled out (multi-cluster)
- Independent scaling of storage and compute
- Automatic suspend and resume to reduce costs

## Concurrency

- Multiple Virtual Warehouse can access the same data simultaneously
- Supports high query concurrency with minimal contention
- Multi-cluster warehouses can automatically add compute resources during peak demand
- Concurrency can be tuned through warehouse configuration parameters

## Versioning & Recovery

- Time Travel allows access to historical versions of data
- Supports recovery of deleted or modified data
- Fail-safe provides an additional recovery period managed by Snowflake

## Data Sharing

- Secure data sharing without copying data
- Cross-account and cross-cloud sharing supported
- Supports data marketplaces and collaboration between organizations
