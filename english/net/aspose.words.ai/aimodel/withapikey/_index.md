---
title: AiModel.WithApiKey
linktitle: WithApiKey
articleTitle: WithApiKey
second_title: Aspose.Words for .NET
description: AiModel WithApiKey method. Sets a specified API key to the model in C#.
type: docs
weight: 20
url: /net/aspose.words.ai/aimodel/withapikey/
---
## AiModel.WithApiKey method

Sets a specified API key to the model.

```csharp
public AiModel WithApiKey(string apiKey)
```

## Examples

Shows how to summarize text using OpenAI and Google models.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Use OpenAI or Google generative language models.
IAiModelText model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

SummarizeOptions options = new SummarizeOptions();

options.SummaryLength = SummaryLength.Short;
Document oneDocumentSummary = model.Summarize(firstDoc, options);
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

options.SummaryLength = SummaryLength.Long;
Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, options);
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### See Also

* class [AiModel](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)
