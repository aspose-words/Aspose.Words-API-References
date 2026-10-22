---
title: aspose.words.ai module
linktitle: aspose.words.ai module
articleTitle: aspose.words.ai module
second_title: Aspose.Words for Python
description: "The Aspose.Words.AI namespace provides seamless integration with large language models (LLMs) for AI-powered document processing"
type: docs
weight: 20
url: /python-net/aspose.words.ai/
---

The **Aspose.Words.AI** namespace provides seamless integration with large language models (LLMs)
for AI-powered document processing. It supports AI models from providers such as OpenAI, Google Gemini,
and Anthropic, as well as on-premise LLM inference through Aspose.LLM.

Classes within this namespace allow to leverage advanced AI capabilities to perform tasks such as
summarizing, translating, checking grammar, and analyzing the content of documents loaded into Aspose.Words.

Both cloud-based and on-premise AI models can be used to extend document automation workflows,
enabling efficient and high-quality text processing while providing flexibility in how document content
is processed and where it is hosted.




## Classes

| Class | Description |
| --- | --- |
| [AiModel](./aimodel/) | An abstract class representing the integration with various AI models within the Aspose.Words. |
| [AnthropicAiModel](./anthropicaimodel/) | An abstract class representing the integration with Anthropic’s AI models within the Aspose.Words. |
| [AsposeLlmModel](./asposellmmodel/) | Provides AI-powered document processing backed by Aspose.LLM - an on-premise LLM inference engine that runs entirely inside the current process, so document content never leaves the machine. |
| [CheckGrammarOptions](./checkgrammaroptions/) | Allows to specify various options while checking grammar of a document using AI. |
| [GoogleAiModel](./googleaimodel/) | Class representing Google AI Models (Gemini) integration within Aspose.Words. |
| [OpenAiModel](./openaimodel/) | Class representing OpenAi models integration within Aspose.Words. |
| [SummarizeOptions](./summarizeoptions/) | Allows to specify various options for summarizing document content. |

## Enumerations

| Enumeration | Description |
| --- | --- |
| [AiModelType](./aimodeltype/) | Represents the types of [AiModel](./aimodel/) that can be integrated into the document processing workflow. |
| [Language](./language/) | Specifies the language into which the text will be translated using AI. . |
| [SummaryLength](./summarylength/) | Enumerates possible lengths of summary. |

