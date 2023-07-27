# C# samples for Azure Cognitive Search at scale

This repository contains C# code samples that demonstrate scale-up strategies for Azure Cognitive Search.

If you want a code sample that deploys Cognitive Search into multiple regions for global availability, try this Bicep sample instead: [**azure-search-multiple-regions**](https://github.com/Azure-Samples/azure-search-multiple-regions).

## In this repository

| Sample | Description |
|--------|-------------|
| multiple-data-sources | This .NET Core console app uses Azure Cognitive Search indexers and the .NET SDK to import data from Azure Cosmos DB and Azure Blob storage, combing data from two sources into one search index. | 
| multiple-search-services | This Azure Cognitive Search sample shows you how to issue a single query across multiple search services and combine the results into a single page. This sample uses [Good Books data](https://github.com/zygmuntz/goodbooks-10k). |
| optimize-data-indexing | This .NET Core console app builds off of the code used in the Quickstart and uses the Azure Cognitive Search .NET SDK to create an index, and efficiently load it with documents. The app allows users to test various batch sizes to understand the optimal batch size and then demonstrates how to efficiently upload 100,000 documents to a search index. This is done by splitting the data into batches, and spinning up several threads to upload the documents. Any failures are monitored and then retried using the exponential backoff retry strategy. The index is modeled on a subset of the Hotels dataset, reduced for readability and comprehension. Index definition and documents are included in the code. |

## More resources

+ See [.NET samples in Azure Cognitive Search](https://learn.microsoft.com/azure/search/samples-dotnet) for a comprehensive list of all Azure Cognitive Search code samples that run on .NET.

+ See [Azure Cognitive Search documentation](https://learn.microsoft.com/azure/search) for product documentation.