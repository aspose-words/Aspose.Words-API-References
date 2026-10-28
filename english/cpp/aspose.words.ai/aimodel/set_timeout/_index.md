---
title: Aspose::Words::AI::AiModel::set_Timeout method
linktitle: set_Timeout
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::AiModel::set_Timeout method. Sets the number of milliseconds to wait before the request to AI model times out. The default value is 100,000 milliseconds (100 seconds) in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.ai/aimodel/set_timeout/
---
## AiModel::set_Timeout method


Sets the number of milliseconds to wait before the request to AI model times out. The default value is 100,000 milliseconds (100 seconds).

```cpp
void Aspose::Words::AI::AiModel::set_Timeout(int32_t value)
```

## Examples


Shows how to change model default timeout.

```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = AiModel::Create(AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Default value 100000ms.
model->set_Timeout(250000);
```
## See Also

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
