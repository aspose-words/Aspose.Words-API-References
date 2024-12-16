---
title: Aspose::Words::AI::OpenAiModel class
linktitle: OpenAiModel
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::OpenAiModel class. An abstract class representing the integration with OpenAI''s large language models within the Aspose.Words in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.ai/openaimodel/
---
## OpenAiModel class


An abstract class representing the integration with OpenAI's large language models within the [Aspose.Words](../../aspose.words/).

```cpp
class OpenAiModel : public Aspose::Words::AI::AiModel,
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
| [WithOrganization](./withorganization/)(const System::String\&) | Sets a specified Organization to the model. |
| [WithProject](./withproject/)(const System::String\&) | Sets a specified Project to the model. |
## See Also

* Class [AiModel](../aimodel/)
* Interface [IAiModelText](../iaimodeltext/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
