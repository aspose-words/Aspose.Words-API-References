---
title: "Método Aspose::Words::AI::AiModel::get_Timeout"
linktitle: "get_Timeout"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::AI::AiModel::get_Timeout. Obtiene o establece el número de milisegundos a esperar antes de que la solicitud al modelo de IA expire. El valor predeterminado es 100 000 milisegundos (100 segundos) en C++."
type: docs
weight: 2667
url: /es/cpp/aspose.words.ai/aimodel/get_timeout/
---
## AiModel::get_Timeout method


Obtiene o establece el número de milisegundos a esperar antes de que la solicitud al modelo [AI](../../) expire. El valor predeterminado es 100 000 milisegundos (100 segundos).

```cpp
int32_t Aspose::Words::AI::AiModel::get_Timeout() const
```


## Ejemplos



Muestra cómo cambiar el tiempo de espera predeterminado del modelo.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Valor predeterminado 100000 ms.
model->set_Timeout(250000);
```

## Ver también

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
