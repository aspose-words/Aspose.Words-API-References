---
title: SummarizeOptions
linktitle: SummarizeOptions
articleTitle: SummarizeOptions
second_title: Aspose.Words for .NET
description: SummarizeOptions constructor. Initializes a new instances of SummarizeOptions class in C#.
type: docs
weight: 10
url: /net/aspose.words.ai/summarizeoptions/summarizeoptions/
---
## SummarizeOptions constructor

Initializes a new instances of [`SummarizeOptions`](../) class.

```csharp
public SummarizeOptions()
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

* class [SummarizeOptions](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)
