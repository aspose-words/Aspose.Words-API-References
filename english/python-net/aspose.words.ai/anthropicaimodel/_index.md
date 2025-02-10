---
title: AnthropicAiModel class
linktitle: AnthropicAiModel class
articleTitle: AnthropicAiModel class
second_title: Aspose.Words for Python
description: "aspose.words.ai.AnthropicAiModel class. An abstract class representing the integration with Anthropic’s AI models within the Aspose.Words."
type: docs
weight: 30
url: /python-net/aspose.words.ai/anthropicaimodel/
---

## AnthropicAiModel class

An abstract class representing the integration with Anthropic’s AI models within the Aspose.Words.


**Inheritance:** [AnthropicAiModel](./) → [AiModel](../aimodel/)

**Interfaces:** [IAiModelText](../iaimodeltext/)

### Methods

| Name | Description |
| --- | --- |
|[ check_grammar(source_document, options)](../iaimodeltext/check_grammar/#document_checkgrammaroptions) | Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document.<br>(Inherited from [IAiModelText](../iaimodeltext/)) |
|[ create(model_type)](../aimodel/create/#aimodeltype) | Creates a new instance of [AiModel](../aimodel/) class.<br>(Inherited from [AiModel](../aimodel/)) |
|[ summarize(source_document, options)](../iaimodeltext/summarize/#document_summarizeoptions) | Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected AI model for content processing.<br>(Inherited from [IAiModelText](../iaimodeltext/)) |
|[ summarize(source_documents, options)](../iaimodeltext/summarize/#documentlist_summarizeoptions) | Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array.<br>(Inherited from [IAiModelText](../iaimodeltext/)) |
|[ translate(source_document, target_language)](../iaimodeltext/translate/#document_language) | Translates the provided document into the specified target language. This operation leverages the connected AI model for content translating.<br>(Inherited from [IAiModelText](../iaimodeltext/)) |
|[ with_api_key(api_key)](../aimodel/with_api_key/#str) | Sets a specified API key to the model.<br>(Inherited from [AiModel](../aimodel/)) |

### See Also

* module [aspose.words.ai](../)
* class [AiModel](../aimodel/)
* class [IAiModelText](../iaimodeltext/)

