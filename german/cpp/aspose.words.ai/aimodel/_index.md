---
title: "Aspose::Words::AI::AiModel class"
linktitle: "AiModel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::AI::AiModel class. Eine abstrakte Klasse, die die Integration mit verschiedenen KI-Modellen innerhalb von Aspose.Words in C++ darstellt."
type: docs
weight: 1000
url: /de/cpp/aspose.words.ai/aimodel/
---
## AiModel class


Eine abstrakte Klasse, die die Integration mit verschiedenen [AI](../)-Modellen innerhalb von [Aspose.Words](../../aspose.words/) darstellt.

```cpp
class AiModel : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [CheckGrammar](./checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Überprüft die Grammatik des bereitgestellten Dokuments. Dieser Vorgang nutzt das verbundene [AI](../)-Modell zur Grammatikprüfung des Dokuments. |
| static [Create](./create/)(Aspose::Words::AI::AiModelType) | Erstellt eine neue Instanz der Klasse [AiModel](./). |
| [get_Timeout](./get_timeout/)() const | Liest oder setzt die Anzahl der Millisekunden, die gewartet werden, bevor die Anfrage an das [AI](../)-Modell abläuft. Der Standardwert beträgt 100.000 Millisekunden (100 Sekunden). |
| virtual [get_Url](./get_url/)() | Liest oder setzt die URL des Modells. Der Standardwert ist modellabhängig. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](./set_timeout/)(int32_t) | Setter für [Aspose::Words::AI::AiModel::get_Timeout](./get_timeout/). |
| virtual [set_Url](./set_url/)(System::String) | Setter für [Aspose::Words::AI::AiModel::get_Url](./get_url/). |
| virtual [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | Erstellt eine Zusammenfassung des angegebenen Dokuments, mit Optionen zur Anpassung der Länge der Zusammenfassung. Dieser Vorgang nutzt das verbundene [AI](../)-Modell zur Inhaltsverarbeitung. |
| virtual [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | Erstellt Zusammenfassungen für ein Array von Dokumenten, mit Optionen zur Steuerung der Zusammenfassungslänge und anderer Einstellungen. Diese Methode nutzt das verbundene [AI](../)-Modell zur Verarbeitung jedes Dokuments im Array. |
| virtual [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) | Übersetzt das bereitgestellte Dokument in die angegebene Zielsprache. Dieser Vorgang nutzt das verbundene [AI](../)-Modell zur Inhaltsübersetzung. |
| static [Type](./type/)() |  |
| [WithApiKey](./withapikey/)(const System::String\&) | Setzt einen angegebenen API-Schlüssel für das Modell. |

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
