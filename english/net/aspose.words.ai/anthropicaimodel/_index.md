---
title: AnthropicAiModel Class
linktitle: AnthropicAiModel
articleTitle: AnthropicAiModel
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.AI.AnthropicAiModel class—your gateway to seamless integration with Anthropics AI models for enhanced document processing.
type: docs
weight: 40
url: /net/aspose.words.ai/anthropicaimodel/
---
## AnthropicAiModel class

An abstract class representing the integration with Anthropic’s AI models within the Aspose.Words.

```csharp
public abstract class AnthropicAiModel : AiModel, IAiModelText
```

## Methods

| Name | Description |
| --- | --- |
| virtual [CheckGrammar](../../aspose.words.ai/aimodel/checkgrammar/)(*[Document](../../aspose.words/document/), [CheckGrammarOptions](../checkgrammaroptions/)*) | Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document. |
| override [Summarize](../../aspose.words.ai/anthropicaimodel/summarize/#summarize)(*[Document](../../aspose.words/document/), [SummarizeOptions](../summarizeoptions/)*) | Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected AI model for content processing. |
| override [Summarize](../../aspose.words.ai/anthropicaimodel/summarize/#summarize_1)(*Document[], [SummarizeOptions](../summarizeoptions/)*) | Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array. |
| override [Translate](../../aspose.words.ai/anthropicaimodel/translate/)(*[Document](../../aspose.words/document/), [Language](../language/)*) | Translates the provided document into the specified target language. This operation leverages the connected AI model for content translating. |
| [WithApiKey](../../aspose.words.ai/aimodel/withapikey/)(*string*) | Sets a specified API key to the model. |

### See Also

* class [AiModel](../aimodel/)
* namespace [Aspose.Words.AI](../../aspose.words.ai/)
* assembly [Aspose.Words](../../)
