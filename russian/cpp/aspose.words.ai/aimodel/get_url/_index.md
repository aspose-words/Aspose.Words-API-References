---
title: "Метод Aspose::Words::AI::AiModel::get_Url"
linktitle: "get_Url"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::AI::AiModel::get_Url. Получает или задает URL модели. Значение по умолчанию специфично для модели на C++."
type: docs
weight: 2834
url: /ru/cpp/aspose.words.ai/aimodel/get_url/
---
## AiModel::get_Url method


Получает или задает URL модели. Значение по умолчанию специфично для модели.

```cpp
virtual System::String Aspose::Words::AI::AiModel::get_Url()=0
```


## Примеры



Показывает, как изменить URL модели по умолчанию.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Значение по умолчанию "https://api.openai.com/".
model->set_Url(u"https://my.a.com/");
```

## См. также

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
