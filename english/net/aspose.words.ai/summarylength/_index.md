---
title: SummaryLength Enum
linktitle: SummaryLength
articleTitle: SummaryLength
second_title: Aspose.Words for .NET
description: Aspose.Words.AI.SummaryLength enum. Enumerates possible lengths of summary in C#.
type: docs
weight: 90
url: /net/aspose.words.ai/summarylength/
---
## SummaryLength enumeration

Enumerates possible lengths of summary.

```csharp
public enum SummaryLength
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| VeryShort | `0` | Try to generate 1-2 sentences. |
| Short | `1` | Try to generate 3-4 sentences. |
| Medium | `2` | Try to generate 5-6 sentences. |
| Long | `3` | Try to generate 7-10 sentences. |
| VeryLong | `4` | Try to generate 11-20 sentences. |

## Examples

Shows how to summarize text using OpenAI and Google models.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Use OpenAI or Google generative language models.
IAiModelText model = (IAiModelText)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey);

Document oneDocumentSummary = model.Summarize(firstDoc, new SummarizeOptions() { SummaryLength = SummaryLength.Short });
oneDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.One.docx");

Document multiDocumentSummary = model.Summarize(new Document[] { firstDoc, secondDoc }, new SummarizeOptions() { SummaryLength = SummaryLength.Long });
multiDocumentSummary.Save(ArtifactsDir + "AI.AiSummarize.Multi.docx");
```

### See Also

* namespace [Aspose.Words.AI](../../aspose.words.ai/)
* assembly [Aspose.Words](../../)
