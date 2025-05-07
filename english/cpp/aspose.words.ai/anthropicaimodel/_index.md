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
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Creates a new instance of [AiModel](../aimodel/) class. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Sets a specified API key to the model. |
## See Also

* Class [AiModel](../aimodel/)
* Interface [IAiModelText](../iaimodeltext/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
