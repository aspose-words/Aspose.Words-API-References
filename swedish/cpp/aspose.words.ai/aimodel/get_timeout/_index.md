---
title: "Aspose::Words::AI::AiModel::get_Timeout‑metod"
linktitle: "get_Timeout"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::AI::AiModel::get_Timeout‑metod. Hämtar eller anger antalet millisekunder att vänta innan begäran till AI‑modellen tidsöverskrider. Standardvärdet är 100 000 millisekunder (100 sekunder) i C++."
type: docs
weight: 2667
url: /sv/cpp/aspose.words.ai/aimodel/get_timeout/
---
## AiModel::get_Timeout method


Hämtar eller anger antalet millisekunder att vänta innan begäran till [AI](../../)‑modellen tidsöverskrider. Standardvärdet är 100 000 millisekunder (100 sekunder).

```cpp
int32_t Aspose::Words::AI::AiModel::get_Timeout() const
```


## Exempel



Visar hur man ändrar modellens standard‑timeout.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Standardvärde 100000 ms.
model->set_Timeout(250000);
```

## Se även

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
