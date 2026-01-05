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

Class representing Google AI Models (Gemini) integration within Aspose.Words.

```csharp
public class GoogleAiModel : AiModel
```

## Constructors

| Name | Description |
| --- | --- |
| [GoogleAiModel](googleaimodel/#constructor)(*string*) | Initializes a new instance of `GoogleAiModel` class. |
| [GoogleAiModel](googleaimodel/#constructor_1)(*string, string*) | Initializes a new instance of `GoogleAiModel` class. |

## Properties

| Name | Description |
| --- | --- |
| [Timeout](../../aspose.words.ai/aimodel/timeout/) { get; set; } | Gets or sets the number of milliseconds to wait before the request to AI model times out. The default value is 100,000 milliseconds (100 seconds). |
| override [Url](../../aspose.words.ai/googleaimodel/url/) { get; set; } | Gets or sets a URL of the model. The default value is "https://generativelanguage.googleapis.com/v1beta/models/". |

## Methods

| Name | Description |
| --- | --- |
| virtual [CheckGrammar](../../aspose.words.ai/aimodel/checkgrammar/)(*[Document](../../aspose.words/document/), [CheckGrammarOptions](../checkgrammaroptions/)*) | Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document. |
| override [Summarize](../../aspose.words.ai/googleaimodel/summarize/#summarize)(*[Document](../../aspose.words/document/), [SummarizeOptions](../summarizeoptions/)*) | Summarizes specified [`Document`](../../aspose.words/document/) object. |
| override [Summarize](../../aspose.words.ai/googleaimodel/summarize/#summarize_1)(*Document[], [SummarizeOptions](../summarizeoptions/)*) | Summarizes specified [`Document`](../../aspose.words/document/) objects. |
| override [Translate](../../aspose.words.ai/googleaimodel/translate/)(*[Document](../../aspose.words/document/), [Language](../language/)*) | Translates a specified document. |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Sets a specified API key to the model. |

## Remarks

Please refer to https://ai.google.dev/gemini-api/docs/models for Gemini models details.

## Examples

Shows how to use google AI model.

```csharp
string apiKey = Environment.GetEnvironmentVariable("API_KEY");
GoogleAiModel model = new GoogleAiModel("gemini-flash-latest", apiKey);

Document doc = new Document(MyDir + "Big document.docx");
SummarizeOptions summarizeOptions = new SummarizeOptions() { SummaryLength = SummaryLength.VeryShort };
Document summary = model.Summarize(doc, summarizeOptions);
```

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
