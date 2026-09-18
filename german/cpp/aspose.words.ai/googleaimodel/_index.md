---
title: "Aspose::Words::AI::GoogleAiModel class"
linktitle: "GoogleAiModel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::AI::GoogleAiModel class. Klasse, die die Integration von Google AI-Modellen (Gemini) in Aspose.Words in C++ darstellt."
type: docs
weight: 2000
url: /de/cpp/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class


Klasse, die die Google [AI](../) Modelle (Gemini) Integration innerhalb von [Aspose.Words](../../aspose.words/) darstellt.

```cpp
class GoogleAiModel : public Aspose::Words::AI::AiModel
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Überprüft die Grammatik des bereitgestellten Dokuments. Dieser Vorgang nutzt das verbundene [AI](../)-Modell zur Grammatikprüfung des Dokuments. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Erstellt eine neue Instanz der Klasse [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | Liest oder setzt die Anzahl der Millisekunden, die gewartet werden, bevor die Anfrage an das [AI](../)-Modell abläuft. Der Standardwert beträgt 100.000 Millisekunden (100 Sekunden). |
| [get_Url](./get_url/)() override | Liefert eine URL des Modells. Der Standardwert ist "https://generativelanguage.googleapis.com/v1beta/models/". |
| [GetType](./gettype/)() const override |  |
| [GoogleAiModel](./googleaimodel/)(const System::String\&) | Initialisiert eine neue Instanz der Klasse [GoogleAiModel](./). |
| [GoogleAiModel](./googleaimodel/)(const System::String\&, const System::String\&) | Initialisiert eine neue Instanz der Klasse [GoogleAiModel](./). |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Setter für [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | Setzt eine URL des Modells. Der Standardwert ist "https://generativelanguage.googleapis.com/v1beta/models/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Fasst das angegebene [Document](../../aspose.words/document/) Objekt zusammen. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Fasst die angegebenen [Document](../../aspose.words/document/) Objekte zusammen. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Übersetzt ein angegebenes Dokument. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Setzt einen angegebenen API-Schlüssel für das Modell. |

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


Zeigt, wie man das Google [AI](../) Modell verwendet.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## Siehe auch

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
