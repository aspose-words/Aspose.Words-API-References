---
title: "Método Aspose::Words::AI::AiModel::get_Url"
linktitle: "get_Url"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::AI::AiModel::get_Url. Obtiene o establece una URL del modelo. El valor predeterminado es específico para el modelo en C++."
type: docs
weight: 2834
url: /es/cpp/aspose.words.ai/aimodel/get_url/
---
## AiModel::get_Url method


Obtiene o establece una URL del modelo. El valor predeterminado es específico para el modelo.

```cpp
virtual System::String Aspose::Words::AI::AiModel::get_Url()=0
```


## Ejemplos



Muestra cómo cambiar la URL predeterminada del modelo.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// Valor predeterminado "https://api.openai.com/".
model->set_Url(u"https://my.a.com/");
```

## Ver también

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
