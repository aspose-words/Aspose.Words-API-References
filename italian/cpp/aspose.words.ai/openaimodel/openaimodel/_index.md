---
title: "Costruttore Aspose::Words::AI::OpenAiModel::OpenAiModel"
linktitle: "OpenAiModel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Costruttore Aspose::Words::AI::OpenAiModel::OpenAiModel. Inizializza una nuova istanza della classe OpenAiModel in C++."
type: docs
weight: 1334
url: /it/cpp/aspose.words.ai/openaimodel/openaimodel/
---
## OpenAiModel::OpenAiModel(const System::String\&) constructor


Inizializza una nuova istanza della classe [OpenAiModel](../).

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | const System::String\& | Il nome del modello. Per esempio, gpt-5.2-chat-latest. |

## Vedi anche

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## OpenAiModel::OpenAiModel(const System::String\&, const System::String\&) constructor


Inizializza una nuova istanza della classe [OpenAiModel](../).

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name, const System::String &apiKey)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | const System::String\& | Il nome del modello. Per esempio, gpt-5.2-chat-latest. |
| apiKey | const System::String\& | La chiave API da utilizzare per l'API OpenAi. |

## Esempi



Mostra come creare un'istanza del modello OpenAI direttamente utilizzando una chiave API e il nome del modello.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Crea un'istanza del modello OpenAI usando il costruttore con il nome del modello e la chiave API.
auto model = System::MakeObject<Aspose::Words::AI::OpenAiModel>(u"gpt-4o-mini", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
// Riassumi il documento usando il modello OpenAI con una lunghezza di riepilogo breve.
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);

summary->Save(get_ArtifactsDir() + u"OpenAiModel.OpenAiModelConstructor.docx");
```

## Vedi anche

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
