---
title: "Aspose::Words::AI::AiModel::get_Url yöntemi"
linktitle: "get_Url"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::AI::AiModel::get_Url yöntemi. Modelin URL'sini alır veya ayarlar. Varsayılan değer, C++'ta modele özgüdür."
type: docs
weight: 2834
url: /tr/cpp/aspose.words.ai/aimodel/get_url/
---
## AiModel::get_Url method


Modelin URL'sini alır veya ayarlar. Varsayılan değer model için özeldir.

```cpp
virtual System::String Aspose::Words::AI::AiModel::get_Url()=0
```


## Örnekler



Modelin varsayılan URL'sinin nasıl değiştirileceğini gösterir.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Varsayılan değer "https://api.openai.com/".
model->set_Url(u"https://my.a.com/");
```

## Ayrıca Bakınız

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
