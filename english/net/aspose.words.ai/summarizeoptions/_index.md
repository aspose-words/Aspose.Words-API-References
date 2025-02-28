---
title: SummarizeOptions Class
linktitle: SummarizeOptions
articleTitle: SummarizeOptions
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.AI.SummarizeOptions class to customize and enhance your document summarization for clearer insights and improved content management.
type: docs
weight: 100
url: /net/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class

Allows to specify various options for summarizing document content.

```csharp
public class SummarizeOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [SummarizeOptions](summarizeoptions/)() | Initializes a new instances of `SummarizeOptions` class. |

## Properties

| Name | Description |
| --- | --- |
| [SummaryLength](../../aspose.words.ai/summarizeoptions/summarylength/) { get; set; } | Allows to specify summary length. Default value is Medium. |

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

* namespace [Aspose.Words.AI](../../aspose.words.ai/)
* assembly [Aspose.Words](../../)
