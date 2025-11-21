---
title: Aspose::Words::AI::AiModel::get_Timeout method
linktitle: get_Timeout
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::AiModel::get_Timeout method. Gets or sets the number of milliseconds to wait before the request to AI model times out. The default value is 100,000 milliseconds (100 seconds) in C++.'
type: docs
weight: 2667
url: /cpp/aspose.words.ai/aimodel/get_timeout/
---
## AiModel::get_Timeout method


Gets or sets the number of milliseconds to wait before the request to [AI](../../) model times out. The default value is 100,000 milliseconds (100 seconds).

```cpp
int32_t Aspose::Words::AI::AiModel::get_Timeout() const
```


## Examples



Shows how to change model default timeout. 
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Default value 100000ms.
model->set_Timeout(250000);
```

## See Also

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
