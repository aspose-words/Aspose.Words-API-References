---
title: "Metodo Aspose::Words::AI::AiModel::get_Url"
linktitle: "get_Url"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::AI::AiModel::get_Url. Ottiene o imposta un URL del modello. Il valore predefinito è specifico per il modello in C++."
type: docs
weight: 2834
url: /it/cpp/aspose.words.ai/aimodel/get_url/
---
## AiModel::get_Url method


Ottiene o imposta un URL del modello. Il valore predefinito è specifico per il modello.

```cpp
virtual System::String Aspose::Words::AI::AiModel::get_Url()=0
```


## Esempi



Mostra come modificare l'URL predefinito del modello.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Valore predefinito "https://api.openai.com/".
model->set_Url(u"https://my.a.com/");
```

## Vedi anche

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
