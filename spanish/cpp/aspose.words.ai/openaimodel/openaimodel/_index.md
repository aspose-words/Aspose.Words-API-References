---
title: "Constructor Aspose::Words::AI::OpenAiModel::OpenAiModel"
linktitle: "OpenAiModel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::AI::OpenAiModel::OpenAiModel constructor. Inicializa una nueva instancia de la clase OpenAiModel en C++."
type: docs
weight: 1334
url: /es/cpp/aspose.words.ai/openaimodel/openaimodel/
---
## OpenAiModel::OpenAiModel(const System::String\&) constructor


Inicializa una nueva instancia de la clase [OpenAiModel](../).

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | const System::String\& | El nombre del modelo. Por ejemplo, gpt-5.2-chat-latest. |

## Ver también

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## OpenAiModel::OpenAiModel(const System::String\&, const System::String\&) constructor


Inicializa una nueva instancia de la clase [OpenAiModel](../).

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name, const System::String &apiKey)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | const System::String\& | El nombre del modelo. Por ejemplo, gpt-5.2-chat-latest. |
| apiKey | const System::String\& | La clave API para usar la API de OpenAi. |

## Ejemplos



Muestra cómo crear una instancia de modelo OpenAI directamente usando una clave API y el nombre del modelo.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Crea una instancia de modelo OpenAI usando el constructor con el nombre del modelo y la clave API.
auto model = System::MakeObject<Aspose::Words::AI::OpenAiModel>(u"gpt-4o-mini", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
// Resume el documento usando el modelo OpenAI con una longitud de resumen corta.
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);

summary->Save(get_ArtifactsDir() + u"OpenAiModel.OpenAiModelConstructor.docx");
```

## Ver también

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
