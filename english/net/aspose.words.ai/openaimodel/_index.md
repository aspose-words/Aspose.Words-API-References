---
title: OpenAiModel Class
linktitle: OpenAiModel
articleTitle: OpenAiModel
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.AI.OpenAiModel class—your gateway to seamless integration with OpenAI's powerful language models for enhanced document processing.
type: docs
weight: 90
url: /net/aspose.words.ai/openaimodel/
---
## OpenAiModel class

An abstract class representing the integration with OpenAI's large language models within the Aspose.Words.

```csharp
public abstract class OpenAiModel : AiModel, IAiModelText
```

## Methods

| Name | Description |
| --- | --- |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Sets a specified API key to the model. |
| [WithOrganization](../../aspose.words.ai/openaimodel/withorganization/)(*string*) | Sets a specified Organization to the model. |
| [WithProject](../../aspose.words.ai/openaimodel/withproject/)(*string*) | Sets a specified Project to the model. |

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

* class [AiModel](../aimodel/)
* interface [IAiModelText](../iaimodeltext/)
* namespace [Aspose.Words.AI](../../aspose.words.ai/)
* assembly [Aspose.Words](../../)
