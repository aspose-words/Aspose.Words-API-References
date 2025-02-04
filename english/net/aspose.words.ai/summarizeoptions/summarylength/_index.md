---
title: SummarizeOptions.SummaryLength
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: Aspose.Words for .NET
description: SummarizeOptions SummaryLength property. Allows to specify summary length. Default value is Medium in C#.
type: docs
weight: 20
url: /net/aspose.words.ai/summarizeoptions/summarylength/
---
## SummarizeOptions.SummaryLength property

Allows to specify summary length. Default value is Medium.

```csharp
public SummaryLength SummaryLength { get; set; }
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

* enum [SummaryLength](../../summarylength/)
* class [SummarizeOptions](../)
* namespace [Aspose.Words.AI](../../../aspose.words.ai/)
* assembly [Aspose.Words](../../../)
