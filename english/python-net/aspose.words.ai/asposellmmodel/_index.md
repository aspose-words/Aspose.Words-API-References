---
title: AsposeLlmModel class
linktitle: AsposeLlmModel class
articleTitle: AsposeLlmModel class
second_title: Aspose.Words for Python
description: "aspose.words.ai.AsposeLlmModel class. Provides AI-powered document processing backed by Aspose.LLM - an on-premise LLM inference engine that runs entirely inside the current process, so document content never leaves the machine."
type: docs
weight: 40
url: /python-net/aspose.words.ai/asposellmmodel/
---

## AsposeLlmModel class

Provides AI-powered document processing backed by Aspose.LLM - an on-premise LLM inference engine
that runs entirely inside the current process, so document content never leaves the machine.


### Remarks

Unlike [OpenAiModel](../openaimodel/) / [GoogleAiModel](../googleaimodel/) / the Anthropic models, this class never
performs an HTTP request.


Aspose.LLM is not a dependency of Aspose.Words. To use this class, install the Aspose.LLM package
(version 26.6.0 or higher) into your project, so that Aspose.LLM.dll is placed next to Aspose.Words.dll.
If it cannot be loaded, the first call to the model throws System.InvalidOperationException.


Aspose.LLM has its own license, separate from the Aspose.Words license. You should set it directly,
the same way as for any other Aspose product, for example:
```

new Aspose.LLM.License().SetLicense("Aspose.Total.lic");

```

This class does not manage that license itself.

The native runtime and the model weights are downloaded by Aspose.LLM on the first request.

Every request is sent in its own chat session, so requests do not affect each other.




**Inheritance:** [AsposeLlmModel](./) → [AiModel](../aimodel/)

### Constructors
| Name | Description |
| --- | --- |
| [AsposeLlmModel(preset_name)](./__init__/#str) | Initializes a new instance of the [AsposeLlmModel](./) class for a specified Aspose.LLM preset. |

### Properties

| Name | Description |
| --- | --- |
| [timeout](../aimodel/timeout/) | Gets or sets the number of milliseconds to wait before the request to AI model times out. The default value is 100,000 milliseconds (100 seconds).<br>(Inherited from [AiModel](../aimodel/)) |
| [url](./url/) | Not used: [AsposeLlmModel](./) runs inference in-process against a local model, so there is no remote endpoint to address. Present only to satisfy the [AiModel](../aimodel/) contract. |

### Methods

| Name | Description |
| --- | --- |
|[ check_grammar(source_document, options)](../aimodel/check_grammar/#document_checkgrammaroptions) | Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document.<br>(Inherited from [AiModel](../aimodel/)) |
|[ create(model_type)](../aimodel/create/#aimodeltype) | Creates a new instance of [AiModel](../aimodel/) class.<br>(Inherited from [AiModel](../aimodel/)) |
|[ summarize(source_document, options)](./summarize/#document_summarizeoptions) | Generates a summary of the specified document, with options to adjust the length of the summary. |
|[ summarize(source_documents, options)](./summarize/#documentlist_summarizeoptions) | Generates a summary for an array of documents, with options to adjust the length of the summary. |
|[ translate(source_document, target_language)](./translate/#document_language) | Translates the provided document into the specified target language. |
|[ with_api_key(api_key)](../aimodel/with_api_key/#str) | Sets a specified API key to the model.<br>(Inherited from [AiModel](../aimodel/)) |

### See Also

* module [aspose.words.ai](../)
* class [AiModel](../aimodel/)

