---
title: AiModel Class
linktitle: AiModel
articleTitle: AiModel
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.AI.AiModel class, your key to leveraging advanced Generative Language Models for enhanced text generation and automation.
type: docs
weight: 20
url: /net/aspose.words.ai/aimodel/
---
## AiModel class

An abstract class representing the integration with various AI models within the Aspose.Words.

```csharp
public abstract class AiModel
```

## Methods

| Name | Description |
| --- | --- |
| static [Create](../../aspose.words.ai/aimodel/create/)(*[AiModelType](../aimodeltype/)*) | Creates a new instance of `AiModel` class. |
| virtual [CheckGrammar](../../aspose.words.ai/aimodel/checkgrammar/)(*[Document](../../aspose.words/document/), [CheckGrammarOptions](../checkgrammaroptions/)*) | Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document. |
| abstract [Summarize](../../aspose.words.ai/aimodel/summarize/#summarize)(*[Document](../../aspose.words/document/), [SummarizeOptions](../summarizeoptions/)*) | Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected AI model for content processing. |
| abstract [Summarize](../../aspose.words.ai/aimodel/summarize/#summarize_1)(*Document[], [SummarizeOptions](../summarizeoptions/)*) | Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array. |
| abstract [Translate](../../aspose.words.ai/aimodel/translate/)(*[Document](../../aspose.words/document/), [Language](../language/)*) | Translates the provided document into the specified target language. This operation leverages the connected AI model for content translating. |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Sets a specified API key to the model. |

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
