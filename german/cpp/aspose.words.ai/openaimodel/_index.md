---
title: "Aspose::Words::AI::OpenAiModel class"
linktitle: "OpenAiModel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::AI::OpenAiModel class. Klasse, die die Integration von OpenAi-Modellen in Aspose.Words in C++ darstellt."
type: docs
weight: 3000
url: /de/cpp/aspose.words.ai/openaimodel/
---
## OpenAiModel class


Klasse, die die Integration von OpenAi-Modellen innerhalb von [Aspose.Words](../../aspose.words/) darstellt.

```cpp
class OpenAiModel : public Aspose::Words::AI::AiModel
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Überprüft die Grammatik des bereitgestellten Dokuments. Dieser Vorgang nutzt das verbundene [AI](../)-Modell zur Grammatikprüfung des Dokuments. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Erstellt eine neue Instanz der Klasse [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | Liest oder setzt die Anzahl der Millisekunden, die gewartet werden, bevor die Anfrage an das [AI](../)-Modell abläuft. Der Standardwert beträgt 100.000 Millisekunden (100 Sekunden). |
| [get_Url](./get_url/)() override | Liefert eine URL des Modells. Der Standardwert ist "https://api.openai.com/". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OpenAiModel](./openaimodel/)(const System::String\&, const System::String\&) | Initialisiert eine neue Instanz der Klasse [OpenAiModel](./). |
| [OpenAiModel](./openaimodel/)(const System::String\&) | Initialisiert eine neue Instanz der Klasse [OpenAiModel](./). |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Setter für [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | Setzt eine URL des Modells. Der Standardwert ist "https://api.openai.com/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Erstellt eine Zusammenfassung des angegebenen Dokuments, mit Optionen zur Anpassung der Länge der Zusammenfassung. Dieser Vorgang nutzt das verbundene [AI](../)-Modell zur Inhaltsverarbeitung. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Erstellt Zusammenfassungen für ein Array von Dokumenten, mit Optionen zur Steuerung der Zusammenfassungslänge und anderer Einstellungen. Diese Methode nutzt das verbundene [AI](../)-Modell zur Verarbeitung jedes Dokuments im Array. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Übersetzt das bereitgestellte Dokument in die angegebene Zielsprache. Dieser Vorgang nutzt das verbundene [AI](../)-Modell zur Inhaltsübersetzung. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Setzt einen angegebenen API-Schlüssel für das Modell. |
| [WithOrganization](./withorganization/)(const System::String\&) | Setzt eine angegebene Organisation für das Modell. |
| [WithProject](./withproject/)(const System::String\&) | Setzt ein angegebenes Projekt für das Modell. |

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

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
