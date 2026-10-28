---
title: Aspose::Words::AI::AiModel::set_Url method
linktitle: set_Url
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::AiModel::set_Url method. Sets a URL of the model. The default value is specific for the model in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.ai/aimodel/set_url/
---
## AiModel::set_Url method


Sets a URL of the model. The default value is specific for the model.

```cpp
virtual void Aspose::Words::AI::AiModel::set_Url(System::String value)
```

## Examples


Shows how to change model default url.

```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = AiModel::Create(AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Default value "https://api.openai.com/".
model->set_Url(u"https://my.a.com/");
```
## See Also

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
