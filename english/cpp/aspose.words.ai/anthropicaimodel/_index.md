---
title: Aspose::Words::AI::AnthropicAiModel class
linktitle: AnthropicAiModel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::AnthropicAiModel class. An abstract class representing the integration with Anthropic’s AI models within the Aspose.Words in C++.'
type: docs
weight: 1250
url: /cpp/aspose.words.ai/anthropicaimodel/
---
## AnthropicAiModel class


An abstract class representing the integration with Anthropic’s AI models within the Aspose.Words.

```cpp
class AnthropicAiModel : public AiModel
```

## Methods

| Method | Description |
| --- | --- |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array. |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected AI model for content processing. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Translates the provided document into the specified target language. This operation leverages the connected AI model for content translating. |
| [get_Url](./get_url/)() override | Gets or sets a URL of the model. The default value is "https://api.anthropic.com/". |
| [set_Url](./set_url/)(System::String) override | Sets a URL of the model. The default value is "https://api.anthropic.com/". |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Checks grammar of the provided document. This operation leverages the connected AI model for checking grammar of document. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Creates a new instance of [AiModel](../aimodel/) class. |
| virtual [Summarize](../aimodel/summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected AI model for processing each document in the array. |
| virtual [Summarize](../aimodel/summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected AI model for content processing. |
| virtual [Translate](../aimodel/translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) | Translates the provided document into the specified target language. This operation leverages the connected AI model for content translating. |
| [WithApiKey](../aimodel/withapikey/)(const System::String \&) | Sets a specified API key to the model. |
| [get_Timeout](../aimodel/get_timeout/)() const | Gets or sets the number of milliseconds to wait before the request to AI model times out. The default value is 100,000 milliseconds (100 seconds). |
| virtual [get_Url](../aimodel/get_url/)() | Gets or sets a URL of the model. The default value is specific for the model. |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Sets the number of milliseconds to wait before the request to AI model times out. The default value is 100,000 milliseconds (100 seconds). |
| virtual [set_Url](../aimodel/set_url/)(System::String) | Sets a URL of the model. The default value is specific for the model. |
## See Also

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
