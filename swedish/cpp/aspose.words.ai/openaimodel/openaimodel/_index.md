---
title: "Aspose::Words::AI::OpenAiModel::OpenAiModel‑konstruktor"
linktitle: "OpenAiModel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::AI::OpenAiModel::OpenAiModel‑konstruktor. Initierar en ny instans av OpenAiModel‑klassen i C++."
type: docs
weight: 1334
url: /sv/cpp/aspose.words.ai/openaimodel/openaimodel/
---
## OpenAiModel::OpenAiModel(const System::String\&) constructor


Initierar en ny instans av klassen [OpenAiModel](../).

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| namn | const System::String\& | Namnet på modellen. Till exempel, gpt-5.2-chat-latest. |

## Se även

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## OpenAiModel::OpenAiModel(const System::String\&, const System::String\&) constructor


Initierar en ny instans av klassen [OpenAiModel](../).

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name, const System::String &apiKey)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| namn | const System::String\& | Namnet på modellen. Till exempel, gpt-5.2-chat-latest. |
| apiKey | const System::String\& | API‑nyckeln för att använda OpenAi‑API:t. |

## Exempel



Visar hur man skapar en OpenAI‑modelinstans direkt med en API‑nyckel och modellnamn.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Skapa en OpenAI‑modelinstans med hjälp av konstruktorn med modellnamn och API‑nyckel.
auto model = System::MakeObject<Aspose::Words::AI::OpenAiModel>(u"gpt-4o-mini", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
// Sammanfatta dokumentet med OpenAI‑modellen med kort sammanfattningslängd.
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);

summary->Save(get_ArtifactsDir() + u"OpenAiModel.OpenAiModelConstructor.docx");
```

## Se även

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
