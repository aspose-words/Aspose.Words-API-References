---
title: AiModelType Enum
linktitle: AiModelType
articleTitle: AiModelType
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.AI.AiModelType enum for seamless integration of AI models in document processing, enhancing efficiency and productivity.
type: docs
weight: 30
url: /net/aspose.words.ai/aimodeltype/
---
## AiModelType enumeration

Represents the types of [`AiModel`](../aimodel/) that can be integrated into the document processing workflow.

```csharp
public enum AiModelType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Gpt4O | `0` | GPT-4o generative model type. |
| Gpt4OMini | `1` | GPT-4o mini generative model type. |
| Gpt4Turbo | `2` | GPT-4 Turbo generative model type. |
| Gpt35Turbo | `3` | GPT-3.5 Turbo generative model type. |
| GeminiFlashLatest | `4` | Gemini Flash latest release generative model type. |
| GeminiProLatest | `6` | Gemini Pro latest release generative model type. |
| Claude35Sonnet | `7` | Claude 3.5 Sonnet generative model type. |
| Claude35Haiku | `8` | Claude 3.5 Haiku generative model type. |
| Claude3Opus | `9` | Claude 3 Opus generative model type. |
| Claude3Sonnet | `10` | Claude 3 Sonnet generative model type. |
| Claude3Haiku | `11` | Claude 3 Haiku generative model type. |

## Remarks

This enumeration is used to define which large language model (LLM) should be utilized for tasks such as summarization, translation, and content generation.

## Examples

Shows how to summarize text using OpenAI and Google models.

```csharp
Document firstDoc = new Document(MyDir + "Big document.docx");
Document secondDoc = new Document(MyDir + "Document.docx");

string apiKey = Environment.GetEnvironmentVariable("API_KEY");
// Use OpenAI or Google generative language models.
AiModel model = ((OpenAiModel)AiModel.Create(AiModelType.Gpt4OMini).WithApiKey(apiKey)).WithOrganization("Organization").WithProject("Project");

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
