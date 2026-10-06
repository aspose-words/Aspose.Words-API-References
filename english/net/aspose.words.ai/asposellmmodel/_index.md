---
title: AsposeLlmModel Class
linktitle: AsposeLlmModel
articleTitle: AsposeLlmModel
second_title: Aspose.Words for .NET
description: Aspose.Words.AI.AsposeLlmModel class. Provides AIpowered document processing backed by Aspose.LLM  an onpremise LLM inference engine that runs entirely inside the current process so document content never leaves the machine.
type: docs
weight: 50
url: /net/aspose.words.ai/asposellmmodel/
---
## AsposeLlmModel class

Provides AI-powered document processing backed by Aspose.LLM - an on-premise LLM inference engine that runs entirely inside the current process, so document content never leaves the machine.

```csharp
public sealed class AsposeLlmModel : AiModel, IDisposable
```

## Constructors

| Name | Description |
| --- | --- |
| [AsposeLlmModel](asposellmmodel/)(*string*) | Initializes a new instance of the `AsposeLlmModel` class for a specified Aspose.LLM preset. |

## Properties

| Name | Description |
| --- | --- |
| [Timeout](../../aspose.words.ai/aimodel/timeout/) { get; set; } | Gets or sets the number of milliseconds to wait before the request to AI model times out. The default value is 100,000 milliseconds (100 seconds). |
| override [Url](../../aspose.words.ai/asposellmmodel/url/) { get; set; } | Not used: `AsposeLlmModel` runs inference in-process against a local model, so there is no remote endpoint to address. Present only to satisfy the [`AiModel`](../aimodel/) contract. |

## Methods

| Name | Description |
| --- | --- |
| virtual [CheckGrammar](../../aspose.words.ai/aimodel/checkgrammar/)(*[Document](../../aspose.words/document/), [CheckGrammarOptions](../checkgrammaroptions/)*) | Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document. |
| [Dispose](../../aspose.words.ai/asposellmmodel/dispose/)() | Releases the underlying Aspose.LLM model and its native resources. |
| override [Summarize](../../aspose.words.ai/asposellmmodel/summarize/#summarize)(*[Document](../../aspose.words/document/), [SummarizeOptions](../summarizeoptions/)*) | Generates a summary of the specified document, with options to adjust the length of the summary. |
| override [Summarize](../../aspose.words.ai/asposellmmodel/summarize/#summarize_1)(*Document[], [SummarizeOptions](../summarizeoptions/)*) | Generates a summary for an array of documents, with options to adjust the length of the summary. |
| override [Translate](../../aspose.words.ai/asposellmmodel/translate/)(*[Document](../../aspose.words/document/), [Language](../language/)*) | Translates the provided document into the specified target language. |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Sets a specified API key to the model. |

## Remarks

Unlike [`OpenAiModel`](../openaimodel/) / [`GoogleAiModel`](../googleaimodel/) / the Anthropic models, this class never performs an HTTP request.

Aspose.LLM is not a dependency of Aspose.Words. To use this class, install the Aspose.LLM package (version 26.6.0 or higher) into your project, so that Aspose.LLM.dll is placed next to Aspose.Words.dll. If it cannot be loaded, the first call to the model throws InvalidOperationException.

Aspose.LLM has its own license, separate from the Aspose.Words license. You should set it directly, the same way as for any other Aspose product, for example:

```csharp
new Aspose.LLM.License().SetLicense("Aspose.Total.lic");
```

This class does not manage that license itself.

The native runtime and the model weights are downloaded by Aspose.LLM on the first request.

Every request is sent in its own chat session, so requests do not affect each other.

### See Also

* class [AiModel](../aimodel/)
* namespace [Aspose.Words.AI](../../aspose.words.ai/)
* assembly [Aspose.Words](../../)
