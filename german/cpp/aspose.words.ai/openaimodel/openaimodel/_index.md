---
title: "Aspose::Words::AI::OpenAiModel::OpenAiModel-Konstruktor"
linktitle: "OpenAiModel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::AI::OpenAiModel::OpenAiModel-Konstruktor. Initialisiert eine neue Instanz der Klasse OpenAiModel in C++."
type: docs
weight: 1334
url: /de/cpp/aspose.words.ai/openaimodel/openaimodel/
---
## OpenAiModel::OpenAiModel(const System::String\&) constructor


Initialisiert eine neue Instanz der Klasse [OpenAiModel](../).

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | const System::String\& | Der Name des Modells. Zum Beispiel gpt-5.2-chat-latest. |

## Siehe auch

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## OpenAiModel::OpenAiModel(const System::String\&, const System::String\&) constructor


Initialisiert eine neue Instanz der Klasse [OpenAiModel](../).

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name, const System::String &apiKey)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | const System::String\& | Der Name des Modells. Zum Beispiel gpt-5.2-chat-latest. |
| apiKey | const System::String\& | Der API‑Schlüssel zur Verwendung der OpenAi-API. |

## Beispiele



Zeigt, wie man eine OpenAI‑Modelinstanz direkt mit einem API‑Schlüssel und Modellnamen erstellt.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Erstellen Sie eine OpenAI‑Modelinstanz mit dem Konstruktor unter Angabe von Modellnamen und API‑Schlüssel.
auto model = System::MakeObject<Aspose::Words::AI::OpenAiModel>(u"gpt-4o-mini", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
// Fassen Sie das Dokument mit dem OpenAI‑Modell bei kurzer Zusammenfassungslänge zusammen.
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);

summary->Save(get_ArtifactsDir() + u"OpenAiModel.OpenAiModelConstructor.docx");
```

## Siehe auch

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
