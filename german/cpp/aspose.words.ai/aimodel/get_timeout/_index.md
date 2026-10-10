---
title: "Aspose::Words::AI::AiModel::get_Timeout Methode"
linktitle: "get_Timeout"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::AI::AiModel::get_Timeout Methode. Ruft die Anzahl Millisekunden ab oder legt sie fest, die gewartet werden sollen, bevor die Anfrage an das KI‑Modell abläuft. Der Standardwert beträgt 100.000 Millisekunden (100 Sekunden) in C++."
type: docs
weight: 2667
url: /de/cpp/aspose.words.ai/aimodel/get_timeout/
---
## AiModel::get_Timeout method


Ruft die Anzahl Millisekunden ab oder legt sie fest, die gewartet werden sollen, bevor die Anfrage an das [AI](../../) Modell abläuft. Der Standardwert beträgt 100.000 Millisekunden (100 Sekunden).

```cpp
int32_t Aspose::Words::AI::AiModel::get_Timeout() const
```


## Beispiele



Zeigt, wie die Standard‑Timeout‑Einstellung des Modells geändert wird.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Standardwert 100000 ms.
model->set_Timeout(250000);
```

## Siehe auch

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
