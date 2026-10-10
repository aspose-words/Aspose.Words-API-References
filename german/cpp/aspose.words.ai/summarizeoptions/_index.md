---
title: "Aspose::Words::AI::SummarizeOptions Klasse"
linktitle: "SummarizeOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::AI::SummarizeOptions Klasse. Ermöglicht die Angabe verschiedener Optionen zum Zusammenfassen von Dokumentinhalten in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class


Ermöglicht das Festlegen verschiedener Optionen zum Zusammenfassen von Dokumentinhalten.

```cpp
class SummarizeOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_SummaryLength](./get_summarylength/)() const | Ermöglicht die Angabe der Zusammenfassungslänge. Standardwert ist [Medium](../summarylength/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SummaryLength](./set_summarylength/)(Aspose::Words::AI::SummaryLength) | Setter für [Aspose::Words::AI::SummarizeOptions::get_SummaryLength](./get_summarylength/). |
| [SummarizeOptions](./summarizeoptions/)() | Initialisiert eine neue Instanz der [SummarizeOptions](./) Klasse. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man Text mit OpenAI‑ und Google‑Modellen zusammenfasst.
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Verwenden Sie generative Sprachmodelle von OpenAI oder Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```

## Siehe auch

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
