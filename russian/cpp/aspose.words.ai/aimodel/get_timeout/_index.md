---
title: "Метод Aspose::Words::AI::AiModel::get_Timeout"
linktitle: "get_Timeout"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::AI::AiModel::get_Timeout. Получает или задает количество миллисекунд ожидания до истечения тайм‑аута запроса к AI‑модели. Значение по умолчанию — 100 000 миллисекунд (100 секунд) в C++."
type: docs
weight: 2667
url: /ru/cpp/aspose.words.ai/aimodel/get_timeout/
---
## AiModel::get_Timeout method


Получает или задает количество миллисекунд ожидания до истечения тайм‑аута запроса к модели [AI](../../). Значение по умолчанию — 100 000 миллисекунд (100 секунд).

```cpp
int32_t Aspose::Words::AI::AiModel::get_Timeout() const
```


## Примеры



Показывает, как изменить тайм‑аут модели по умолчанию.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Значение по умолчанию 100000 мс.
model->set_Timeout(250000);
```

## См. также

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
