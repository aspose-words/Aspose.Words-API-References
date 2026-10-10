---
title: "Metodo Aspose::Words::AI::AiModel::get_Timeout"
linktitle: "get_Timeout"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::AI::AiModel::get_Timeout. Ottiene o imposta il numero di millisecondi da attendere prima che la richiesta al modello AI scada. Il valore predefinito è 100.000 millisecondi (100 secondi) in C++."
type: docs
weight: 2667
url: /it/cpp/aspose.words.ai/aimodel/get_timeout/
---
## AiModel::get_Timeout method


Ottiene o imposta il numero di millisecondi da attendere prima che la richiesta al modello [AI](../../) scada. Il valore predefinito è 100.000 millisecondi (100 secondi).

```cpp
int32_t Aspose::Words::AI::AiModel::get_Timeout() const
```


## Esempi



Mostra come modificare il timeout predefinito del modello.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Valore predefinito 100000ms.
model->set_Timeout(250000);
```

## Vedi anche

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
