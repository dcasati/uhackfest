# Azure Cosmos DB Hackfest

## Issues
1. Scale
2. Data Structures
3. Global Scale
4. Latencies
5. Consistency Models
6. Cost

## Factors
	1. Partition Key: as RU's are spread across partitions evenly, hot partitions can become an issue; if that happens, then RU's should be provisioned for peak hot partition, resulting in wasted RU's across ancillary partitions.
	2. Consistency Models: lower tiers of consistency can equate to 50% reduction in throughput needs.
	3. Result Sets: size of results can impact throughput needs (minimize)
	4. Index: Data can be omitted from the index; which requires less computation on write

## Help
	1. Official Docs: https://www.gotcosmos.com/
	2. Playground: https://www.documentdb.com/sql/demo
	3. Free: https://azure.microsoft.com/en-us/try/cosmosdb/
	4. RU Calculator: https://www.documentdb.com/capacityplanner
	5. Indexing Policy: https://docs.microsoft.com/en-us/azure/cosmos-db/indexing-policies

### Information
In sizing for price I am taking the baseline of what the partner has given me. If they are comfortable with that, then we can look at specific queries against real/mock data to determine actual cost of execution. Which will help us get a better estimate of RU's through the response headers which show RU usage. We will also be able to determine a more focused partition key strategy and tune queries to make the most of the RU's.