---
title: "Constructor GoogleAiModel de Aspose::Words::AI::GoogleAiModel"
linktitle: "GoogleAiModel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Constructor GoogleAiModel de Aspose::Words::AI::GoogleAiModel. Inicializa una nueva instancia de la clase GoogleAiModel en C++."
type: docs
weight: 1500
url: /es/cpp/aspose.words.ai/googleaimodel/googleaimodel/
---
## GoogleAiModel::GoogleAiModel(const System::String\&) constructor


Inicializa una nueva instancia de la clase [GoogleAiModel](../).

```cpp
Aspose::Words::AI::GoogleAiModel::GoogleAiModel(const System::String &name)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | const System::String\& | El nombre del modelo. Por ejemplo, gemini-2.5-flash. |

## Ejemplos



Muestra cómo usar el modelo [AI](../../) de Google.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## Ver también

* Class [GoogleAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## GoogleAiModel::GoogleAiModel(const System::String\&, const System::String\&) constructor


Inicializa una nueva instancia de la clase [GoogleAiModel](../).

```cpp
Aspose::Words::AI::GoogleAiModel::GoogleAiModel(const System::String &name, const System::String &apiKey)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | const System::String\& | El nombre del modelo. Por ejemplo, gemini-2.5-flash. |
| apiKey | const System::String\& | La clave API para usar la API Gemini. Por favor, consulte [https://ai.google.dev/gemini-api/docs/api-key](https://ai.google.dev/gemini-api/docs/api-key) para más detalles. |

## Ejemplos



Muestra cómo usar el modelo [AI](../../) de Google.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## Ver también

* Class [GoogleAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
