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


An abstract class representing the integration with Anthropic’s [AI](../) models within the [Aspose.Words](../../aspose.words/).

```cpp
class AnthropicAiModel : public Aspose::Words::AI::AiModel,
                         public Aspose::Words::AI::IAiModelText
```

## Methods

| Method | Description |
| --- | --- |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Checks grammar of the provided document. This operation leverages the connected [AI](../) model for checking grammar of document. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Creates a new instance of [AiModel](../aimodel/) class. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Generates a summary of the specified document, with options to adjust the length of the summary. This operation leverages the connected [AI](../) model for content processing. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Generates summaries for an array of documents, with options to control the summary length and other settings. This method utilizes the connected [AI](../) model for processing each document in the array. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Translates the provided document into the specified target language. This operation leverages the connected [AI](../) model for content translating. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Sets a specified API key to the model. |
## See Also

* Class [AiModel](../aimodel/)
* Interface [IAiModelText](../iaimodeltext/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
