---
title: "Aspose::Words::AI::AiModel::get_Url‑metod"
linktitle: "get_Url"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::AI::AiModel::get_Url‑metod. Hämtar eller anger en URL för modellen. Standardvärdet är specifikt för modellen i C++."
type: docs
weight: 2834
url: /sv/cpp/aspose.words.ai/aimodel/get_url/
---
## AiModel::get_Url method


Hämtar eller anger en URL för modellen. Standardvärdet är specifikt för modellen.

```cpp
virtual System::String Aspose::Words::AI::AiModel::get_Url()=0
```


## Exempel



Visar hur man ändrar modellens standard‑URL.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Standardvärde "https://api.openai.com/".
model->set_Url(u"https://my.a.com/");
```

## Se även

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
