---
title: "Costruttore GoogleAiModel di Aspose::Words::AI::GoogleAiModel"
linktitle: "GoogleAiModel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Costruttore GoogleAiModel di Aspose::Words::AI::GoogleAiModel. Inizializza una nuova istanza della classe GoogleAiModel in C++."
type: docs
weight: 1500
url: /it/cpp/aspose.words.ai/googleaimodel/googleaimodel/
---
## GoogleAiModel::GoogleAiModel(const System::String\&) constructor


Inizializza una nuova istanza della classe [GoogleAiModel](../).

```cpp
Aspose::Words::AI::GoogleAiModel::GoogleAiModel(const System::String &name)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | const System::String\& | Il nome del modello. Per esempio, gemini-2.5-flash. |

## Esempi



Mostra come utilizzare il modello [AI](../../) di Google.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## Vedi anche

* Class [GoogleAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## GoogleAiModel::GoogleAiModel(const System::String\&, const System::String\&) constructor


Inizializza una nuova istanza della classe [GoogleAiModel](../).

```cpp
Aspose::Words::AI::GoogleAiModel::GoogleAiModel(const System::String &name, const System::String &apiKey)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | const System::String\& | Il nome del modello. Per esempio, gemini-2.5-flash. |
| apiKey | const System::String\& | La chiave API per utilizzare l'API Gemini. Si prega di consultare [https://ai.google.dev/gemini-api/docs/api-key](https://ai.google.dev/gemini-api/docs/api-key) per i dettagli. |

## Esempi



Mostra come utilizzare il modello [AI](../../) di Google.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## Vedi anche

* Class [GoogleAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
