---
title: GoogleAiModel Class
linktitle: GoogleAiModel
articleTitle: GoogleAiModel
second_title: Aspose.Words for .NET
description: Unlock the power of Aspose.Words.AI.GoogleAiModel class to seamlessly integrate Google AI models, enhancing your document processing capabilities effortlessly.
type: docs
weight: 60
url: /net/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class

An abstract class representing the integration with Google’s AI models within the Aspose.Words.

```csharp
public abstract class GoogleAiModel : AiModel, IAiModelText
```

## Methods

| Name | Description |
| --- | --- |
| virtual [CheckGrammar](../../aspose.words.ai/aimodel/checkgrammar/)(*[Document](../../aspose.words/document/), [CheckGrammarOptions](../checkgrammaroptions/)*) | Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document. |
| override [Summarize](../../aspose.words.ai/googleaimodel/summarize/#summarize)(*[Document](../../aspose.words/document/), [SummarizeOptions](../summarizeoptions/)*) | Summarizes specified [`Document`](../../aspose.words/document/) object. |
| override [Summarize](../../aspose.words.ai/googleaimodel/summarize/#summarize_1)(*Document[], [SummarizeOptions](../summarizeoptions/)*) | Summarizes specified [`Document`](../../aspose.words/document/) objects. |
| override [Translate](../../aspose.words.ai/googleaimodel/translate/)(*[Document](../../aspose.words/document/), [Language](../language/)*) | Translates a specified document. |
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

* class [AiModel](../aimodel/)
* namespace [Aspose.Words.AI](../../aspose.words.ai/)
* assembly [Aspose.Words](../../)
