---
title: "Aspose::Words::AI::AiModel::get_Url Methode"
linktitle: "get_Url"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::AI::AiModel::get_Url Methode. Ruft die URL des Modells ab oder legt sie fest. Der Standardwert ist modellabhängig in C++."
type: docs
weight: 2834
url: /de/cpp/aspose.words.ai/aimodel/get_url/
---
## AiModel::get_Url method


Liest oder setzt die URL des Modells. Der Standardwert ist modellabhängig.

```cpp
virtual System::String Aspose::Words::AI::AiModel::get_Url()=0
```


## Beispiele



Zeigt, wie die Standard‑URL des Modells geändert wird.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Standardwert "https://api.openai.com/".
model->set_Url(u"https://my.a.com/");
```

## Siehe auch

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
