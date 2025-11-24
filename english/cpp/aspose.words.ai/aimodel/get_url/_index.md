---
title: Aspose::Words::AI::AiModel::get_Url method
linktitle: get_Url
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::AI::AiModel::get_Url method. Gets or sets a URL of the model. The default value is specific for the model in C++.'
type: docs
weight: 2834
url: /cpp/aspose.words.ai/aimodel/get_url/
---
## AiModel::get_Url method


Gets or sets a URL of the model. The default value is specific for the model.

```cpp
virtual System::String Aspose::Words::AI::AiModel::get_Url()=0
```


## Examples



Shows how to change model default url. 
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Default value "https://api.openai.com/".
model->set_Url(u"https://my.a.com/");
```

## See Also

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
