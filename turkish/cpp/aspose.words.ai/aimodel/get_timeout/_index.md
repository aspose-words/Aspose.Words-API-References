---
title: "Aspose::Words::AI::AiModel::get_Timeout yöntemi"
linktitle: "get_Timeout"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::AI::AiModel::get_Timeout yöntemi. AI modeline yapılan isteğin zaman aşımına uğramadan önce beklenecek milisaniye sayısını alır veya ayarlar. Varsayılan değer C++'da 100.000 milisaniyedir (100 saniye)."
type: docs
weight: 2667
url: /tr/cpp/aspose.words.ai/aimodel/get_timeout/
---
## AiModel::get_Timeout method


İsteğin [AI](../../) modeline zaman aşımına uğramadan önce beklenecek milisaniye sayısını alır veya ayarlar. Varsayılan değer 100.000 milisaniyedir (100 saniye).

```cpp
int32_t Aspose::Words::AI::AiModel::get_Timeout() const
```


## Örnekler



Modelin varsayılan zaman aşımının nasıl değiştirileceğini gösterir.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Varsayılan değer 100000ms.
model->set_Timeout(250000);
```

## Ayrıca Bakınız

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
